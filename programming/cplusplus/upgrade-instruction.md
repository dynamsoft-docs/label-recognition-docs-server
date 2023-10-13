---
title: Upgrade Instructions - Dynamsoft Label Recognizer C++ Edition
keywords: c++, cplusplus, upgrade
description: This page introduces how to upgrade Dynamsoft Label Recognizer
needAutoGenerateSidebar: false
permalink: /programming/cplusplus/upgrade-instruction.html
---

# How to Upgrade

## From 2.x to 3.x

Dynamsoft Label Recognizer SDK has been refactored to integrate with [`DynamsoftCaptureVision (DCV)`]({{ site.dcv_introduction }}) architecture. Notice the following break changes when upgrading your SDK.

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
        #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x64/DynamsoftLicensex64.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x64/DynamsoftCaptureVisionRouterx64.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x64/DynamsoftCorex64.lib")
    #else
        #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x86/DynamsoftLicensex86.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x86/DynamsoftCaptureVisionRouterx86.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x86/DynamsoftCorex86.lib")
    #endif
#endif
```

**Distribution**

- Copy `[INSTALLATION FOLDER]/Distributables/DLR-PresetTemplates.json` to the same folder as the executable program.
- Copy the libraries to the same folder as the executable program.
  - For Windows: Copy **ALL** `*.dll` files under `[INSTALLATION FOLDER]/Distributables/Lib/Windows/[platform]`. Replace `[platform]` with your project's platform setting.
  - For Linux: Copy **ALL** `*.so` files under `[INSTALLATION FOLDER]/Distributables/Lib/Linux/[platform]`. Replace `[platform]` with your project's platform setting.

### Update Single Image Recognizing APIs

The APIs for recognizing single image has been adjusted as follows:

| Old APIs | New APIs |
| :----------- | :------- |
| `CLabelRecognizer.RecognizeFile` | `CCaptureVisionRouter.Capture(const char* filePath, const char* templateName)` |
| `CLabelRecognizer.RecognizeFileInMemory` | `CCaptureVisionRouter.Capture(const unsigned char *fileBytes, int fileSize, const char* templateName)` |
| `CLabelRecognizer.RecognizeBuffer` | `CCaptureVisionRouter.Capture(const CImageData* pImageData, const char* templateName)` |
| `struct DLR_Result` | `class CTextLineResultItem` |
| `struct DLR_ResultArray` | `class CCapturedResult` |

> Note: The `Capture` API is designed to recognize text in single-page files, such as images or PDFs. If you need to extract text from multi-page files, it is recommended to use the [`CFileFetcher`]({{site.dcv_cpp_api}}utility/file-fetcher.html) instead.

### Update Video Streaming Recognizing Code

`CImageSourceAdapter` is added to replace the `FrameDecodeingParameters` and the previous video methods. You should implement `CImageSourceAdapter` to transfer image data from camera or video file to buffer. The following code snippet demonstrate basic usage of recognizing video frames:

```cpp
class MyVideoSource : public CProactiveImageSourceAdapter 
{
    // You should implement the `HasNextImageToFetch` method to indicate if there is a next frame
    bool HasNextImageToFetch() const override 
    {
        return true;
    }

    // You should implement the `FetchImage` method to get the next frame
    CImageData* FetchImage() override
    {
        // Add code to get the video frame from camera or video file
    }
};

class MyTextLineResultReceiver: public CCapturedResultReceiver
{
public:
    virtual void OnRecognizedTextLinesReceived(RecognizedTextLinesResult * result) {
        // Add code to process the result
    }
};

int main()
{
    CCaptureVisionRouter *cvr = new CCaptureVisionRouter;

    // Create your video source and bind it to the router
    MyVideoSource *source = new MyVideoSource;
    cvr->SetInput(source);

    // Create a CCapturedResultReceiver instance 
    MyTextLineResultReceiver *labelReceiver = new MyTextLineResultReceiver;
    cvr->AddResultReceiver(labelReceiver);

    // Start capturing
    errorCode = cvr->StartCapturing(CPresetTemplate::PT_RECOGNIZE_TEXT_LINES, true, errorMsg, 512);

    delete labelReceiver;
    delete source;
    delete cvr;
}
```

### Update Images Batch Recognizing Code

1. DCV architecture allows you to set a folder as an image source to fetch image from. To use this feature, you have to set [`CDirectoryFetcher`]({{site.dcv_cpp_api}}utility/directory-fetcher.html) as the input via class `CCaptureVisionRouter`.
2. You need to register a [`CCapturedResultReceiver`]({{site.dcv_cpp_api}}core/basic-structures/captured-result-receiver.html) to receive the label recognizing results.
3. Please refer to the [`user guide`](../cplusplus/user-guide.md#process-multiple-images) for more details.

### Migrate Your Templates

The template system is upgraded. The template you used for the previous version can't be directly recognized by the new version. Please <a href="mailto:support@dynamsoft.com">contact us</a> to upgrade your template.
