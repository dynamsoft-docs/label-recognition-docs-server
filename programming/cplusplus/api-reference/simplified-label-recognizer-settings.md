---
layout: default-layout
title: struct SimplifiedLabelRecognizerSettings - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the SimplifiedLabelRecognizerSettings struct of the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: struct, c++, SimplifiedLabelRecognizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ SimplifiedLabelRecognizerSettings Struct
---

# SimplifiedLabelRecognizerSettings

The `SimplifiedLabelRecognizerSettings` struct contains settings for label recognition. It is a sub-parameter of `SimplifiedCaptureVisionSettings`

```cpp
typedef struct tagSimplifiedLabelRecognizerSettings
{
    GrayscaleTransformationMode grayscaleTransformationModes[8];
    GrayscaleEnhancementMode grayscaleEnhancementModes[8];
    char characterModelName[64];
    char lineStringRegExPattern[1024];
    int maxThreadsInOneTask;
    int scaleDownThreshold;
    char reserved[508];
} SimplifiedLabelRecognizerSettings;
```

## Attributes Summary

| Attribute | Type |
| --------- | ---- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *GrayscaleTransformationMode[8]* |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *GrayscaleEnhancementMode[8]* |
| [`characterModelName`](#charactermodelname) | *char[64]* |
| [`lineStringRegExPattern`](#linestringregexpattern) | *char[1024]* |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* |
| [`scaleDownThreshold`](#scaledownthreshold) | *int* |
| [`reserved`](#reserved) | *char[508]* |

### grayscaleTransformationModes

Set the grayscale transformation modes with an array of enumeration `GrayscaleTransformationMode`. View the reference page of <a href="{{ site.dcv_cpp_api}}core/enum-grayscale-transformation-mode.html?src=cpp&&lang=cpp" target="_blank">`GrayscaleTransformationMode`</a> for more detail about grayscale transformation modes.

```cpp
GrayscaleTransformationMode grayscaleTransformationModes[8];
```

### grayscaleEnhancementModes

Set the grayscale enhancement modes with an array of enumeration `GrayscaleEnhancementMode`. View the reference page of <a href="{{ site.dcv_cpp_api}}core/enum-grayscale-enhancement-mode.html?src=cpp&&lang=cpp" target="_blank">`GrayscaleEnhancementMode`</a> for more detail about grayscale enhancement modes.

```cpp
GrayscaleEnhancementMode grayscaleEnhancementModes[8];
```

### characterModelName

Specify a character model by its name.

```cpp
char characterModelName[64];
```

### lineStringRegExPattern

Set the RegEx pattern of the text line string to filter out the unqualified results.

```cpp
char lineStringRegExPattern[1024];
```

### maxThreadsInOneTask

Set the maximum available threads count in one label recognition task.

```cpp
int maxThreadsInOneTask;
```

**Value Range**

[1, 256]

**Default value**

4

**Remarks**

To keep a balance between speed and quality, the library concurrently runs four different threads by default.

### scaleDownThreshold

Sets the threshold for the image shrinking.

```cpp
int scaleDownThreshold;
```

**Value Range**

[512, 0x7fffffff]

**Default Value**

2300

**Remarks**

If the shorter edge size is larger than the given threshold value, the library will calculate the required height and width of the barcode image and shrink the image to that size before localization. Otherwise, the library will perform label localization on the original image.

### reserved

Reserved for future use.

```cpp
char reserved[508];
```
