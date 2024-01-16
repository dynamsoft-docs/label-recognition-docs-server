---
layout: default-layout
title: Index - Dynamsoft Capture Vision C++ Edition API Reference
description: The index of Dynamsoft Capture Vision C++ edition API reference.
keywords: API reference, index, c++
needAutoGenerateSidebar: false
---

# Dynamsoft Capture Vision API Reference - C++ Edition

## DynamsoftCaptureVisionRouter

### [CCaptureVisionRouter]({{ site.dcv_cpp_api }}capture-vision-router/capture-vision-router.html)

- [`Constructor and Destructor`]({{ site.dcv_cpp_api }}capture-vision-router/instantiate.html)
- [`Single-File Processing`]({{ site.dcv_cpp_api }}capture-vision-router/single-file-processing.html)
- [`Multiple-File Processing`]({{ site.dcv_cpp_api }}capture-vision-router/multiple-file-processing.html)
- [`Settings`]({{ site.dcv_cpp_api }}capture-vision-router/settings.html)
- [`Intermediate Result`]({{ site.dcv_cpp_api }}capture-vision-router/intermediate-result.html)
- [`Auxiliary Methods`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-methods.html)

### Classes

- [`CCaptureStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`CCaptureVisionRouterModule`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`CCapturedResultFilter`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)
- [`CCapturedResultReceiver`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)
- [`CImageSourceStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)
- [`CIntermediateResultManager`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/intermediate-result-manager.html)
- [`CIntermediateResultReceiver`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html)
- [`CPresetTemplate`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/preset-template.html)

### Structs

- [`SimplifiedCaptureVisionSettings`]({{ site.dcv_cpp_api }}capture-vision-router/structs/simplified-capture-vision-settings.html)

### Enums

- [`CaptureState`]({{ site.dcv_enumerations }}capture-vision-router/capture-state.html?lang=cpp)

## DynamsoftLabelRecognizer

### Classes

- [`CCharacterResult`]({{ site.dlr_cpp_api }}character-result.html)
- [`CLabelRecognizerModule`]({{ site.dlr_cpp_api }}label-recognizer-module.html)
- [`CLocalizedTextLineElement`]({{ site.dlr_cpp_api }}localized-text-line-element.html)
- [`CLocalizedTextLinesUnit`]({{ site.dlr_cpp_api }}localized-text-lines-unit.html)
- [`CRecognizedTextLineElement`]({{ site.dlr_cpp_api }}recognized-text-line-element.html)
- [`CRecognizedTextLinesResult`]({{ site.dlr_cpp_api }}recognized-text-lines-result.html)
- [`CRecognizedTextLinesUnit`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html)
- [`CTextLineResultItem`]({{ site.dlr_cpp_api }}text-line-result-item.html)

### Structs

- [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_cpp_api }}simplified-label-recognizer-settings.html)

## DynamsoftCore

### Classes

- [`CAbstractIntermediateResultReceiver`]({{ site.dcv_cpp_api }}core/intermediate-results/abstract-intermediate-result-receiver.html)
- [`CBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/binary-image-unit.html)
- [`CCapturedResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html)
- [`CCapturedResult`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result.html)
- [`CColourImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/colour-image-unit.html)
- [`CContoursUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/contours-unit.html)
- [`CContour`]({{ site.dcv_cpp_api }}core/basic-structures/contour.html)
- [`CCoreModule`]({{ site.dcv_cpp_api }}core/basic-structures/core-module.html)
- [`CCorner`]({{ site.dcv_cpp_api }}core/basic-structures/corner.html)
- [`CEdge`]({{ site.dcv_cpp_api }}core/basic-structures/edge.html)
- [`CEnhancedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
- [`CFileImageTag`]({{ site.dcv_cpp_api }}core/basic-structures/file-image-tag.html)
- [`CGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/grayscale-image-unit.html)
- [`CImageData`]({{ site.dcv_cpp_api }}core/basic-structures/image-data.html)
- [`CImageSourceAdapter`]({{ site.dcv_cpp_api }}core/basic-structures/image-source-adapter.html)
- [`CImageSourceErrorListener`]({{ site.dcv_cpp_api }}core/basic-structures/image-source-error-listener.html)
- [`CImageTag`]({{ site.dcv_cpp_api }}core/basic-structures/image-tag.html)
- [`CIntermediateResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html)
- [`CIntermediateResult`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result.html)
- [`CLineSegmentsUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/line-segments-unit.html)
- [`CLineSegment`]({{ site.dcv_cpp_api }}core/basic-structures/line-segment.html)
- [`CObservationParameters`]({{ site.dcv_cpp_api }}core/intermediate-results/observed-parameters.html)
- [`COriginalImageResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/original-image-result-item.html)
- [`CPDFReadingParameter`]({{ site.dcv_cpp_api }}core/basic-structures/pdf-reading-parameter.html)
- [`CPoint`]({{ site.dcv_cpp_api }}core/basic-structures/point.html)
- [`CPredetectedRegionElement`]({{ site.dcv_cpp_api }}core/intermediate-results/predetected-region-element.html)
- [`CPredetectedRegionsUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/predetected-regions-unit.html)
- [`CQuadrilateral`]({{ site.dcv_cpp_api }}core/basic-structures/quadrilateral.html)
- [`CRect`]({{ site.dcv_cpp_api }}core/basic-structures/rect.html)
- [`CRegionObjectElement`]({{ site.dcv_cpp_api }}core/intermediate-results/region-object-element.html)
- [`CScaledDownColourImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
- [`CShortLinesUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/short-lines-unit.html)
- [`CTextRemovedBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/text-removed-binary-image-unit.html)
- [`CTextZone`]({{ site.dcv_cpp_api }}core/intermediate-results/text-zone.html)
- [`CTextZonesUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/text-zones-unit.html)
- [`CTextureDetectionResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-detection-result-unit.html)
- [`CTextureRemovedBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
- [`CTextureRemovedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
- [`CTransformedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/transformed-grayscale-image-unit.html)
- [`CVector4`]({{ site.dcv_cpp_api }}core/basic-structures/vector4.html)
- [`CVideoFrameTag`]({{ site.dcv_cpp_api }}core/basic-structures/video-frame-tag.html)

### Structs

- [`IntermediateResultExtraInfo`]({{ site.dcv_cpp_api }}core/structs/intermediate-result-extra-info.html)

### Enums

- [`BufferOverflowProtectionMode`]({{ site.dcv_enumerations }}core/buffer-overflow-protection-mode.html?lang=cpp)
- [`CapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=cpp)
- [`ColourChannelUsageType`]({{ site.dcv_enumerations }}core/colour-channel-usage-type.html?lang=cpp)
- [`CornerType`]({{ site.dcv_enumerations }}core/corner-type.html?lang=cpp)
- [`ErrorCode`]({{ site.dcv_enumerations }}core/error-code.html?lang=cpp)
- [`GrayscaleEnhancementMode`]({{ site.dcv_enumerations }}core/grayscale-enhancement-mode.html?lang=cpp)
- [`GrayscaleTransformationMode`]({{ site.dcv_enumerations }}core/grayscale-transformation-mode.html?lang=cpp)
- [`ImageCaptureDistanceMode`]({{ site.dcv_enumerations }}core/image-capture-distance-mode.html?lang=cpp)
- [`ImagePixelFormat`]({{ site.dcv_enumerations }}core/image-pixel-format.html?lang=cpp)
- [`ImageSourceState`]({{ site.dcv_enumerations }}core/image-source-state.html?lang=cpp)
- [`ImageTagType`]({{ site.dcv_enumerations }}core/image-tag-type.html?lang=cpp)
- [`IntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=cpp)
- [`PDFReadingMode`]({{ site.dcv_enumerations }}core/pdf-reading-mode.html?lang=cpp)
- [`RasterDataSource`]({{ site.dcv_enumerations }}core/raster-data-source.html?lang=cpp)
- [`RegionObjectElementType`]({{ site.dcv_enumerations }}core/region-object-element-type.html?lang=cpp)
- [`SectionType`]({{ site.dcv_enumerations }}core/section-type.html?lang=cpp)
- [`TargetType`]({{ site.dcv_enumerations }}core/target-type.html?lang=cpp)
- [`VideoFrameQuality`]({{ site.dcv_enumerations }}core/video-frame-quality.html?lang=cpp)

## DynamsoftUtility

- [`CDirectoryFetcher`]({{ site.dcv_cpp_api }}utility/directory-fetcher.html)
- [`CFileFetcher`]({{ site.dcv_cpp_api }}utility/file-fetcher.html)
- [`CImageManager`]({{ site.dcv_cpp_api }}utility/image-manager.html)
- [`CMultiFrameResultCrossFilter`]({{ site.dcv_cpp_api }}utility/multi-frame-result-cross-filter.html)
- [`CProactiveImageSourceAdapter`]({{ site.dcv_cpp_api }}utility/proactive-image-source-adapter.html)
- [`CUtilityModule`]({{ site.dcv_cpp_api }}utility/utility-module.html)

## DynamsoftLicense

- [`CLicenseManager`]({{ site.dcv_cpp_api }}license/license-manager.html)
- [`CLicenseModule`]({{ site.dcv_cpp_api }}license/license-module.html)

## DynamsoftImageProcessing

- [`CImageProcessingModule`]({{ site.dcv_cpp_api }}image-processing/image-processing-module.html)

