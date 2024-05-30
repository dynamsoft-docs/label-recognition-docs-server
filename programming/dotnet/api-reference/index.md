---
layout: default-layout
title: Dynamsoft Label Recognizer .NET API Reference - Main Page
description: This is the main page of Dynamsoft Label Recognizer SDK API Reference for .NET Language.
keywords: label recognition, api reference, .NET
---

# Dynamsoft Capture Vision API Reference - .NET Edition

## DynamsoftCaptureVisionRouter

### [CaptureVisionRouter]({{ site.dcv_dotnet_api }}capture-vision-router/capture-vision-router.html)

- [`Constructor and Destructor`]({{ site.dcv_dotnet_api }}capture-vision-router/instantiate.html)
- [`Single-File Processing`]({{ site.dcv_dotnet_api }}capture-vision-router/single-file-processing.html)
- [`Multiple-File Processing`]({{ site.dcv_dotnet_api }}capture-vision-router/multiple-file-processing.html)
- [`Settings`]({{ site.dcv_dotnet_api }}capture-vision-router/settings.html)
- [`Buffered Items`]({{ site.dcv_dotnet_api }}capture-vision-router/buffered-items.html)
- [`Auxiliary Methods`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-methods.html)

### Classes

- [`ICaptureStateListener`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`CaptureVisionRouterModule`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`CapturedResult`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result.html)
- [`CapturedResultFilter`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)
- [`CapturedResultReceiver`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)
- [`IImageSourceStateListener`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)
- [`PresetTemplate`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/preset-template.html)

### Structs

- [`SimplifiedCaptureVisionSettings`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

### Enums

- [`EnumCaptureState`]({{ site.dcv_enumerations }}capture-vision-router/capture-state.html?lang=dotnet)
- [`EnumImageSourceState`]({{ site.dcv_enumerations }}capture-vision-router/image-source-state.html?lang=dotnet)

## DynamsoftLabelRecognizer

### Classes

- [`CharacterResult`]({{ site.dlr_dotnet_api }}character-result.html)
- [`LabelRecognizerModule`]({{ site.dlr_dotnet_api }}label-recognizer-module.html)
- [`RecognizedTextLinesResult`]({{ site.dlr_dotnet_api }}recognized-text-lines-result.html)
- [`TextLineResultItem`]({{ site.dlr_dotnet_api }}text-line-result-item.html)

### Structs

- [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_dotnet_api }}simplified-label-recognizer-settings.html)

## DynamsoftCore

### Classes

- [`CapturedResultItem`]({{ site.dcv_dotnet_api }}core/basic-classes/captured-result-item.html)
- [`CoreModule`]({{ site.dcv_dotnet_api }}core/basic-classes/core-module.html)
- [`FileImageTag`]({{ site.dcv_dotnet_api }}core/basic-classes/file-image-tag.html)
- [`ImageData`]({{ site.dcv_dotnet_api }}core/basic-classes/image-data.html)
- [`ImageSourceAdapter`]({{ site.dcv_dotnet_api }}core/basic-classes/image-source-adapter.html)
- [`IImageSourceErrorListener`]({{ site.dcv_dotnet_api }}core/basic-classes/image-source-error-listener.html)
- [`ImageTag`]({{ site.dcv_dotnet_api }}core/basic-classes/image-tag.html)
- [`CLineSegment`]({{ site.dcv_dotnet_api }}core/basic-classes/line-segment.html)
- [`OriginalImageResultItem`]({{ site.dcv_dotnet_api }}core/basic-classes/original-image-result-item.html)
- [`PDFReadingParameter`]({{ site.dcv_dotnet_api }}core/basic-classes/pdf-reading-parameter.html)
- [`Point`]({{ site.dcv_dotnet_api }}core/basic-classes/point.html)
- [`Quadrilateral`]({{ site.dcv_dotnet_api }}core/basic-classes/quadrilateral.html)
- [`Rect`]({{ site.dcv_dotnet_api }}core/basic-classes/rect.html)
- [`VideoFrameTag`]({{ site.dcv_dotnet_api }}core/basic-classes/video-frame-tag.html)

### Structs


### Enums

- [`EnumBufferOverflowProtectionMode`]({{ site.dcv_enumerations }}core/buffer-overflow-protection-mode.html?lang=dotnet)
- [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=dotnet)
- [`EnumColourChannelUsageType`]({{ site.dcv_enumerations }}core/colour-channel-usage-type.html?lang=dotnet)
- [`EnumErrorCode`]({{ site.dcv_enumerations }}core/error-code.html?lang=dotnet)
- [`EnumGrayscaleEnhancementMode`]({{ site.dcv_enumerations }}core/grayscale-enhancement-mode.html?lang=dotnet)
- [`EnumGrayscaleTransformationMode`]({{ site.dcv_enumerations }}core/grayscale-transformation-mode.html?lang=dotnet)
- [`EnumImageCaptureDistanceMode`]({{ site.dcv_enumerations }}core/image-capture-distance-mode.html?lang=dotnet)
- [`EnumImagePixelFormat`]({{ site.dcv_enumerations }}core/image-pixel-format.html?lang=dotnet)
- [`EnumImageTagType`]({{ site.dcv_enumerations }}core/image-tag-type.html?lang=dotnet)
- [`EnumPDFReadingMode`]({{ site.dcv_enumerations }}core/pdf-reading-mode.html?lang=dotnet)
- [`EnumRasterDataSource`]({{ site.dcv_enumerations }}core/raster-data-source.html?lang=dotnet)
- [`EnumVideoFrameQuality`]({{ site.dcv_enumerations }}core/video-frame-quality.html?lang=dotnet)

## DynamsoftUtility

- [`DirectoryFetcher`]({{ site.dcv_dotnet_api }}utility/directory-fetcher.html)
- [`FileFetcher`]({{ site.dcv_dotnet_api }}utility/file-fetcher.html)
- [`ImageManager`]({{ site.dcv_dotnet_api }}utility/image-manager.html)
- [`MultiFrameResultCrossFilter`]({{ site.dcv_dotnet_api }}utility/multi-frame-result-cross-filter.html)
- [`ProactiveImageSourceAdapter`]({{ site.dcv_dotnet_api }}utility/proactive-image-source-adapter.html)
- [`UtilityModule`]({{ site.dcv_dotnet_api }}utility/utility-module.html)

## DynamsoftLicense

- [`LicenseManager`]({{ site.dcv_dotnet_api }}license/license-manager.html)
- [`LicenseModule`]({{ site.dcv_dotnet_api }}license/license-module.html)

## DynamsoftImageProcessing

- [`ImageProcessingModule`]({{ site.dcv_dotnet_api }}image-processing/image-processing-module.html)

