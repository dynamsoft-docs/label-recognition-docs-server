---
layout: default-layout
title: Main Page - Dynamsoft Label Recognizer for C++
description: This is the main page of Dynamsoft Label Recognizer for C++ Language.
keywords: c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /programming/c-cplusplus/cpp-index.html
---

# C++ Edition Introduction

Dynamsoft Label Recognizer (DLR) is an SDK designed to recognize meaningful zonal text or symbols in an image (or a 'Label' in this context). Starting from version 3.0, the DLR is designed based on a new [DCV architecture]({{site.dcv_arch}}). The CVR module will serve as the active organizer and coordinator, while the DLR module will become a passive algorithm module, dynamically loaded and used by the CVR.

## Modules of SDK

|Modules|Description|Header files|dll/so files|
|:---|:---|:---|:---|
|Capture Vision Router (CVR)        |Active organizer and coordinator                       |DynamsoftCaptureVisionRouter.h      |Windows:<br/>DynamsoftCaptureVisionRouter[**arch**].dll<br/><br/>Linux:<br/>DynamsoftCaptureVisionRouter.so|
|Dynamsoft Label Recognizer (DLR)   |Label recognition algorithms                           |DynamsoftLabelRecognizer.h          |Windows:<br/>DynamsoftLabelRecognizer[**arch**].dll<br/><br/>Linux:<br/>DynamsoftLabelRecognizer.so|
|Dynamsoft Core (DC)                |Basic structures and common intermediate results       |DynamsoftCore.h                     |Windows:<br/>DynamsoftCore[**arch**].dll<br/><br/>Linux:<br/>DynamsoftCore.so|
|Dynamsoft Image Processing (DIP)   |Image processing algorithms                            |-                                   |Windows:<br/>DynamsoftImageProcessing[**arch**].dll<br/><br/>Linux:<br/>DynamsoftImageProcessing.so|
|Dynamsoft License (DL)             |License module                                         |DynamsoftLicense.h                  |Windows:<br/>DynamsoftLicense[**arch**].dll<br/><br/>Linux:<br/>DynamsoftLicense.so|
|Dynamsoft Utility (DU)             |Contains some useful utility classes                   |DynamsoftUtility.h                  |Windows:<br/>DynamsoftUtility[**arch**].dll<br/><br/>Linux:<br/>DynamsoftUtility.so|

>Note: **arch** refers to the CPU architecture for Windows edition, which could be either x86 or x64 here.

## Main Classes of SDK

- class CCaptureVisionRouter

The `CCaptureVisionRouter` class is a router responsible for obtaining images from the registered `CImageSourceAdatper` object, distributing them to the label recognition module for text recognition, and then calling back the `CCapturedResultReceiver` object registered by the user to return the `CRecognizedTextLinesResult` result.

- class CImageSourceAdapter

The `CImageSourceAdapter` class provides an interface for fetching and buffering images. It is an abstract class that needs to be implemented by a concrete class to provide actual functionality. The `CDirectoryFetcher` class inherits and implements `CImageSourceAdapter`, and obtains image files from the specified directory according to certain conditions.

- class CCapturedResultReceiver

The `CCaptureResultReceiver` class is responsible for receiving captured results. It contains several callback functions for different types of results, including raw image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results. The DLR recognition result is returned by the `OnRecognizedTextLinesReceived` callback function.

- class CRecognizedTextLinesResult

The `CRecognizedTextLinesResult` class represents the result of a text recognition process. It provides access to information about the recognized text lines, the source image, and any errors that occurred during the recognition process.


## Getting Started

- [User Guide](cpp-user-guide.md)

## API Reference

- [API Reference](api-reference/index.md)

## Release Notes

- [Version 3.x](release-notes/cpp-3.md)
- [Version 2.x]({{c-cplusplus-release-notes}}c-cpp-2.html)
- [Version 1.x]({{c-cplusplus-release-notes}}c-cpp-1.html)
