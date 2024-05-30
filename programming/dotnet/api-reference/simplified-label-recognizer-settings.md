---
layout: default-layout
title: SimplifiedLabelRecognizerSettings Class - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: Definition of the SimplifiedLabelRecognizerSettings class in Dynamsoft Label Recognizer Module .NET Edition.
keywords: class, .NET, SimplifiedLabelRecognizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# SimplifiedLabelRecognizerSettings

The `SimplifiedLabelRecognizerSettings` class contains settings for label recognition. It is a sub-parameter of [`SimplifiedCaptureVisionSettings`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html).

## Definition

```csharp
public class SimplifiedLabelRecognizerSettings
```

## Attributes

| Attribute | Type |
| --------- | ---- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *EnumGrayscaleTransformationMode[]* |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *EnumGrayscaleEnhancementMode[]* |
| [`characterModelName`](#charactermodelname) | *string* |
| [`lineStringRegExPattern`](#linestringregexpattern) | *string* |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* |
| [`scaleDownThreshold`](#scaledownthreshold) | *int* |

### grayscaleTransformationModes

Set the grayscale transformation modes using an [`EnumGrayscaleEnhancementMode`]({{ site.dcv_enumerations }}core/grayscale-transformation-mode.html?lang=dotnet) array with 8 elements. View the reference page of <a href="{{ site.dcv_parameters_reference }}image-parameter/grayscale-transformation-modes.html?product=dlr&repoType=core" target="_blank">`GrayscaleTransformationModes`</a> for more detail about grayscale transformation modes.

```csharp
EnumGrayscaleEnhancementMode[] grayscaleTransformationModes;
```

### grayscaleEnhancementModes

Set the grayscale enhancement modes using an [`EnumGrayscaleTransformationMode`]({{ site.dcv_enumerations }}core/grayscale-enhancement-mode.html?lang=dotnet) array with 8 elements. View the reference page of <a href="{{ site.dcv_parameters_reference }}image-parameter/grayscale-enhancement-modes.html?product=dlr&repoType=core" target="_blank">`GrayscaleEnhancementModes`</a> for more detail about grayscale enhancement modes.

```csharp
EnumGrayscaleTransformationMode[] grayscaleEnhancementModes;
```

### characterModelName

Specify a character model by its name.

```csharp
string characterModelName;
```

### lineStringRegExPattern

Set the RegEx pattern of the text line string to filter out the unqualified results.

```csharp
string lineStringRegExPattern;
```

### maxThreadsInOneTask

Set the maximum available threads count in one label recognition task.

```csharp
int maxThreadsInOneTask;
```

**Value Range**

[1, 256]

**Default value**

4

### scaleDownThreshold

Sets the threshold for the image shrinking.

```csharp
int scaleDownThreshold;
```

**Value Range**

[512, 0x7fffffff]

**Default Value**

2300

**Remarks**

If the shorter edge size is larger than the given threshold value, the library will calculate the required height and width of the target image and shrink the image to that size before further operation. Otherwise, the library will perform operation on the original image.

