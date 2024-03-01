---
layout: default-layout
title: struct SimplifiedLabelRecognizerSettings - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the SimplifiedLabelRecognizerSettings struct of the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: struct, c++, SimplifiedLabelRecognizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ SimplifiedLabelRecognizerSettings Struct
permalink: /programming/cplusplus/api-reference/simplified-label-recognizer-settings-v3.0.10.html
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
    char reserved[512];
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
| [`reserved`](#reserved) | *char[512]* |

### grayscaleTransformationModes

Set the grayscale transformation modes with an array of enumeration `GrayscaleTransformationMode`. View the reference page of <a href="{{ site.dcv_enumerations}}core/grayscale-transformation-mode.html?src=cpp&&lang=cpp" target="_blank">`GrayscaleTransformationMode`</a> for more detail about grayscale transformation modes.

```cpp
GrayscaleTransformationMode grayscaleTransformationModes[8];
```

### grayscaleEnhancementModes

Set the grayscale enhancement modes with an array of enumeration `GrayscaleEnhancementMode`. View the reference page of <a href="{{ site.dcv_enumerations}}core/grayscale-enhancement-mode.html?src=cpp&&lang=cpp" target="_blank">`GrayscaleEnhancementMode`</a> for more detail about grayscale enhancement modes.

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
