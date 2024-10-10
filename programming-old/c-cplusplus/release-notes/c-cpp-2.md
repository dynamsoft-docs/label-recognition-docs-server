---
layout: default-layout
title: C/C++ SDK Release Notes 2.x - Dynamsoft Label Recoginizer 
description: This is the release notes page of Dynamsoft Label Recoginizer for C/C++ SDK version 2.x.
keywords: release notes, c, c++
needAutoGenerateSidebar: false
permalink: /programming/c-cplusplus/release-notes/c-cpp-2.html
---

# Release Notes - C/C++ 2.x

## 2.2.20 (09/29/2022)

### New

- Added new methods
  - [`DLR_InitRuntimeSettingsFromFile`](../../c/api-reference/label-recognizer-functions.html#dlrinitruntimesettingsfromfile)
  - [`DLR_InitRuntimeSettings`](../../c/api-reference/label-recognizer-functions.html#dlrinitruntimesettings)
  - [`DLR_SetCharacterModelDefaultPath`](../../c/api-reference/label-recognizer-functions.html#dlrsetcharactermodeldefaultpath)
  - [`DLR_FreeString`](../../c/api-reference/label-recognizer-functions.html#dlrfreestring)

### Renamed

- The following methods are renamed
  - Renamed `DLR_OutputSettingsToFile` to [`DLR_OutputRuntimeSettingsToFile`](../../c/api-reference/label-recognizer-functions.html#dlroutputruntimesettingstofile)
  - Renamed `DLR_OutputSettingsToString` to [`DLR_OutputRuntimeSettingsToString`](../../c/api-reference/label-recognizer-functions.html#dlroutputruntimesettings)
  - Renamed `DLR_RecognizeByBuffer` to [`DLR_RecognizeBuffer`](../../c/api-reference/label-recognizer-functions.html#dlrrecognizebuffer)
  - Renamed `DLR_RecognizeByFile` to [`DLR_RecognizeFile`](../../c/api-reference/label-recognizer-functions.html#dlrrecognizefile)

### Removed

- The following methods are removed
  - `DLR_InitLicense`. The method is replaced by [`DC_InitLicense`](../../cplusplus/api-reference/license-manager.html#initlicense) under `DynamsoftCore`.
  - `DLR_AppendSettingsFromString`
  - `DLR_AppendSettingsFromFile`
  - `DLR_ClearAppendedSettings`
  - `DLR_UpdateRuntimeSettingsFromString`

## 2.2.10 (06/21/2022)

### Changelog

- Reduced the size of MRZ model from 10MB to 2.56MB.
- Improved single-line text confidence. This enables users to implement a result confidence filter to improve the recognition accuracy.
- Improved character segmentation when processing some connected characters. This improves the recognition accuracy.

## 2.2.2 (03/03/2022)

### Changelog

#### Fixed

- Fixed a bug that might cause incorrect regular expression matching.
- Fixed a bug that might output incorrect MRZ results.

## 2.2 (11/30/2021)

### Highlights

{%- include release-notes/product-highlight-2.2.md -%}

### Changelog

#### New

- Added a new method [`DLR_UpdateRuntimeSettingsFromString`](../../c/api-reference/label-recognizer-functions.html#dlr_updateruntimesettingsfromstring)  for users to upload runtime settings from stringified JSON data.
- Added a new method [`DLR_OutputSettingsToString`](../../c/api-reference/label-recognizer-functions.html#dlr_outputsettingstostring) for users to output runtime settings to stringified JSON data.
- Added a new method [`DLR_RecognizeFileInMemory`](../../c/api-reference/label-recognizer-functions.html#dlr_recognizefileinmemory) to recognize from a file in the memory.
- Added a new method [`UpdateRuntimeSettingsFromString`](../../cplusplus/api-reference/label-recognizer.html#updateruntimesettingsfromstring) for users to upload runtime settings from stringified JSON data.
- Added a new method [`OutputSettingsToString`](../../cplusplus/api-reference/label-recognizer.html#outputsettingstostring) for users to output runtime settings to stringified JSON data.
- Added a new method [`RecognizeFileInMemory`](../../cplusplus/api-reference/label-recognizer.html#recognizefileinmemory) to recognize from a file in the memory.
- Added modes parameter `CharacterNormalizationModes` to normalize the text. The parameter is available under the following classes:
  - `LabelRecognizerParameter`
  - `TextArea`
  - `LineSpecification`

## 2.0 (08/26/2021)

### Highlights

{%- include release-notes/product-highlight-2.0.md -%}

### Changelog

#### New
- Added auto-deskew algorithm to improve the performance on recognizing the skewed characters. 
- Added header file `DynamsoftCore.h` to replace the header file `DynamsoftCommon.h`. All the core structs/enums in `DynamsoftLabelRecognizer.h` and `DynamsoftCommon.h` are migrated to the header file `DynamsoftCore.h`.
- Added struct [`BarcodeResultArray`](../api-reference/barcode-result-array.html) and [`BarcodeResult`](../api-reference/barcode-result.html) for users to interact with Dynamsoft Barcode Reader SDK.
- Added [`DLR_RuntimeSettings`](../api-reference/dlr-runtime-settings.html) property [`dictionaryPath`](../api-reference/dlr-runtime-settings.html#dictionarypath) and [`dictionaryCorrectionThreshold`](../api-reference/dlr-runtime-settings.html#dictionarycorrectionthreshold) for users to further improve the recognizing accuracy by referencing dictionary files.
- Added struct [`DLR_DictionaryCorrectionThreshold`](../api-reference/dlr-dictionary-correction-threshold.html).
- Added struct [`DLR_FurtherModes`](../api-reference/dlr-further-modes.html) and property [`DLR_RuntimeSettings.furtherModes`](../api-reference/dlr-runtime-settings.html#furthermodes) for users to config more processing modes.
- Added enumeration [`TextureDetectionMode`]({{ site.dlr_enumerations }}texture-detection-mode.html) and property [`DLR_FurtherModes.textureDetectionModes`](../api-reference/dlr-further-modes.html#texturedetectionmodes) for users to detect and remove the texture background.
- Added enumeration [`ColourConversionMode`]({{ site.dlr_enumerations }}colour-conversion-mode.html) and property [`DLR_FurtherModes.colourConversionModes`](../api-reference/dlr-further-modes.html#colourconversionmodes) for users to convert color images to grayscale images in differenct ways.
- Added enumeration [`BinarizationMode`]({{ site.dlr_enumerations }}binarization-mode.html) and property [`DLR_RuntimeSettings.binarizationModes`](../api-reference/dlr-runtime-settings.html#binarizationmodes) for users to convert grayscale images to binary images in different ways.
- Added enumeration [`GrayscaleEnhancementMode`]({{ site.dlr_enumerations }}grayscale-enhancement-mode.html) and property [`DLR_FurtherModes.grayscaleEnhancementModes`](../api-reference/dlr-further-modes.html#grayscaleenhancementmodes) for users to enable grayscale images preprocessing. 
- Added [`charaterHConfidence`](../api-reference/dlr-character-result.html#characterhconfidence), [`charaterMConfidence`](../api-reference/dlr-character-result.html#charactermconfidence) and [`charaterLConfidence`](../api-reference/dlr-character-result.html#characterlconfidence) properties in [`DLRCharacterResult`](../api-reference/dlr-character-result.html) struct so that more alternative results will be available for users.

#### Improved

- Improved the neural network performance by replacing Caffe engine with OpenCV DNN engine.

#### Fixed

- Fixed a bug that might cause wrong line number matching when using [`LineSpecification.LineNumber`]({{ site.dlr_parameters_reference }}line-specification/parameter-control.html#linenumber).

#### API Changes

- Modified the function `DLR_InitLicense(void*, const char*)` to [`DLR_InitLicense(const char*,char errorMsgBuffer[], const int errorMsgBufferLen)`](../../c/api-reference/label-recognizer-functions.html#dlr_initlicense) (C).
- Modified the method `InitLicense(const char*)` to static [`InitLicense(const char*,char errorMsgBuffer[] = NULL, const int errorMsgBufferLen = 0)`](../../cplusplus/api-reference/label-recognizer.html#initlicense) (C++).
- Modified the first parameter type of the method [`UpdateReferenceRegionFromBarcodeResults`](../../cplusplus/api-reference/label-recognizer.html#updatereferenceregionfrombarcoderesults) from `TextResultArray` to `BarcodeResultArray`.
- Modified the parameters [`LabelRecognizerParameter.LetterHeightRange`]({{ site.dlr_parameters_reference }}label-recognition-parameter/parameter-control.html#letterheightrange) and [`TextArea.LetterHeightRange`]({{ site.dlr_parameters_reference }}text-area/parameter-control.html#letterheightrange). The value unit of the parameters are modified from percentage to thousandth. The available range of the value and the default value are updated as well.
- Renamed class `CLabelRecognition` to [`CLabelRecognizer`](../../cplusplus/api-reference/label-recognizer.html).
- Renamed function `DLR_GetAllDLRResults` to [`DLR_GetAllResults`](../../c/api-reference/label-recognizer-functions.html#dlr_getallresults).
- Renamed function `DLR_FreeDLRResults` to [`DLR_FreeResults`](../../c/api-reference/label-recognizer-functions.html#dlr_freeresults).
- Renamed method `GetAllDLRResults` to [`GetAllResults`](../../cplusplus/api-reference/label-recognizer.html#getallresults).
- Renamed method `FreeDLRResults` to [`FreeResults`](../../cplusplus/api-reference/label-recognizer.html#freeresults).
- Renamed enum `DLRLocalizationSourceType` to [`LocalizationSourceType`]({{ site.dlr_enumerations }}localization-source-type.html).
- Renamed struct `DLRReferenceRegion` to [`DLR_ReferenceRegion`](../api-reference/dlr-reference-region.html).
- Renamed struct `DLRRuntimeSettings` to [`DLR_RuntimeSettings`](../api-reference/dlr-runtime-settings.html).
- Renamed struct `DLRCharacterResult` to [`DLR_CharacterResult`](../api-reference/dlr-character-result.html).
- Renamed struct `DLRLineResult` to [`DLR_LineResult`](../api-reference/dlr-line-result.html).
- Renamed struct `DLRResult` to [`DLR_Result`](../api-reference/dlr-result.html).
- Renamed struct `DLRResultArray` to [`DLR_ResultArray`](../api-reference/dlr-result-array.html).
- Removed function `DLR_InitLicenseFromLTS`.
- Removed function `DLR_InitLTSConnectionParameters`.
- Removed struct `DM_LTSConnectionParameters`.
