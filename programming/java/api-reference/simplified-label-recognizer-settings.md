---
layout: default-layout
title: SimplifiedLabelRecognizerSettings Class - Dynamsoft Label Recognizer Module Java Edition API Reference
description: Definition of the SimplifiedLabelRecognizerSettings class in Dynamsoft Label Recognizer Module Java Edition.
keywords: class, java, SimplifiedLabelRecognizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# SimplifiedLabelRecognizerSettings

The `SimplifiedLabelRecognizerSettings` class contains settings for label recognition. It is a sub-parameter of [`SimplifiedCaptureVisionSettings`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html).

## Definition

*Package:* com.dynamsoft.dlr

```java
public class SimplifiedLabelRecognizerSettings
```

## Properties

| Property  | Type |
| --------- | ---- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *int[]* |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *int[]* |
| [`characterModelName`](#charactermodelname) | *String* |
| [`lineStringRegExPattern`](#linestringregexpattern) | *String* |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* |
| [`scaleDownThreshold`](#scaledownthreshold) | *int* |

### grayscaleTransformationModes

Specifies how grayscale transformations should be applied, including whether to process inverted grayscale images and the specific transformation mode to use.

It is an array of integers, where each integer represents a mode specified by the [`EnumGrayscaleTransformationMode`]({{ site.dcvb_java_api }}core/enum-grayscale-transformation-mode.html) enumeration.

View the parameter reference page of <a href="{{ site.dcvb_parameters_reference }}image-parameter/grayscale-transformation-modes.html?product=dlr&repoType=core" target="_blank">`GrayscaleTransformationModes`</a> for more detail about grayscale transformation modes.

### grayscaleEnhancementModes

Specifies how to enhance the quality of the grayscale image.

It is an array of integers, where each integer represents a mode specified by the [`EnumGrayscaleEnhancementMode`]({{ site.dcvb_java_api }}core/enum-grayscale-enhancement-mode.html) enumeration.

View the parameter reference page of <a href="{{ site.dcvb_parameters_reference }}image-parameter/grayscale-enhancement-modes.html?product=dlr&repoType=core" target="_blank">`GrayscaleEnhancementModes`</a> for more detail about grayscale enhancement modes.

### characterModelName

Specifies a character model by its name.

### lineStringRegExPattern

Specifies the RegEx pattern of the text line string to filter out the unqualified results.

### maxThreadsInOneTask

Specifies the maximum available threads count in one label recognition task.

**Value Range**

[1, 256]

**Default value**

4

### scaleDownThreshold

Specifies the threshold for the image shrinking.

**Value Range**

[512, 0x7fffffff]

**Default Value**

2300

**Remarks**

If the shorter edge size is larger than the given threshold value, the library will calculate the required height and width of the target image and shrink the image to that size before further operation. Otherwise, the library will perform operation on the original image.

