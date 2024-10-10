---
layout: default-layout
title: Python User Guide - Dynamsoft Label Recognizer
description: This is the user guide page of Dynamsoft Label Recognizer SDK Python Edition.
keywords: python, user guide
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Getting Started with Dynamsoft Label Recognizer SDK Python Edition

In this guide, you will learn step by step on how to build a label recognition application with Dynamsoft Label Recognizer SDK using C#.

> Read more on [Dynamsoft Label Recognizer Features](https://www.dynamsoft.com/label-recognition/features/)

- [Getting Started with Dynamsoft Label Recognizer SDK Python Edition](#getting-started-with-dynamsoft-label-recognizer-sdk-python-edition)
  - [System Requirements](#system-requirements)
  - [Build Your First Application](#build-your-first-application)
    - [Create a New Project](#create-a-new-project)
    - [Install the NuGet Package](#install-the-nuget-package)
    - [Import the Namespace](#import-the-namespace)
    - [Initialize the License Key](#initialize-the-license-key)
    - [Create a CaptureVisionRouter Instance](#create-a-capturevisionrouter-instance)
    - [Invoke the Text Capturing](#invoke-the-text-capturing)
    - [Filter and Get Recognized Text Results](#filter-and-get-recognized-text-results)
    - [Build and Run the Project](#build-and-run-the-project)
  - [Process Multiple Images](#process-multiple-images)
    - [Import the Additional Namespace.](#import-the-additional-namespace)
    - [Create an ImageSource as the Input](#create-an-imagesource-as-the-input)
    - [Implement a CapturedResultReceiver as the Output Listener](#implement-a-capturedresultreceiver-as-the-output-listener)
    - [Handle Capture Stoppage by Implementing a ImageSource State Listener](#handle-capture-stoppage-by-implementing-a-imagesource-state-listener)
    - [Register the Input, Output Listener and ImageSource State Listener to the CaptureVisionRouter Instance](#register-the-input-output-listener-and-imagesource-state-listener-to-the-capturevisionrouter-instance)
    - [Start the Capturing Process](#start-the-capturing-process)
    - [Build and Run the Project Again](#build-and-run-the-project-again)

## System Requirements

To find out whether your environment is supported, please read the [System Requirements]({{ site.dlr_python }}index.html#system-requirements).

## Build Your First Application

Let's start by creating a console application which demonstrates how to use the minimum code to recognize text from an image file.

> You can <a href="https://github.com/Dynamsoft/label-recognizer-python-samples/tree/main/Samples/HelloWorld/RecognizeAnImage" target="_blank">download the entire source code from here</a>.

### Create a New Project

Start Visual Studio or your preferred C# IDE.

Create a new C# Console Application project.

### Install the NuGet Package

In the Solution Explorer, right-click on your project and select Manage NuGet Packages.

Search for and install the `Dynamsoft.DotNet.LabelRecognizer.Bundle` and `Dynamsoft.DotNet.character_model.NumberLetter` nuget package.

> If you prefer to use the offline packages, please
> 
> <a href="https://www.dynamsoft.com/label-recognition/downloads/?utm_source=docs" target="_blank">Download the `python Package`</a> now and extract it into a directory of your choice.
> 
> Add the extracted `.\Dynamsoft\Packages` directory as a new package source
> 
> Install following packages from the added package source:
> * Dynamsoft.DotNet.LabelRecognizer
> * Dynamsoft.DotNet.CaptureVisionRouter
> * Dynamsoft.DotNet.Core
> * Dynamsoft.DotNet.ImageProcessing
> * Dynamsoft.DotNet.License
> * Dynamsoft.DotNet.Utility
> * Dynamsoft.DotNet.NeuralNetwork
> * Dynamsoft.DotNet.character_model.NumberLetter

### Import the Namespace

Open the `Program.cs` file and add the following namespaces.

```python
using Dynamsoft.DLR
using Dynamsoft.Core
using Dynamsoft.CVR
using Dynamsoft.License
```

### Initialize the License Key

Open the `Program.cs` file and add the following code inside the `Main` method to initialize the license for using the SDK in the application:

```python
int error_code = 1
string errorMsg
error_code = LicenseManager.init_license("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", out errorMsg)
if (error_code != (int)EnumErrorCode.EC_OK && error_code != (int)EnumErrorCode.EC_LICENSE_CACHE_USED)
    Console.WriteLine("License initialization error: " + errorMsg)
```

> The string "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" here is a free public trial license. Note that network connection is required for this license to work. You can request a 30-day trial license via the [Request a Trial License](https://www.dynamsoft.com/customer/license/trialLicense?product=dlr&utm_source=guide&package=python){:target="_blank"} link.

### Create a CaptureVisionRouter Instance

```python
using (CaptureVisionRouter cvr = new CaptureVisionRouter())
{
    //code for invoking the text capturing
}
```

### Invoke the Text Capturing

```python
using (CaptureVisionRouter cvr = new CaptureVisionRouter())
{
    string imageFile = "[PATH-TO-THE-IMAGE-FILE]"
    CapturedResult? result = cvr.Capture(imageFile, PresetTemplate.PT_RECOGNIZE_TEXT_LINES)
    //code for filtering and getting recognition results
}
```

> Please change the `[PATH-TO-THE-IMAGE-FILE]` to a real image file path.
> 
> Sample images are also available in the `\Dynamsoft\Resources\LabelRecognizer\Images` directory within the downloaded `python Package`.

### Filter and Get Recognized Text Results

```python
if (result == null)
{
    Console.WriteLine("No Result.")
}
else if(result.get_error_code() != 0)
{
    Console.WriteLine("Error: " + result.get_error_code() + ", " + result.get_error_string())
}
else
{
    RecognizedTextLinesResult? textLinesResult = result.get_recognized_text_lines_result()
    if (textLinesResult != null)
    {
        TextLineResultItem[] items = textLinesResult.get_items()
        Console.WriteLine("Recognized " + items.Length + " text lines")
        foreach (TextLineResultItem textLineItem in items)
        {
            Console.WriteLine(">>Line result : " + Array.IndexOf(items, textLineItem) + ": " + textLineItem.get_text())
        }
    }
}
```

### Build and Run the Project

Save the `Program.cs` file and then compile and run the program using your IDE (such as Visual Studio). You will see the output message in the console like

```
Recognized 2 text lines
>>Line result : 1: XXX
>>Line result : 2: XXX
```

## Process Multiple Images

If, instead of processing one single image, you need to process many images at once, you can follow these steps:

> These steps follow the step [Create a CaptureVisionRouter Instance](#create-a-capturevisionrouter-instance) mentioned above.

> You can <a href="https://github.com/Dynamsoft/label-recognizer-python-samples/tree/main/Samples/HelloWorld/RecognizeMultipleImages" target="_blank">download the entire source code from here</a>.

### Import the Additional Namespace.

```python
using Dynamsoft.Utility
```

### Create an ImageSource as the Input

An `ImageSource` is required when crreating a multi-image processing application. You can either utilize ready-made image sources such as [`FileFetcher`]({{ site.dcv_python_api }}utility/file-fetcher.html) and [`DirectoryFetcher`]({{ site.dcv_python_api }}utility/directory-fetcher.html), or customize your own image source based on the base class [`ImageSourceAdapter`]({{ site.dcv_python_api }}core/basic-classes/image-source-adapter.html).

In this sample, we will use the `DirectoryFetcher` to retrieve images from a local directory.

```python
DirectoryFetcher fetcher = new DirectoryFetcher()
fetcher.set_directory("[THE DIRECTORY THAT HOLDS THE IMAGES]")
```

> Please change the `[THE DIRECTORY THAT HOLDS THE IMAGES]` to full path of the directory holding image files.
> 
> Sample images are also available in the `\Dynamsoft\Resources\LabelRecognizer\Images` directory within the downloaded `python Package`.

### Implement a CapturedResultReceiver as the Output Listener

Create a class `MyCapturedResultReceiver` to implement the `CapturedResultReceiver` class, and get the recognized text results in `on_recognized_text_lines_received` callback function.

```python
class MyCapturedResultReceiver : CapturedResultReceiver
{
    public override void on_recognized_text_lines_received(RecognizedTextLinesResult result)
    {
        FileImageTag? tag = (FileImageTag?)result.get_original_image_tag()
        Console.WriteLine("File: " + tag.get_file_path())
        if (result.get_error_code() != (int)EnumErrorCode.EC_OK)
        {
            Console.WriteLine("Error: " + result.get_error_string())
        }
        else
        {
            TextLineResultItem[] items = result.get_items()
            Console.WriteLine("Recognized " + items.Length + " text lines")
            foreach (TextLineResultItem item in items)
            {
                Console.WriteLine(">>Line result : " + Array.IndexOf(items, item) + ": " + item.get_text())
            }
        }
        Console.WriteLine()
    }
}
```

### Handle Capture Stoppage by Implementing a ImageSource State Listener

Create a class `MyImageSourceStateListener` to implement the `ImageSourceStateListener` class, and call stop_capturing in `on_image_source_state_received` callback function when the state is `ISS_EXHAUSTED`.

```python
class MyImageSourceStateListener : ImageSourceStateListener
{
    private CaptureVisionRouter? cvr = null
    public MyImageSourceStateListener(CaptureVisionRouter cvr)
    {
        this.cvr = cvr
    }
    public void on_image_source_state_received(EnumImageSourceState state)
    {
        if (state == EnumImageSourceState.ISS_EXHAUSTED)
        {
            if (cvr != null)
            {
                cvr.stop_capturing()
            }
        }
    }
}
```

### Register the Input, Output Listener and ImageSource State Listener to the CaptureVisionRouter Instance

```python
cvr.set_input(fetcher)
CapturedResultReceiver receiver = new MyCapturedResultReceiver()
cvr.add_result_receiver(receiver)
MyImageSourceStateListener listener = new MyImageSourceStateListener(cvr)
cvr.add_image_source_state_listener(listener)
```

### Start the Capturing Process

Call the method `start_capturing()` to start processing all the images in the specified folder.

```python
error_code = cvr.start_capturing(PresetTemplate.PT_RECOGNIZE_TEXT_LINES, true, out errorMsg)
if (error_code != (int)EnumErrorCode.EC_OK)
{
    Console.WriteLine("error: " + errorMsg)
}
```

During the process, the callback function `on_recognized_text_lines_received()` is triggered each time processing of an image is finished. After all images are processed, the listener function `on_image_source_state_received()` will be triggered while the image source state is `ISS_EXHAUSTED` and the process is stopped with the method `stop_capturing()`.

### Build and Run the Project Again

Please refer to [Build and Run the Project](#build-and-run-the-project).
