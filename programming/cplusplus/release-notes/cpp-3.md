---
layout: default-layout
title: C/C++ SDK Release Notes 3.x - Dynamsoft Label Recoginizer 
description: This is the release notes page of Dynamsoft Label Recoginizer for C/C++ SDK version 3.x.
keywords: release notes, c++
needAutoGenerateSidebar: false
---

# Release Notes - C++ 3.x

## 3.4.10 (07/23/2024)

<!-- Added internal logic for usage count. -->
### New

- Added a new parameter CharSet to the [`CharacterModel`]({{ site.dcv_parameters }}character-model/) object to include or exclude characters for recognition.
- Added a new algorithm stage `IRUT_RAW_TEXT_LINES`. Corresponding APIs are added to obtain the intermediate result of this stage.
  - Class [`CRawTextLinesUnit`]({{ site.dlr_cpp_api }}raw-text-lines-unit.html)
  - Class [`CRawTextLine`]({{ site.dlr_cpp_api }}raw-text-line.html)
  - Enumeration [`RawTextLineStatus`]({{ site.dlr_cpp_api }}raw-text-line-status.html)
- Added the following intermediate result altering functions to the class [`CRecognizedTextLinesUnit`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html).
  - Added function [`RemoveRecognizedTextLine`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html#removerecognizedtextLine)
  - Added function [`AddRecognizedTextLine`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html#addrecognizedtextline)
  - Added function [`SetRecognizedTextLine(index,element,matrixToOriginalImage)`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html#setrecognizedtextlineindexelementmatrixtooriginalimage)
- Added a new function [`CreateRawTextLine`]({{ site.dlr_cpp_api }}raw-text-lines-unit.html#createRawTextLine) to the class [`CLabelRecognizerModule`]({{ site.dlr_cpp_api }}label-recognizer-module.html).
- Added a new function [`GetRawText`]({{ site.dlr_cpp_api }}text-line-result-item.html#getrawtext) to the class [`CRecognizedTextLineELement`]({{ site.dlr_cpp_api }}recognized-text-line-element.html).
- Added a new function [`GetRawText`]({{ site.dlr_cpp_api }}text-line-result-item.html#getrawtext) to the class [`CTextLineResultItem`]({{ site.dlr_cpp_api }}text-line-result-item.html).
- Added a new function [`AddItem`]({{ site.dlr_cpp_api }}recognized-text-lines-result.html#additem) to the class [`CRecognizedTextLinesResult`]({{ site.dlr_cpp_api }}recognized-text-lines-result.html).
- Added a new function [`SetLocation`]({{ site.dlr_cpp_api }}text-line-result-item.html#setlocation) to the class [`CTextLineResultItem`]({{ site.dlr_cpp_api }}text-line-result-item.html).
- Added a new enumeration member `IRUT_RAW_TEXT_LINES` to the [`IntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=cpp).
- Added a new function [`Clone`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html#clone) to the class [`CCapturedResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html).
- Added a new callback function [`OnRawTextLinesReceived`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html#onrawtextlinesreceived) to the class [`CIntermediateResultReceiver`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html).
- Added a new function [`AddItem`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html#additem) to the class [`CCapturedResult`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html).
- Updated the function [`StopCapturing`]({{ site.dcv_cpp_api }}capture-vision-router/multiple-file-processing.html#stopcapturing). Changed the default value of parameter `waitForRemaingTasks` from `false` to `true`.
- Add a new charge way, `TimeSliceCount`.

### Changed

- Changed the maximum length of the `DeviceFriendlyName` to 255. If the length exceeds 255, it will be truncated.
- Changed the default value of the `waitForThreadExit` parameter to `true` for the [`StopCapturing`]({{ site.dcv_cpp_api }}capture-vision-router/multiple-file-processing.html#stopcapturing) method.

### Fixed

- Fixed a bug where `CaptureVisionRouter.StartCapturing` would erroneously halt the fetching process when its status was running, leading to an unnecessary stop and restart of the fetching operation.
- Fixed a bug where `CDirectoryFetcher` would prematurely read an image before verifying if the buffer was full, resulting in potential loss of the image that did not make it into the buffer upon calling `StopFetching`.

### Deprecated

- Deprecated function [`SetRecognizedTextLine(element,matrixToOriginalImage)`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html#setrecognizedtextlineelementmatrixtooriginalimage) of the class [`CRecognizedTextLinesUnit`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html).

## 3.2.30 (05/13/2024)

### Fixed

- Fixed a bug where the DynamsoftNeuralNetwork module failed to load due to a path error.
- Fixed a bug where users would not receive proper error messages when attempting to configure [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_cpp_api }}simplified-label-recognizer-settings.html) with an incorrect `CharacterModel`.
- Fixed a bug where the characters might not be correctly excluded when they are configured in the filter file.

## 3.2.20 (04/07/2024)

### Highlights

- Added confusable character distinguishing: this feature enhances the library's ability to distinguish between common confusable character sets including {0, o, O}, {1, I, l}, and {5, s, S}, across popular fonts like Arial, Times New Roman, and Verdana, etc.
- Supported confusable character set customization: leveraging the new caching mechanism in the `CaptureVisionRouter (CVR)` module, the library now enables users to customize confusable character sets to meet the needs of specific scenarios.

### Changelogs

#### Improved

- Improved the speed of `TextLineGroup` detection by optimizing internal logic.

#### New

- Added new APIs for users to obtain the cached character items and the character clusters:
  - A new class [`CBufferedCharacterItemSet`]({{ site.dlr_cpp_api }}buffered-character-item-set.html) to represent a collection of buffered character items and cluster information.
  - A new class [`CBufferedCharacterItem`]({{ site.dlr_cpp_api }}buffered-character-item.html) to represent a basic item of the buffered characters with its image and features information.
  - A new class [`CCharacterCluster`]({{ site.dlr_cpp_api }}character-cluster.html) to represent a character cluster generated from the collected buffered character items.
  - Added a new class [`CBufferedItemsManager`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/buffered-items-manager.html) to manage the buffered character items.
  - Added a new method [`GetBufferedItemsManger`]({{ site.dcv_cpp_api }}capture-vision-router/buffered-items.html#getbuffereditemsmanager) to get an object of `CBufferedItemsManager`.
- Added new [`LabelRecognizerTaskSettings`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/index.html) parameters.
  - Added [`ConfusableCharactersPath`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/confusable-characters-path.html) to define the path of the resource files that store the confusable characters' information.
  - Added [`ClusterSamplesCountThreshold`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/cluster-samples-count-threshold.html) to specify the lowest required sample count for clustering.
- Added new [`TextLineSpecification`]({{ site.dcv_parameters_reference }}text-line-specification/index.html) parameters.
  - Added [`ConfusableCharactersCorrection`]({{ site.dcv_parameters_reference }}text-line-specification/confusable-characters-correction.html) to define which confusable characters you are going to distinguish. You can also specify the font type of the characters.
  - Added [`ExpectedGroupCount`]({{ site.dcv_parameters_reference }}text-line-specification/expected-groups-count.html) to define the count of `TextLineGroups` that might exist on the image.
- Added a new method [`GetSpecificationName`]({{ site.dlr_cpp_api }}text-line-result-item.html) to the `CTextLineResultItem` class to get the name of the `TextLineSpecification`object that generated this `CTextLineResultItem`.
- Added a new method [`GetSpecificationName`]({{ site.dlr_cpp_api }}recognized-text-line-element.html) to the `CRecognizedTextLineElement` class to get the name of the `TextLineSpecification`object that generated this `CRecognizedTextLineElement`.
- Added a new error code [`EC_PDF_LIBRARY_LOAD_FAILED`]({{ site.dcv_enumerations }}core/error-code.html?lang=cpp).

## 3.2.10 (03/01/2024)

### Improved

- Security update for `DynamsoftLabelRecognizer` library and other corresponding libraries.
- Supported multiple instances of the class [`CCaptureVisionRouter`]({{ site.dcv_cpp_api }}capture-vision-router/capture-vision-router.html).
- Supported the filter configuration of the characters that are not recognized by the Deep Neural Network via the `Filter.txt` file.
- Improved the usage count logic of the concurrent license mode.
- Improved the experience of local cache usage when failing to connect the license server. The renewal of the local cache is optimized as well.

### New

- Added new error codes:
  - `EC_RESULT_TYPE_MISMATCH_IRREPLACEABLE`
  - `EC_LICENSE_CACHE_USED`
- Added a virtual destructor to the interface [`CImageSourceErrorListener`]({{ site.dcv_cpp_api }}core/basic-structures/image-source-error-listener.html) to prevent memory leaks.
- Added a new function [`GetRecognizedTextLinesResult`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html#getrecognizedtextlinesresult) to the `CCapturedResult` class to get all the result items with the type `CRIT_TEXT_LINE`.
- Added new virtual destructors to the following interfaces to prevent memory leaks.
  - [`CCaptureStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
  - [`CImageSourceStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

### Changed

- Changed the internal logic of the function [`SetResultUnitTypesOnlyForInput`]({{ site.dcv_cpp_api }}core/intermediate-results/observed-parameters.html#setresultunittypesonlyforinput) of `ObservationParameters`. The function only takes effect when the callback of the specified result unit is implemented.

### Fixed

- Fixed a crash bug of the Replace method of the [`IntermediateResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) class. The method will return the error code `EC_RESULT_TYPE_MISMATCH_IRREPLACEABLE` when the result type is mismatched.
- Fixed a bug where error messages are not output when parsing the parameter templates.
- Fixed a bug where multiple results were output from the same text area.
- Fixed a bug where the capture might be blocked due to the network latency.
- Fixed a bug where the `DetectAndNormalizeDocument` task might be approved without a valid license.
- Fixed the bugs of usage count.
  - Count twice for a single PDF417 barcode when a code parser task is implemented on the result.
  - The barcode decoding result might not be uploaded timely.
  - The usage count of text line recognition might be double counted when the intermediate results are output.
  - The document boundary detection result might be miscounted.
  - Patchcode might be counted even if there is no Patchcode license item.

## 3.2.0 (01/16/2024)

### Highlights

- Introduced the capability for users to influence the image processing process by altering intermediate results. Users can now clone, edit, and substitute intermediate result units within the callback function of each type. Subsequent operations will then proceed based on the updated unit.
- Introduced a feature for multi-condition filtering across products. Users can now specify filtering criteria for the task results of a `TargetROIDef` by implementing an `OutputTaskSetting` based on the task results of varying products from descendant `TargetROIDef` objects.
- Enhanced the `Offset` parameter in `TargetROIDef`. Users now have the capability to meticulously customize components of the coordinate system, including the origin, X-axis, and Y-axis, for precise offset calculation.
- Introduced a feature for grouping text lines. A text line group consists of spatially adjacent lines of text. Through the `TextLineSpecification` parameters, users can now do two things:
  - Put text lines in groups and also define the spatial relationship between different groups;
  - Specify whether to concatenate text line results within a group, how to do the concatenation and whether to output the concatenated result.

### Changelogs

#### New

- Updated the template system
  - Added `StringLengthRange` for TextDetectionMode.
  - Added `ReferenceTaskNameArray` under `Location.ReferenceObjectFilter` to filter the reference objects generated by the task name.
  - Added the support of the `OutputTaskSetting` definition. The following subparameters are available in `OutputTaskSetting` object:
    - `OutputCondition`
    - `TaskResultArray`
    - `TargetROIDefName`
    - `TaskSettingNameArray`
    - `BackwardReferenceOutput`
    - `ReferenceTaskNameArray`
    - `ReferenceResultTypeArray`
    - `Operator`
  - Updated `TextLineSpecification` to support text line group definition. Added the following subparameters:
    - `OutputResults`
    - `ConcatResults`
    - `ConcatSeparator`
    - `ConcatStringLengthRange`
    - `ConcatStringRegExPattern`
    - `ReferenceGroupName`
    - `TextLinesCount`
    - `SubGroups`
  - Offset parameter is optimized.
    - Added `ReferenceObjectType` to specify whether the reference object is an atomic object or the whole image.
    - Added `ReferenceXAxis` & `ReferenceYAxis` to define the X & Y axis.
    - Modified `FirstPoint`, `SecondPoint`, `ThirdPoint` & `FourthPoint`. You can specify whether the X or Y coordinate of the point is measured by percentage.
    - Deprecated `ReferenceObjectSize` Type.
- The following classes are migrated from `DynamsoftCore` module to the `DynamsoftCaptureVisionRouter` module:
  - `CIntermediateResultReceiver`
  - `CapturedResultReceiver`
  - `CapturedResultFilter`
  - `CIntermediateResultManager`
- Added a new class back method `OnShortLinesUnitReceived` to the `CIntermediateResultReceiver` class.
- Added a new class `CAbstractIntermediateResultReceiver`. It is the super class of the `CIntermediateResultReceiver`.
- Added methods `PauseCapturing` and `ResumeCapturing`. Two new `CapturedState` members, `CS_PAUSED` and `CS_RESUMED`, are added as well.
- Added a new property `documentSettings` to struct `SimplifiedCaptureVisionSettings`. The corresponding struct `SimplifiedDocumentNormalizerSettings` is added to the `DynamsoftDocumentNormalizer` module to store the `documentSettings`.
- Added the following methods to the `CObservationParameters` class to specify the `input only` result unit.
  - `SetResultUnitTypesOnlyForInput`
  - `GetResultUnitTypesOnlyForInput`
  - `IsResultUnitTypeOnlyForInput`
- Added the following methods to the `CRegionObjectElement` class to support the intermediate result modification.
  - `SetLocation`
  - `Clone`
  - `Retain`
  - `Release`
- Added a new method `Replace` to the `CIntermediateResultUnit` class to support the replacement of intermediate result units.
- Added `SetImageData` methods to the following classes:
  - `CCapturedResult`
  - `CCapturedResultItem`
  - `CRegionObjectElement`
  - `CIntermediateResultUnit`
  - `CLocalizedTextLineElement`
  - `CLocalizedTextLinesUnit`
  - `CRecognizedTextLineElement`
  - `CRecognizedTextLinesUnit`
  - `CRecognizedTextLinesResult`
- Added new methods to the `CPredetectedRegionsUnit` class to add, remove or set the predetected regions.
- Added new methods to the `CLineSegmentsUnit` class to add, remove or set the line segments.
- Added new methods to the `CTextZonesUnit` class to add, remove or set the text zones. Added a new class `CTextZone` to store the information of a single text zone.
- Added a new method `SetContours` to the `CContourUnit` class.
- Added new methods to the `CTextureDetectionResultUnit` class to set the X & Y spacing.
- Added a new intermediate result unit, `CShortLinesUnit`, to output the detected short lines. The corresponding enumeration member `IRUT_SHORT_LINES` is added to the `IntermediateResultUnitType`.
- Added the following methods to the `CCapturedResultItem` class
  - `GetTargetROIDefName`
  - `GetTaskName`
  - `Retain`
  - `Release`
- Added the following new error codes
  - `EC_IMAGE_SIZE_NOT_MATCH`
  - `EC_IMAGE_PIXEL_FORMAT_NOT_MATCH`
  - `EC_SECTION_LEVEL_RESULT_IRREPLACEABLE`
  - `EC_AXIS_DEFINITION_INCORRECT`
  - `EC_TEXT_LINE_GROUP_LAYOUT_CONFLICT`
  - `EC_TEXT_LINE_GROUP_REGEX_CONFLICT`
- Added the following methods to the `CCapturedResult` class.
  - A new override constructor.
  - `Retain`
  - `Release`
- Updated `CImageData` class
  - Change the return value of `GetBytesLength` from int to unsigned long long.
  - Added a new constructor.
- Added a new supported image pixel format, binary 8 inverted. The corresponding enumeration member is added to the `ImagePixelFormat`.
- Added return value for the `Retain` method of the `CIntermediateResultUnit` class. The method will return the pointer of the current `CIntermediateResultUnit`.
- Added a new method `CreatePredetectedRegionElement` to the `CImageProcessingModule` class to create the predetected region element.
- Added new methods to the `CLocalizedTextLinesUnit` class to add, set or remove the localized text line elements.
- Added new methods to the `CRecognizedTextLinesUnit` class to add, set or remove the recognized text line elements.
- Added the following methods to the `CRecognizedTextLineElement` class
  - A new constructor (the old one is removed)
  - `SetText`
- Added a new constructor to the `CTextLineResultItem` class to replace the previous one.
- Added the following methods to the `CrecognizedTextLinesResult` class.
  - A new constructor
  - `Retain`
  - `Release`
- Added the following methods to the `CLabelRecognizerModule` class to create the corresponding elements.
  - `CreateRecognizedTextLineElement`
  - `CreateLocalizedTextLineElement`

#### Fixed

- Fixed a crash bug that might happen when triggering the `SetNextImageToReturn` method of the `ImageSourceAdapter` class.

#### Break Changes

- Changed the logic of the `StopCapturing` method.
  - `CaptureResultReceiver` will not receive results after `StopCapturing` is triggered with `waitForRemainingTasks` false.
  - Support stop capturing after the `PauseCapturing` method is triggered.
- Changed the logic of the `capturedResultItemTypes` setting of `SimplifiedCaptureVisionSettings`:
  - If the result item types don't match the specified template, the method `UpdateSettings` will return the error code `EC_PARAMETER_VALUE_INVALID` with the message "The captured result item types do not match the task configurations in the template".
  - Based on the `capturedResultItemTypes` setting, the irrelevant tasks will be removed from the template.
  - The `capturedResultItemTypes` should include at least one of the `CRIT_BARCODE`, `CRIT_TEXT_LINE`, `CRIT_DETECTED_QUAD`, `CRIT_NORMALIZED_IMAGE`. Otherwise, the method `UpdateSettings` will return the error code `EC_PARAMETER_VALUE_INVALID` with the message " The captured result item types should contain at least one task result type ".
- Refactored the `CContour` class. Please view API reference - `CContour` class for more information.
- The destructor functions of the following classes are changed to protected:
  - `CCandidateQuadEdgesUnit`
  - `CCornersUnit`
  - `CDetectedQuadElement`
  - `CDetectedQuadsUnit`
  - `CLongLinesUnit`
  - `CNormalizedImageElement`
  - `CNormalizedImageUnit`
  - `CNormalizedImagesResult`
  - `CDetectedQuadsResult`
- Change the compiler option of the runtime library of Windows DLLs from MD to MT.
- The `DeepNeuralNetwork` module is separated from the `DynamsoftImageProcessing` module.

## 3.0.30 (02/01/2024)

### New

- Added internal logic to obtain resources based on the specified template.

### Fixed

- Small fixes and tweaks in the license module.

## 3.0.20 (10/26/2023)

### New

- Added the following preset templates:
  - PT_READ_BARCODES_SPEED_FIRST
  - PT_READ_BARCODES_READ_RATE_FIRST
  - PT_READ_BARCODES_BALANCED
  - PT_READ_SINGLE_BARCODE
  - PT_READ_DENSE_BARCODES
  - PT_READ_DISTANT__BARCODES
  - PT_RECOGNIZE_NUMBERS
  - PT_RECOGNIZE_LETTERS
  - PT_RECOGNIZE_NUMBERS_AND_LETTERS
  - PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS
  - PT_RECOGNIZE_UPPERCASE_LETTERS
- Added parameter `Page` to `ImageSource` object.
- Added a new method `SetPages` to the class `CDirectoryFetcher` and class `CFileFetcher`.
- Added a new parameter `scaleDownThreshold` to the struct `SimplifiedLabelRecognizerSettings`.
- Added `CImageSourceErrorListener` to receive the errors from an image source. 
- Added method `SetErrorListener` to class `CImageSourceAdapter` to add the `CImageSourceErrorListener`.
- Added a new parameter `minImageCaptureInterval` which can be set via the struct `SimplifiedCaptureVisionSettings` or the `CaptureVisionTemplate` object of a JSON template file.
- Added "UNKNOWN" as a supported value of the `TextDetectionMode.Direction` parameter. Changed the default value of `Direction` to "UNKNOWN".
- Added the following error codes:
  - EC_FILE_ALREADY_EXISTS
  - EC_CREATE_FILE_FAILED
  - EC_IMGAE_DATA_INVALID

### Improved

- The class `CDirectoryFetcher` and `CFileFetcher` will be able to return error codes via `CImageSourceErrorListener`
- Updated the error codes of the method `SaveToFile` of the class `CImageManager`.
- Optimize the logic to support calling `CIntermediateResultManager.AddResultReceiver` and  `CIntermediateResultManager.RemoveResultReceiver` after StartCapturing.
- Added ability to output all templates via methods `OutputSettings` and `OutputSettingsToFile` by specifying "*" for the parameter `templateName`.

### Fixed

- Small fixes and tweaks.

### Changed

- Changed the upper limit to the `DuplicateForgetTime`, which is 3 minutes.
- Changed the timing of `OnOriginalImageResultReceived` so that it is triggered immediately after receiving the image.
- Changed the constructors of the following classes from public to protected.
  - CImageTag
  - CCapturedResultReceiver
  - CCapturedResultFilter
  - CImageSourceAdapter
  - CProactiveImageSourceAdapter
  - CIntermediateResultUnit
  - CIntermediateResultReceiver
- Remove const modifiers of all callback methods of class `CCapturedResultReceiver` and class `CIntermediateResultReceiver`.

## 3.0.10 (08/08/2023)

### New

- Added a new class `CVector4` in the core module.

- Added new methods `SetTransformMatrix` and `GetTransformMatrix` to the class `CIntermediateResultUnit`. Enumeration `TransformMatrixType` is also added to support users specifying the type of the target matrix.

- Added enumeration `RasterDataSource` to specify the raster data source when reading PDF files. The previous enumeration `TargetType` is removed. The attribute `TargetType type` of Class `CPDFReadingParameter` is replaced by `RasterDataSource rasterDataSource`.  

- Added method `GetContours` to the `CContourUnit` class to get all the `CContour` objects contained in the unit and their hierarchies.

### Improved

- Improved the implementation of the `StopCapturing` method to prevent deadlock when invoked in the management thread.

### Fixed

- Fixed crash bugs that happen in rare cases.

- Fixed a bug where the local license is not successfully updated when initialing the license again.

### Changed

- Changed the parameters and the return value of the method `GetLineSegment` of CLineSegmentsUnit class. The method will require an `index` value as the parameter and return a `CLineSegment` object as the return value.

- Changed the structure of class `CPoint`.

- Renamed method `GetRawImage` to `GetOriginalImage`.

- Renamed method `GetSourceImageHashId` to `GetOriginalImageHashId`. This change applies to the following classes:

  - `CIntermediateResultUnit`

  - `CCapturedResult`

  - `CRecognizedTextLinesResult`

- Renamed method `GetSourceImageTag` to `GetOriginalImageTag`. This change applies to the following classes:

  - `CIntermediateResultUnit`

  - `CCapturedResult`

  - `CRecognizedTextLinesResult`

- Renamed methods `GetCount` to `GetItemsCount`. This change applies to the following classes:

  - `CCapturedResult`

  - `CRecognizedTextLinesResult`

- Renamed an enumeration member of `CapturedResultItemType` from `CRIT_RAW_IMAGE` to `CRIT_ORIGINAL_IMAGE`.

- Renamed a method of `CapturedResultReceiver` from `OnRawImageResultReceived` to `OnOriginalImageResultReceived`.

- Renamed a method of `CapturedResultFilter` from `OnRawImageResultReceived` to `OnOriginalImageResultReceived`.

- Renamed the class `CRawImageResultItem` to `COriginalImageResultItem`.

- Renamed an enumeration member of `BufferOverflowProtectionMode` from `BOPM_APPEND` to `BOPM_UPDATE`.

- The following methods are renamed:

  - Renamed `EnableResultVerification` to `EnableResultCrossVerification`.

  - Renamed `isResultVerificationEnable` to `isResultCrossVerificationEnabled`.

  - Renamed `EnableDuplicateFilter` to `EnableResultDeduplication`.

  - Renamed `isDuplicateFilterEnabled` to `isResultDeduplicationEnabled`.

- Renamed parameter `CornerAngleRangeArray` to `CornerAngleRange`. The range of the sub parameter `MinValue` is restricted to [0,90] and the range of `MaxValue` is restricted to [90,180].

### Removed

- Removed `Set/GetLocalToSourceImageTransformMatrix` methods from `CIntermediateResultUnit` class.

- Removed `Set/GetRotationTransformMatrix` methods from `CIntermediateResultUnit` class.

- Removed methods `GetCount` and `GetContour` from CContourUnit class. Use the method `GetContours` instead.

## 3.0.0 (07/04/2023)

{%- include release-notes/product-highlight-3.0.0.md -%}

