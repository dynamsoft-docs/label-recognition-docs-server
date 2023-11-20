---
layout: default-layout
title: C++ User Guide - Dynamsoft Label Recognizer
description: This is the user guide page of Dynamsoft Label Recognizer for C++ Language.
keywords: c++, user guide
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /programming/cplusplus/user-guide.html
---

# User Guide - C++

In this guide, you will learn step by step on how to build a label recognizer application with Dynamsoft Label Recognizer SDK using C++ language.

> Read more on [Dynamsoft Label Recognizer Features]({{site.introduction}})

<span style="font-size:20px">Table of Contents</span>

- [User Guide - C++](#user-guide---c)
  - [Requirements](#requirements)
  - [Installation](#installation)
  - [Build Your First Application](#build-your-first-application)
    - [Create A New Project](#create-a-new-project)
      - [For Windows](#for-windows)
      - [For Linux](#for-linux)
    - [Include the Library](#include-the-library)
    - [Initialize a Capture Vision Router Instance](#initialize-a-capture-vision-router-instance)
    - [Recognize and Output Recognition Results](#recognize-and-output-recognition-results)
    - [Release the Allocated Memory](#release-the-allocated-memory)
    - [Build and Run the Project](#build-and-run-the-project)
      - [On windows](#on-windows)
      - [On Linux](#on-linux)
  - [Process Multiple Images](#process-multiple-images)
    - [Preparation Steps](#preparation-steps)
    - [Add an Image Source as the Input](#add-an-image-source-as-the-input)
    - [Add Captured Result Receiver](#add-captured-result-receiver)
    - [Start Recognition](#start-recognition)
    - [Release Allocated Memory](#release-allocated-memory)
    - [Build and Run the Project Again](#build-and-run-the-project-again)

## Requirements

- Windows
  - Windows 7, 8, 10, 2003, 2008, 2008 R2, 2012.
  - Visual Studio 2012 or above

- Linux
  - Linux x64: Ubuntu 14.04.4+ LTS, Debian 8+, etc.
  - GCC 5.4+

## Installation

If you don't have SDK yet, please go to <a href="https://www.dynamsoft.com/survey/dlr/?utm_source=docs" target="_blank">Dynamsoft website</a> to get it. After the folder is decompressed, the root directory of the DLR installation package is called `[INSTALLATION FOLDER]` in this guide.

## Build Your First Application

Let's start by creating a console application which demonstrates the minimum code needed to recognize text from an image file.

>You can download the complete source code from [here](https://github.com/Dynamsoft/label-recognizer-c-cpp-samples/tree/master/samples/HelloWorld/RecognizeAnImage).

### Create A New Project

#### For Windows

1. Open Visual Studio. Go to File > New > Project, select Empty App and enter `RecognizeAnImage` in the `name` text box.

2. Add a new source file named `RecognizeAnImage.cpp` into the project.

#### For Linux

1. Create a new source file named `RecognizeAnImage.cpp` and place it into the folder `[INSTALLATION FOLDER]\Dynamsoft\Resources\LabelRecognizer\Samples\HelloWorld\RecognizeAnImage`.

2. Create a file named `Makefile` and put it in the same directory as the file `RecognizeAnImage.cpp`. The content of `Makefile` is as follows:

    ```makefile
    CC=gcc
    CCFLAGS=-c -std=c++11

    DLRMODEL_PATH=../../../CharacterModel
    DS_LIB_PATH=../../../Lib/Linux/x64
    LDFLAGS=-L $(DS_LIB_PATH) -Wl,-rpath=$(DS_LIB_PATH) -Wl,-rpath=./
    DS_LIB=-lDynamsoftCaptureVisionRouter -lDynamsoftCore -lDynamsoftLicense

    STDLIB=-lstdc++

    TARGET=RecognizeAnImage
    OBJECT=RecognizeAnImage.o
    SOURCE=RecognizeAnImage.cpp

    # build rule for target.
    $(TARGET): $(OBJECT)
        $(CC) -o $(TARGET) $(OBJECT) $(STDLIB) $(DS_LIB) $(LDFLAGS)
        cp -r $(DLRMODEL_PATH) $(DS_LIB_PATH)

    # target to build an object file
    $(OBJECT): $(SOURCE)
        $(CC) $(CCFLAGS) $(SOURCE)

    # the clean target
    .PHONY : clean
    clean: 
        rm -f $(OBJECT) $(TARGET) -r $(DS_LIB_PATH)/CharacterModel
    ```

    >Note: The `DS_LIB_PATH` variable should be set to the correct directory where the DLR library files are located. The files and character models directory can be found in `[INSTALLATION FOLDER]/Dynamsoft/Lib/Linux/x64`.

### Include the Library

1. Add headers and libs in `RecognizeAnImage.cpp`.

    ```cpp
    #include <iostream>
    #include <string>
    #include "[INSTALLATION FOLDER]/Dynamsoft/Include/DynamsoftCaptureVisionRouter.h"

    using namespace std;
    using namespace dynamsoft::cvr;
    using namespace dynamsoft::dlr;
    using namespace dynamsoft::license;

    // The following code only applies to Windows.
    #if defined(_WIN64) || defined(_WIN32)
        #ifdef _WIN64
            #pragma comment(lib, "[INSTALLATION FOLDER]/Dynamsoft/Lib/Windows/x64/DynamsoftCaptureVisionRouterx64.lib")
            #pragma comment(lib, "[INSTALLATION FOLDER]/Dynamsoft/Lib/Windows/x64/DynamsoftCorex64.lib")
            #pragma comment(lib, "[INSTALLATION FOLDER]/Dynamsoft/Lib/Windows/x64/DynamsoftLicensex64.lib")
        #else
            #pragma comment(lib, "[INSTALLATION FOLDER]/Dynamsoft/Lib/Windows/x86/DynamsoftCaptureVisionRouterx86.lib")
            #pragma comment(lib, "[INSTALLATION FOLDER]/Dynamsoft/Lib/Windows/x86/DynamsoftCorex86.lib")
            #pragma comment(lib, "[INSTALLATION FOLDER]/Dynamsoft/Lib/Windows/x86/DynamsoftLicensex86.lib")
        #endif
    #endif
    ```

### Initialize a Capture Vision Router Instance

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
    CCaptureVisionRouter* router = new CCaptureVisionRouter();
    ```

### Recognize and Output Recognition Results

1. Recognize an image file

    ```cpp
    string imageFile = "[INSTALLATION FOLDER]/Dynamsoft/Resources/LabelRecognizer/Images/dlr-sample-vin.png";
    CCapturedResult* result = router->Capture(imageFile.c_str(), CPresetTemplate::PT_RECOGNIZE_TEXT_LINES);
    ```

    > Note:
    >
    > Please change all `[INSTALLATION FOLDER]` in above code snippet to your unpacking path.

2. Output the recognition results

    ```cpp
    cout << "File: " << imageFile << endl;

    if (result->GetErrorCode() != 0) {
        cout << "Error: " << result->GetErrorCode() << "," << result->GetErrorString() << endl;
    }

    int count = result->GetItemsCount();
    cout << "Recognized " << count << " text lines" << endl;
    for (int i = 0; i < count; i++) {
        const CCapturedResultItem* item = result->GetItem(i);

        CapturedResultItemType type = item->GetType();
        if (type == CapturedResultItemType::CRIT_TEXT_LINE) {
            const CTextLineResultItem* textLine = dynamic_cast<const CTextLineResultItem*>(item);

            cout << ">>Line result " << i << ": " << textLine->GetText() << endl;
        }
    }
    ```

### Release the Allocated Memory

```cpp
delete router, router = NULL;
delete result, result = NULL;   
```

### Build and Run the Project

#### On windows

1. Build the application through Visual Studio.

2. Copy the related DLL files to the same folder as the EXE file. The DLL files can be found in `[INSTALLATION FOLDER]\Dynamsoft\Lib\Windows\[platforms]`
    >Note: Select the corresponding folder (x86 or x64) based on your project's platform setting.

3. Copy the `[INSTALLATION FOLDER]\Dynamsoft\Resources\LabelRecognizer\CharacterModel` directory to the same folder as the EXE file.

4. Run the program `RecognizeAnImage.exe`.

#### On Linux

1. Open a terminal and change to the target directory where `Makefile` located in. Build the sample:

    ```sh
    >make
    ```

2. Run the program `RecognizeAnImage`.

    ```sh
    >./RecognizeAnImage
    ```

## Process Multiple Images

If you need to process multiple images at once instead of one image, you can follow these steps:

### Preparation Steps

1. [Create a new project](#create-a-new-project) named `RecognizeMultipleImages`.
2. [Initialize a Capture Vision Router Instance](#initialize-a-capture-vision-router-instance).
3. [Include the Library](#include-the-library).

>You can download the complete source code from [here](https://github.com/Dynamsoft/label-recognizer-c-cpp-samples/tree/master/samples/HelloWorld/RecognizeMultipleImages).

### Add an Image Source as the Input

The class `CDirectoryFetcher` is capable of converting a local directory to an image source. We will use it to connect multiple images to the image-processing engine.

1. Include additional `DynamsoftUtility` module which contains `CDirectoryFetcher`.

    ```cpp
    using namespace dynamsoft::utility;

    // The following code only applies to Windows.
    #if defined(_WIN64) || defined(_WIN32)
        #ifdef _WIN64
            #pragma comment(lib, "[INSTALLATION FOLDER]/Dynamsoft/Lib/Windows/x64/DynamsoftUtilityx64.lib")
        #else
            #pragma comment(lib, "[INSTALLATION FOLDER]/Dynamsoft/Lib/Windows/x86/DynamsoftUtilityx86.lib")
        #endif
    #endif
    ```

2. Setting up a directory fetcher to retrieve image data sources from a directory.

    ```cpp
    CDirectoryFetcher *dirFetcher = new CDirectoryFetcher;
    dirFetcher->SetDirectory("[Your Image Path]");

    router->SetInput(dirFetcher);
    ```

3. Create a class `MyImageSourceStateListener` to implement the `CImageSourceStateListenter` interface, and call `StopCapturing` in the callback function.

    ```cpp
    class MyImageSourceStateListener : public CImageSourceStateListener
    {
    private:
        CCaptureVisionRouter* m_router;

    public:
        MyImageSourceStateListener(CCaptureVisionRouter* router) {
            m_router = router;
        }

        virtual void OnImageSourceStateReceived(ImageSourceState state)
        {
            if(state == ISS_EXHAUSTED)
                m_router->StopCapturing();
        }
    };
    ```

4. Register the `MyImageSourceStateListener` object to monitor the status of the image source.

    ```cpp
    CImageSourceStateListener *listener = new MyImageSourceStateListener(router);
    router->AddImageSourceStateListener(listener);
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

            int lCount = pResult->GetItemsCount();
            cout << "Recognized " << lCount << " text lines" << endl;
            for (int li = 0; li < lCount; ++li)
            {
                const CTextLineResultItem* textLine = pResult->GetItem(li);
                cout << ">>Text line result " << li << ": " << textLine->GetText() << endl;
            }
        }
    };
    ```

    >For the error handling mechanism, the SDK returns Error Code in the `CRecognizedTextLinesResult` object. You can add error handling code as needed. See [Error Code]({{site.dcv_enumerations}}core/error-code.html) for a full list of supported error codes.

2. Register the `MyResultReceiver` object to monitor the captured results of the router.

    ```cpp
    CCapturedResultReceiver* recv = new MyResultReceiver();
    router->AddResultReceiver(recv);
    ```

### Start Recognition

1. Start recognition with the default Label Recognizer Template.

    ```cpp
    router->StartCapturing(CPresetTemplate::PT_RECOGNIZE_TEXT_LINES, true);
    ```

   >Note:
    >
    >- During the process, the callback function `OnRecognizedTextLinesReceived()` is triggered each time an image finishes processing. After all images are processed, the listener function `OnImageSourceStateReceived()` will return the image source state as `ISS_EXHAUSTED` and the process is stopped with the method `StopCapturing()`.

### Release Allocated Memory

```cpp
delete router, router = NULL;
delete dirFetcher, dirFetcher = NULL;
delete listener, listener = NULL;
delete recv, recv = NULL;
```

### Build and Run the Project Again

Please refer to [Build and Run the Project](#build-and-run-the-project).
