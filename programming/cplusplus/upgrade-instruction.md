---
title: Upgrade Instructions - Dynamsoft Label Recognizer C++ Edition
keywords: c++, cplusplus, upgrade
description: This page introduces how to upgrade Dynamsoft Label Recognizer
needAutoGenerateSidebar: false
permalink: /programming/cplusplus/upgrade-instruction.html
---

# How to Upgrade

## From 2.x to 3.x

`DynamsoftLabelRecognizer` SDK has been refactored to integrate with `DynamsoftCaptureVision (DCV)` architecture. Notice the following break changes when upgrading your SDK.

### Update the Included .h .lib & .dll/.so file

Since the SDK architecture is changed, you have to change you code for including the headers, libs(windows only). You can use the following code to replace your previous code.

```cpp
#include "[INSTALLATION FOLDER]/Include/DynamsoftCaptureVisionRouter.h"

using namespace std;
using namespace dynamsoft::license;
using namespace dynamsoft::cvr;
using namespace dynamsoft::dlr;

#if defined(_WIN64) || defined(_WIN32)
    #ifdef _WIN64
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x64/DynamsoftLicensex64.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x64/DynamsoftCaptureVisionRouterx64.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x64/DynamsoftCorex64.lib")
    #else
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x86/DynamsoftLicensex86.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x86/DynamsoftCaptureVisionRouterx86.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Lib/Windows/x86/DynamsoftCorex86.lib")
    #endif
#endif
```

Put the following **.dll/.so** files in your executable path:

- Windows
  - x64:
    - DynamsoftCaptureVisionRouterx64.dll
    - DynamsoftCorex64.dll
    - DynamsoftImageProcessingx64.dll
    - DynamsoftLabelRecognizerx64.dll
    - DynamsoftLicensex64.dll
    - DynamsoftUtilityx64.dll(Optional)

  - x86:
    - DynamsoftCaptureVisionRouterx86.dll
    - DynamsoftCorex86.dll
    - DynamsoftImageProcessingx86.dll
    - DynamsoftLabelRecognizerx86.dll
    - DynamsoftLicensex86.dll
    - DynamsoftUtilityx86.dll(Optional)

- Linux
  - x64:
    - libDynamsoftCaptureVisionRouter.so
    - libDynamsoftCore.so
    - libDynamsoftImageProcessing.so
    - libDynamsoftLabelRecognizer.so
    - libDynamsoftLicense.so
    - libDynamsoftUtility.so(Optional)

### Migrate from Class CLabelRecognizer to Class CCaptureVisionRouter

The `CCaptureVisionRouter` class serves as the central class of the DCV framework's execution flow. It encompasses the following functionalities:

- Retrieving images from the `ImageSourceAdapter`.
- Updating templates and configuring settings.
- Dynamically loading the `DynamsoftLabelRecognizer` module for label recognition.
- Dispatching the results to registered receivers of type `CapturedResultReceiver`.

### Templates Migration

The template system is upgraded. The template you used for the previous version can't be directly recognized by the new version. Please <a href="mailto:support@dynamsoft.com">contact us</a> to upgrade your template.

### Update Your Image Label Recognizing Codes

#### Single Image Label Recognizing

Please refer to the [user guide](../cplusplus/user-guide.md#create-a-new-project) for more detailed information on using the following `Capture` APIs instead of the `Recognize` APIs.

```cpp
// Capture from a file.
CCapturedResult* Capture(const char* filePath, const char* templateName="");
// Capture from a file in memory.
CCapturedResult* Capture(const unsigned char *fileBytes, int fileSize, const char* templateName="");
// Capture from a CImageData object.
CCapturedResult* Capture(const CImageData* pImageData, const char* templateName="");
```

> Note: The `Capture` API is designed to recognize text in single-page files, such as images or PDFs. If you need to extract text from multi-page files, it is recommended to use the [`FileFetcher`]({{site.dcv_cpp_api}}utility/file-fetcher.html) instead.

#### Batch Image Label Recognizing

1. DCV architecture allows you to set a folder as an image source to fetch image from. To use this feature, you have to set [`DirectoryFetcher`]({{site.dcv_cpp_api}}utility/directory-fetcher.html) as the input via class `CCaptureVisionRouter`.
2. You need to register a [`CCapturedResultReceiver`]({{site.dcv_cpp_api}}core/basic-structures/captured-result-receiver.html) to receive the label recognizing results.
3. Please refer to the [user guide](../cplusplus/user-guide.md#process-multiple-images) for more details.

>Note: creating multiple `CCaptureVisionRouter` instances might cause crash bugs. Multi-thread processing is internally implemented. As a result you don't need to create multi-thread code by yourself.

### Update Your Video Streaming Label Recognizing Codes

`CImageSourceAdapter` is added to replace the `FrameDecodeingParameters` and the previous video methods. The following steps shows how to implement video streaming label recognizing with `CImageSourceAdapter`:

```cpp
class MyImageSource : public CImageSourceAdapter 
{
  // Add code to implement CImageSourceAdapter
};
int main()
{
    CCaptureVisionRouter cvr;

    MyImageSource* source = new MyImageSource;
    cvr.SetInput(source);
}
```

>Note: creating multiple `CCaptureVisionRouter` instances might cause crash bugs. Multi-thread processing is internally implemented. As a result you don't need to create multi-thread code by yourself.
