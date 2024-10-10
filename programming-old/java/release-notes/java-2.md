---
layout: default-layout
title: Java SDK Release Notes 2.x - Dynamsoft Label Recognizer
description: This is the release notes page of Dynamsoft Label Recognizer for Java SDK version 2.x.
keywords: release notes, java
needAutoGenerateSidebar: false
permalink: /programming/java/release-notes/java-2.html
---

# Release Notes - Java 2.x

## 2.2.10 (06/27/2024)

### Highlights

{%- include release-notes/product-highlight-2.2.md -%}

### Changelog

#### New

- Added a new property [`timeout`](../../java/api-reference/dlr-runtime-settings.html#timeout) to [`DLRRuntimeSettings`](../../java/api-reference/dlr-runtime-settings.html) class.
- Added modes parameter `CharacterNormalizationModes` to normalize the text. The parameter is available under the following classes:
  - `LabelRecognizerParameter`
  - `TextArea`
  - `LineSpecification`

#### Improved

- Reduced the size of MRZ model from 10MB to 2.56MB.
- Improved single-line text confidence. This enables users to implement a result confidence filter to improve the recognition accuracy.
- Improved character segmentation when processing some connected characters. This improves the recognition accuracy.

## 2.0 (08/26/2021)

### Highlights

{%- include release-notes/product-highlight-2.0.md -%}

### Changelog

#### New
- Added auto-deskew algorithm to improve the performance on recognizing the skewed characters. 
- Added package `dynamsoft-core.jar`. Migrated the Dynamsoft core classes from package `dynamsoft-labelrecognizer.jar` to `dynamsoft-core.jar `.
- Added class [`BarcodeResult`](../api-reference/barcode-result.html) for users to interact with Dynamsoft Barcode Reader SDK.
- Added [`DLRRuntimeSettings`](../api-reference/dlr-runtime-settings.html) property [`dictionaryPath`](../api-reference/dlr-runtime-settings.html#dictionarypath) and [`dictionaryCorrectionThreshold`](../api-reference/dlr-runtime-settings.html#dictionarycorrectionthreshold) for users to further improve the recognizing accuracy by referencing dictionary files.
- Added class [`DLRDictionaryCorrectionThreshold`](../api-reference/dlr-dictionary-correction-threshold.html).
- Added class [`DLRFurtherModes`](../api-reference/dlr-further-modes.html) and property [`DLRRuntimeSettings.furtherModes`](../api-reference/dlr-runtime-settings.html#furthermodes) for users to config more processing modes.
- Added enumeration  [`TextureDetectionMode`]({{ site.dlr_enumerations }}texture-detection-mode.html) and property [`DLRFurtherModes.textureDetectionModes`](../api-reference/dlr-further-modes.html#texturedetectionmodes) for users to detect and remove the texture background.
- Added enumeration  [`ColourConversionMode`]({{ site.dlr_enumerations }}colour-conversion-mode.html) and property [`DLRFurtherModes.colourConversionModes`](../api-reference/dlr-further-modes.html#colourconversionmodes) for users to convert color images to grayscale images in differenct ways. 
- Added enumeration [`BinarizationMode`]({{ site.dlr_enumerations }}binarization-mode.html) and property [`DLRRuntimeSettings.binarizationModes`](../api-reference/dlr-runtime-settings.html#binarizationmodes) for users to convert grayscale images to binary images in different ways. 
- Added enumeration [`GrayscaleEnhancementMode`]({{ site.dlr_enumerations }}grayscale-enhancement-mode.html) and property [`DLRFurtherModes.grayscaleEnhancementModes`](../api-reference/dlr-further-modes.html#grayscaleenhancementmodes) for users to enable grayscale images preprocessing.
- Added [`characterHConfidence`](../api-reference/dlr-character-result.html#characterhconfidence), [`characterMConfidence`](../api-reference/dlr-character-result.html#charactermconfidence) and [`characterLConfidence`](../api-reference/dlr-character-result.html#characterlconfidence) properties in [`DLRCharacterResult`](../api-reference/dlr-character-result.html) class so that more alternative results will be available for users.

#### Improved
- Improved the neural network performance by replacing Caffe engine with OpenCV DNN engine.

#### Fixed
- Fixed a bug that might cause wrong line number matching when using [`LineSpecification.LineNumber`]({{ site.dlr_parameters_reference }}line-specification/parameter-control.html#linenumber).

#### API Changes
- Modified the method `initLicense(String)` to static [`initLicense(String)`](../api-reference/label-recognizer.html#initlicense).
- Modified the parameter type of the method [`updateReferenceRegionFromBarcodeResults`](../api-reference/label-recognizer.html#updatereferenceregionfrombarcoderesults) from `TextResult[]` to `BarcodeResult[]`.
- Modified the parameters [`LabelRecognizerParameter.LetterHeightRange`]({{ site.dlr_parameters_reference }}label-recognition-parameter/parameter-control.html#letterheightrange) and [`TextArea.LetterHeightRange`]({{ site.dlr_parameters_reference }}text-area/parameter-control.html#letterheightrange). The value unit of the parameters are modified from percentage to thousandth. The available range of the value and the default value are updated as well.
- Renamed class `LabelRecognition` to [`LableRecognizer`](../api-reference/label-recognizer.html).
- Removed method `initLicenseFromLTS`. 
- Removed method `LabelRecognizer(string license)`.
- Removed method `initLTSConnectionParameters`.
- Removed class `DMLTSConnectionParameters`.

