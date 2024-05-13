---
layout: default-layout
title: .Net SDK Release Notes 2.x - Dynamsoft Label Recognizer
description: This is the release notes page of Dynamsoft Label Recognizer for .Net SDK version 2.x.
keywords: release notes, .Net
needAutoGenerateSidebar: false
permalink: /programming/dotnet/release-notes/dotnet-2.html
---

# Release Notes - .Net 2.x

## 2.0 (08/26/2021)

### Highlights

{%- include release-notes/product-highlight-2.0.md -%}

### Changelog

#### New

- Added auto-deskew algorithm to improve the performance on recognizing the skewed characters.
- Added library `Dynamsoft.Core.dll`. Migrated the Dynamsoft core classes/enums from library `Dynamsoft.LabelRecognizer.dll` and `DynamsoftCommon.dll` to library `Dynamsoft.Core.dll`.
- Added class [`BarcodeResult`]({{site.dlr_dotnet_api}}barcode-result.html) for users to interact with Dynamsoft Barcode Reader SDK.
- Added [`DLR_RuntimeSettings`]({{site.dlr_dotnet_api}}dlr-runtime-settings.html) property [`DictionaryPath`]({{site.dlr_dotnet_api}}dlr-runtime-settings.html#dictionarypath) and [`DictionaryCorrectionThreshold`]({{site.dlr_dotnet_api}}dlr-runtime-settings.html#dictionarycorrectionthreshold) for users to further improve the recognizing accuracy by referencing dictionary files.
- Added class [`DLR_DictionaryCorrectionThreshold`]({{site.dlr_dotnet_api}}dlr-dictionary-correction-threshold.html).
- Added class [`DLR_FurtherModes`]({{site.dlr_dotnet_api}}dlr-further-modes.html) and property [`DLR_RuntimeSettings.FurtherModes`]({{site.dlr_dotnet_api}}dlr-runtime-settings.html#furthermodes) for users to config more processing modes.
- Added enumeration [`TextureDetectionMode`]({{ site.dlr_enumerations }}texture-detection-mode.html) and property [`DLR_FurtherModes.TextureDetectionModes`]({{site.dlr_dotnet_api}}dlr-further-modes.html#texturedetectionmodes) for users to detect and remove the texture background.
- Added enumeration [`ColourConversionModes`]({{ site.dlr_enumerations }}colour-conversion-mode.html) and property [`DLR_FurtherModes.ColourConversionModes`]({{site.dlr_dotnet_api}}dlr-further-modes.html#colourconversionmodes) for users to convert color images to grayscale images in differenct ways.
- Added enumeration [`BinarizationMode`]({{ site.dlr_enumerations }}binarization-mode.html) and property [`DLR_RuntimeSettings.BinarizationModes`]({{site.dlr_dotnet_api}}dlr-runtime-settings.html#binarizationmodes) for users to convert grayscale images to binary images in different ways.
- Added enumeration [`GrayscaleEnhancementMode`]({{ site.dlr_enumerations }}grayscale-enhancement-mode.html) and property [`DLR_FurtherModes.GrayscaleEnhancementModes`]({{site.dlr_dotnet_api}}dlr-further-modes.html#grayscaleenhancementmodes) for users to enable grayscale images preprocessing.  
- Added [`CharacterHConfidence`]({{site.dlr_dotnet_api}}dlr-character-result.html#characterhconfidence), [`CharacterMConfidence`]({{site.dlr_dotnet_api}}dlr-character-result.html#charactermconfidence) and [`CharacterLConfidence`]({{site.dlr_dotnet_api}}dlr-character-result.html#characterlconfidence) properties in [`DLR_CharacterResult`]({{site.dlr_dotnet_api}}dlr-character-result.html) class so that more alternative results will be available for users.

#### Improved

- Improved the neural network performance by replacing Caffe engine with OpenCV DNN engine.

#### Fixed

- Fixed a bug that might cause wrong line number matching when using [`LineSpecification.LineNumber`]({{ site.dlr_parameters_reference }}line-specification/parameter-control.html#linenumber).

#### API Changes

- Modified the `InitLicense(string)` to static [`InitLicense(string)`]({{site.dlr_dotnet_api}}label-recognizer.html#initlicense).
- Modified the parameter type of the method [`UpdateReferenceRegionFromBarcodeResults`]({{site.dlr_dotnet_api}}label-recognizer.html#updatereferenceregionfrombarcoderesults) from `TextResult[]` to `BarcodeResult[]`.
- Modified the parameters [`LabelRecognizerParameter.LetterHeightRange`]({{ site.dlr_parameters_reference }}label-recognition-parameter/parameter-control.html#letterheightrange) and [`TextArea.LetterHeightRange`]({{ site.dlr_parameters_reference }}text-area/parameter-control.html#letterheightrange). The value unit of the parameters are modified from percentage to thousandth. The available range of the value and the default value are updated as well.
- Renamed class `LabelRecognition` to [`LableRecognizer`]({{site.dlr_dotnet_api}}label-recognizer.html).
- Renamed exception `DLR_Exception` to [`LabelRecognizerException`]({{site.dlr_dotnet_api}}label-recognizer-exception.html).
- Removed method `InitLicenseFromLTS`.
- Removed method `InitLTSConnectionParameters`.
- Removed class `DMLTSConnectionParameters`.
