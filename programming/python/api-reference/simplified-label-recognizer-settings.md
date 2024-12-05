---
layout: default-layout
title: SimplifiedLabelRecognizerSettings Class - Dynamsoft Label Recognizer Module Python Edition API Reference
description: Definition of the SimplifiedLabelRecognizerSettings class in Dynamsoft Label Recognizer Module Python Edition.
keywords: class, python, SimplifiedLabelRecognizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# SimplifiedLabelRecognizerSettings

The `SimplifiedLabelRecognizerSettings` class contains settings for label recognition. It is a sub-parameter of [`SimplifiedCaptureVisionSettings`]({{ site.dcv_python_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html).

## Definition

```python
class SimplifiedLabelRecognizerSettings
```

## Properties

| Property  | Type |
| --------- | ---- |
| [`grayscale_transformation_modes`](#grayscale_transformation_modes) | *List[int]* |
| [`grayscale_enhancement_modes`](#grayscale_enhancement_modes) | *List[int]* |
| [`character_model_name`](#character_model_name) | *str* |
| [`line_string_regex_pattern`](#line_string_regex_pattern) | *str* |
| [`max_threads_in_one_task`](#max_threads_in_one_task) | *int* |
| [`scale_down_threshold`](#scale_down_threshold) | *int* |

### grayscale_transformation_modes

Specifies how grayscale transformations should be applied, including whether to process inverted grayscale images and the specific transformation mode to use.

It is a list of 8 integers, where each integer represents a mode specified by the [`EnumGrayscaleTransformationMode`]({{ site.dcv_enumerations }}core/grayscale-transformation-mode.html?lang=python) enumeration.

View the parameter reference page of <a href="{{ site.dcv_parameters_reference }}image-parameter/grayscale-transformation-modes.html?product=dlr&repoType=core" target="_blank">`GrayscaleTransformationModes`</a> for more detail about grayscale transformation modes.

### grayscale_enhancement_modes

Specifies how to enhance the quality of the grayscale image.

It is a list of 8 integers, where each integer represents a mode specified by the [`EnumGrayscaleEnhancementMode`]({{ site.dcv_enumerations }}core/grayscale-enhancement-mode.html?lang=python) enumeration.

View the parameter reference page of <a href="{{ site.dcv_parameters_reference }}image-parameter/grayscale-enhancement-modes.html?product=dlr&repoType=core" target="_blank">`GrayscaleEnhancementModes`</a> for more detail about grayscale enhancement modes.


### character_model_name

Specifies a character model by its name.

### line_string_regex_pattern

Specifies the RegEx pattern of the text line string to filter out the unqualified results.

### max_threads_in_one_task

Specifies the maximum available threads count in one label recognition task.

**Value Range**

[1, 256]

**Default value**

4

### scale_down_threshold

Specifies the threshold for the image shrinking.

**Value Range**

[512, 0x7fffffff]

**Default Value**

2300

**Remarks**

If the shorter edge size is larger than the given threshold value, the library will calculate the required height and width of the target image and shrink the image to that size before further operation. Otherwise, the library will perform operation on the original image.

## Methods
  
| Method | Description |
|------- | ---- |
| [`__init__`](#__init__) | Initializes a new instance of the `SimplifiedLabelRecognizerSettings` class. |

### \_\_init\_\_

Initializes a new instance of the `SimplifiedLabelRecognizerSettings` class.

```python
def __init__(self):
```

