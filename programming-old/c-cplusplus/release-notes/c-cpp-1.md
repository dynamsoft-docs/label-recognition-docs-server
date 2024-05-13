---
layout: default-layout
title: C/C++ SDK Release Notes 1.x - Dynamsoft Label Recoginizer 
description: This is the release notes page of Dynamsoft Label Recoginizer for C/C++ SDK version 1.x.
keywords: release notes, c, c++
needAutoGenerateSidebar: false
permalink: /programming/c-cplusplus/release-notes/c-cpp-1.html
---

# Release Notes - C/C++ 1.x

## 1.2.1 (06/08/2021)

### New

- Added a new property [`products`]({{ site.dlr_c_cplusplus_api_reference }}structs/dm-lts-connection-parameters.html#products) to `DMLTSConnectionParameters`.
- Added a new enumeration [`Product`]({{ site.dlr_enumerations }}other-enums.html#product).

### Fixed

- Fixed a bug of license client.

## 1.2 (05/18/2021)

### New

- Added a new parameter [`LabelRecognitionParameter.Timeout`]({{ site.dlr_parameters_reference }}label-recognition-parameter/parameter-control.html#timeout). Should the recognition time pass the value of this parameter, a new error code [`DLRERR_RECOGNITION_TIMEOUT`]({{ site.dlr_enumerations }}error-code.html) will be returned.

- Added a new parameter [`LabelRecognitionParameter.Page`]({{ site.dlr_parameters_reference }}label-recognition-parameter/parameter-control.html#page) that specifies a page or a subset of pages of a single file to run the recognition process on.

- Added the following error codes: [`DLRERR_TIFF_READ_FAILED`]({{ site.dlr_enumerations }}error-code.html) , [`DLRERR_PDF_READ_FAILED`]({{ site.dlr_enumerations }}error-code.html) and [`DLRERR_PDF_DLL_MISSING`]({{ site.dlr_enumerations }}error-code.html). These error codes will be returned when the recognizer fails to read a TIFF file, a PDF file, or if the PDF DLL is missing, respectively.

- Added a new property [`pageNumber`]({{ site.dlr_c_cplusplus_structs }}dlr-result.html#pagenumber) to `DLRResult` to identify the page on which the result is located.

- Added parameters `TextStringLengthRange` and `LineStringLengthRange` that can be used to define the minimum and maximum string length when running the recognition process on a text area or a specific line, respectively. They are available as:
  - [`LabelRecognitionParameter.TextStringLengthRange`]({{ site.dlr_parameters_reference }}label-recognition-parameter/parameter-control.html#textstringlengthrange)
  - [`LabelRecognitionParameter.LineStringLengthRange`]({{ site.dlr_parameters_reference }}label-recognition-parameter/parameter-control.html#linestringlengthrange)
  - [`TextArea.TextStringLengthRange`]({{ site.dlr_parameters_reference }}text-area/parameter-control.html#textstringlengthrange)
  - [`TextArea.LineStringLengthRange`]({{ site.dlr_parameters_reference }}text-area/parameter-control.html#linestringlengthrange)
  - [`LineSpecification.LineStringLengthRange`]({{ site.dlr_parameters_reference }}line-specification/parameter-control.html#linestringlengthrange)

- Added a new parameter `MaxLineCharacterSpacing` to limit the spacing between characters treated as one line. They are available as:
  - [`LabelRecognitionParameter.MaxLineCharacterSpacing`]({{ site.dlr_parameters_reference }}label-recognition-parameter/parameter-control.html#maxlinecharacterspacing)
  - [`TextArea.MaxLineCharacterSpacing`]({{ site.dlr_parameters_reference }}text-area/parameter-control.html#maxlinecharacterspacing)

- Added parameters [`LineSpecification.FirstPoint`]({{ site.dlr_parameters_reference }}line-specification/parameter-control.html#firstpoint), [`LineSpecification.SecondPoint`]({{ site.dlr_parameters_reference }}line-specification/parameter-control.html#secondpoint), [`LineSpecification.ThirdPoint`]({{ site.dlr_parameters_reference }}line-specification/parameter-control.html#thirdpoint), and [`LineSpecification.FourthPoint`]({{ site.dlr_parameters_reference }}line-specification/parameter-control.html#fourthpoint) to specify the coordinates of a line.

- Added a new API [`AppendSettingsFromFile`]({{ site.dlr_cpp_methods }}settings.html#appendsettingsfromfile)/[`DLR_AppendSettingsFromFile`]({{ site.dlr_c_functions }}settings.html#dlr_appendsettingsfromfile) to allow appending settings directly from a JSON file.

### Improved

- Improved the recognition performance.

- Improved the regular expression parameter by supporting more [RegEx pattern syntaxes]({{ site.dlr_parameters_reference }}label-recognition-parameter/parameter-control.html#textregexpattern).

- Improved the recognition accuracy when dealing with skewed and italics characters.

- Improved the recognition accuracy for serif fonts.


## 1.0 (02/24/2021)

- Supports text recognition from BMP, JPEG, PNG and single-page TIFF files.
- Supports zonal OCR and provides three ways to localize text areas:
    - Pre-define an area manually in pixel or percentage.
    - Specify an area relative to the barcode zone, which allows you to recognize accompanying texts near the barcode. 
    - Specify an area relative to blocks which share the same colour or uses the same font colour. A common example would be a price tag, where the text of interest is always on a yellow square background, the yellow square can serve as the reference region.
- Supports specifying a regular expression to improve recognition accuracy and robustness.


## 1.0 Beta (12/10/2020)

- Supports recognition of `A-Z`, `a-z`, `0-9`, `.`, `-`, `_`, `(blank space)`, `/` and `:` characters. 