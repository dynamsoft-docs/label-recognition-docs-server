---
layout: default-layout
title: C++ User Guide - Dynamsoft Label Recognizer
description: This is the user guide page of Dynamsoft Label Recognizer for C++ Language.
keywords: c++, user guide
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /programming/c-cplusplus/cpp-user-guide.html
---

# User Guide - C++

<span style="font-size:20px">Table of Contents</span>

- [User Guide - C++](#user-guide---c)
  - [Requirements](#requirements)
  - [Installation](#installation)
  - [Build Your First Application](#build-your-first-application)
    - [Create A New Project](#create-a-new-project)
      - [For Windows](#for-windows)
      - [For Linux](#for-linux)
    - [Include the Library](#include-the-library)
    - [Initialize the Capture Vision Router](#initialize-the-capture-vision-router)
    - [Set Input Image Source](#set-input-image-source)
    - [Add Captured Result Receiver](#add-captured-result-receiver)
    - [Start Recognition](#start-recognition)
    - [Build and Run the Project](#build-and-run-the-project)
      - [On windows](#on-windows)
      - [On Linux](#on-linux)

## Requirements

- Windows
  - Windows 7, 8, 10, 2003, 2008, 2008 R2, 2012.
  - Visual Studio 2012 or above

- Linux
  - Linux x64: Ubuntu 14.04.4+ LTS, Debian 8+, etc
  - GCC 4.2+

## Installation

If you don't have SDK yet, please go to <a href="https://www.dynamsoft.com/survey/dlr/?utm_source=docs" target="_blank">Dynamsoft website</a> to get it. Once the folder is decompressed, the root directory of the DLR installation package is `DynamsoftLabelRecognizer`, which we will refer to as `[INSTALLATION FOLDER]` throughout this guide.

## Build Your First Application

Let's start by creating a console application which demonstrates the minimum code needed to recognize text from an image file.

>You can download the complete source code referenced in this guide from [here](https://github.com/Dynamsoft/label-recognizer-c-cpp-samples/tree/master/samples/C++/HelloWorld).

### Create A New Project

#### For Windows

1. Open Visual Studio. Go to File > New > Project, select Empty App and enter `HelloWorld` in the `name` text box.

2. Add a new source file named `HelloWorld.cpp` into the project.

#### For Linux

1. Create a new source file named `HelloWorld.cpp` and place it into the folder `[INSTALLATION FOLDER]\Samples\C++\HelloWorld`.

2. Create a file named `Makefile` and put it in the same directory as the file `HelloWorld.cpp`. The content of `Makefile` is as follows:

    ```makefile
    CC=gcc
    CCFLAGS=-c

    DLRMODEL_PATH=../../../CharacterModel
    DLRLIB_PATH=../../../Lib/Linux/x64
    LDFLAGS=-L $(DLRLIB_PATH) -Wl,-rpath=$(DLRLIB_PATH) -Wl,-rpath=./
    DLRLIB=-lDynamsoftCaptureVisionRouter -lDynamsoftCore -lDynamsoftLicense -lDynamsoftUtitlity

    STDLIB=-lstdc++

    TARGET=HelloWorld
    OBJECT=HelloWorld.o
    SOURCE=HelloWorld.cpp

    # build rule for target.
    $(TARGET): $(OBJECT)
        $(CC) -o $(TARGET) $(OBJECT) $(STDLIB) $(DLRLIB) $(LDFLAGS)
        cp -r $(DLRMODEL_PATH) $(DLRLIB_PATH)

    # target to build an object file
    $(OBJECT): $(SOURCE)
        $(CC) $(CCFLAGS) $(SOURCE)

    # the clean target
    .PHONY : clean
    clean: 
        rm -f $(OBJECT) $(TARGET) -r $(DLRLIB_PATH)/CharacterModel
    ```

    >Note: The `DLRLIB_PATH` variable should be set to the correct directory where the DLR library files are located. The files and character models directory can be found in `[INSTALLATION FOLDER]/Lib/Linux/x64`.

### Include the Library

1. Add headers and libs in `HelloWorld.cpp`.

    ```cpp
    #include <iostream>
    #include "<relative path>/Include/DynamsoftCaptureVisionRouter.h"
    #include "<relative path>/Include/DynamsoftLicense.h"
    #include "<relative path>/Include/DynamsoftUtility.h"

    using namespace std;
    using namespace dynamsoft::cvr;
    using namespace dynamsoft::dlr;
    using namespace dynamsoft::license;
    using namespace dynamsoft::basic_structures;
    using namespace dynamsoft::utility;

    // The following code only applies to Windows.
    #if defined(_WIN64) || defined(_WIN32)
        #ifdef _WIN64
            #pragma comment(lib, "<relative path>/Lib/Windows/x64/DynamsoftCaptureVisionRouterx64.lib")
            #pragma comment(lib, "<relative path>/Lib/Windows/x64/DynamsoftCorex64.lib")
            #pragma comment(lib, "<relative path>/Lib/Windows/x64/DynamsoftUtilityx64.lib")
            #pragma comment(lib, "<relative path>/Lib/Windows/x64/DynamsoftLicensex64.lib")
        #else
            #pragma comment(lib, "<relative path>/Lib/Windows/x86/DynamsoftCaptureVisionRouterx86.lib")
            #pragma comment(lib, "<relative path>/Lib/Windows/x86/DynamsoftCorex86.lib")
            #pragma comment(lib, "<relative path>/Lib/Windows/x64/DynamsoftUtilityx86.lib")
            #pragma comment(lib, "<relative path>/Lib/Windows/x86/DynamsoftLicensex86.lib")
        #endif
    #endif
    ```

    >Please replace `<relative path>` in the above code with the relative path to the `HelloWorld.cpp` file. The c++ header file can be found in `[INSTALLATION FOLDER]/Include/`. The import lib files (only for Windows) can be found in `[INSTALLATION FOLDER]/Lib/Windows/[platform]`.

### Initialize the Capture Vision Router

1. Initialize the license key

    ```cpp
    char error[512];
    
    CLicenseManger::InitLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", error, 512);
    cout << "License initialization: " << error << endl;
    ```

    >Note:
    >
    >- An internet connection is required for the license to work.
    >- "DLS2***" is a default free public trial license used in the sample.
    >- If the license has expired, please request an extension through the <a href="https://www.dynamsoft.com/customer/license/trialLicense?utm_source=docs" target="_blank">customer portal</a>.

2. Create an instance of Dynamsoft Capture Vision Router

    ```cpp
    CCaptureVisionRouter router;
    ```

### Set Input Image Source

1. Setting up a directory fetcher to retrieve image data sources from a directory.

    ```cpp
    CDirectoryFetcher dirFetcher;
    dirFetcher.SetDirectory("[Your Image Path]");

    router.SetInput(&dirFetcher);
    ```

2. Create a class `MyImageSourceStateListener` to implement the `CImageSourceStateListenter` interface, and call `StopCapturing` in the callback function.

    ```cpp
    class MyImageSourceStateListener : public CImageSourceStateListener
    {
    private:
        CCaptureVisionRouter* m_router;

    public:
        MyImageSourceStateListener(CCaptureVisionRouter* router) {
            m_router = router;
        }

        virtual void OnImageSourceStateChanged(ImageSourceState state)
        {
            if(state == ISS_EXHAUSTED)
                m_router->StopCapturing();
        }
    };
    ```

3. Register the `MyImageSourceStateListener` object to monitor the status of the image source.

    ```cpp
    MyImageSourceStateListener listener(&router);
    router.AddImageSourceAdapterStateListener(&listener);
    ```

### Add Captured Result Receiver

1. Create a class `MyResultReceiver` to implement the `CCapturedResultReceiver` interface, and get the recognition results in `OnRecognizedTextLinesReceived` callback function.

    ```cpp
    class MyResultReceiver : public CCapturedResultReceiver
    {
    public:
        virtual void OnRecognizedTextLinesReceived(const CRecognizedTextLinesResult* pResult)
        {
            if(pResult->GetErrorCode() != EC_OK)
                cout << "Error: " << pResult->GetErrorString() << endl;

            int lCount = pResult->GetCount();
            cout << "Recognized " << lCount << " text lines" << endl;
            for (int li = 0; li < lCount; ++li)
            {
                const CTextLineResultItem* textLine = pResult->GetItem(li);
                cout << ">>Text line result " << li << ": " << textLine->GetText() << endl;
            }
        }
    };
    ```

    >For the error handling mechanism, the SDK returns Error Code in the `CRecognizedTextLinesResult` object. You can add error handling code as needed. See [Error Code]({{site.enumerations}}error-code.html) for a full list of supported error codes.

2. Register the `MyResultReceiver` object to monitor the captured results of the router.

    ```cpp
    MyResultReceiver recv;
    router.AddResultReceiver(&recv);
    ```

### Start Recognition

1. Start recognition with the default Label Recognizer Template.

    ```cpp
    router.StartCapturing("recognize-textlines", true);
    ```

   >Note:
    >
    >- The second parameter is set to true, all images in the folder will be processed before returning. If set to false, it will return immediately.
    >- You can also manually call StopCapturing to stop the current recognition task..

You can download the similar complete source code from [Here](https://github.com/Dynamsoft/label-recognizer-c-cpp-samples/tree/master/samples/C++/HelloWorld).

### Build and Run the Project

#### On windows

1. Build the application through Visual Studio.

2. Copy the related DLL files to the same folder as the EXE file. The DLL files can be found in `[INSTALLATION FOLDER]\Lib\Windows\[platforms]`
    >Note: Select the corresponding folder (x86 or x64) based on your project's platform setting.

3. Copy the `[INSTALLATION FOLDER]\CharacterModel` directory to the same folder as the EXE file.

4. Run the program `HelloWorld.exe`.

#### On Linux

1. Open a terminal and change to the target directory where `Makefile` located in. Build the sample:

    ```sh
    >make
    ```

2. Run the program `HelloWorld`.

    ```sh
    >./HelloWorld
    ```
