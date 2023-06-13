---
layout: default-layout
title: struct SimplifiedLabelRecognizerSettings - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the SimplifiedLabelRecognizerSettings struct of the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: struct, c++, SimplifiedLabelRecognizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ SimplifiedLabelRecognizerSettings Struct
permalink: /programming/c-cplusplus/api-reference/simplified-label-recognizer-settings.html
---

# SimplifiedLabelRecognizerSettings

The `SimplifiedLabelRecognizerSettings` struct contains settings for barcode decoding. It is a sub-parameter of `SimplifiedCaptureVisionSettings`

```cpp
typedef struct tagSimplifiedLabelRecognizerSettings
{
    GrayscaleTransformationMode grayscaleTransformationModes[8];
    GrayscaleEnhancementMode grayscaleEnhancementModes[8];
    char characterModelName[64];
    char lineStringRegExPattern[1024];
    int maxThreadsInOneTask;
    char reserved[512];
} SimplifiedLabelRecognizerSettings;
```

## Attributes Summary

| Attribute | Type |
| --------- | ---- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *GrayscaleTransformationMode[8]* |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *GrayscaleEnhancementMode[8]* |
| [`characterModelName`](#charactermodelname) | *LocalizationMode[8]* |
| [`lineStringRegExPattern`](#linestringregexpattern) | *DeblurMode[10]* |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* |
| [`reserved`](#reserved) | *char[512]* |

### grayscaleTransformationModes

Set the grayscale transformation modes with an array of enumeration `GrayscaleTransformationMode`. View the reference page of <a href="" target="_blank">`GrayscaleTransformationMode`</a> for more detail about grayscale transformation modes.

```cpp
GrayscaleTransformationMode grayscaleTransformationModes[8];
```

### grayscaleEnhancementModes

Set the grayscale enhancement modes with an array of enumeration `GrayscaleEnhancementModes`. View the reference page of <a href="" target="_blank">`GrayscaleEnhancementModes`</a> for more detail about grayscale enhancement modes.

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

### reserved

Reserved for future use.

```cpp
char reserved[512];
```
