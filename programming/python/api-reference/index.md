---
layout: default-layout
title: Dynamsoft Label Recognizer Python Edition API Reference - Main Page
description: This is the main page of Dynamsoft Label Recognizer SDK API Reference for Python Edition.
keywords: label recognition, api reference, python
---

# Dynamsoft Capture Vision API Reference - Python Edition

## DynamsoftCaptureVisionRouter

### [CaptureVisionRouter]({{ site.dcv_python_api }}capture-vision-router/capture-vision-router.html)

- [`Constructor`]({{ site.dcv_python_api }}capture-vision-router/instantiate.html)
- [`Single-File Processing`]({{ site.dcv_python_api }}capture-vision-router/single-file-processing.html)
- [`Multiple-File Processing`]({{ site.dcv_python_api }}capture-vision-router/multiple-file-processing.html)
- [`Settings`]({{ site.dcv_python_api }}capture-vision-router/settings.html)
- [`Buffered Items`]({{ site.dcv_python_api }}capture-vision-router/buffered-items.html)

### Classes

- [`BufferedItemsManager`]({{ site.dcv_python_api }}capture-vision-router/auxiliary-classes/buffered-items-manager.html)
- [`CaptureStateListener`]({{ site.dcv_python_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`CaptureVisionRouterModule`]({{ site.dcv_python_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`CapturedResultFilter`]({{ site.dcv_python_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)
- [`CapturedResultReceiver`]({{ site.dcv_python_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)
- [`CapturedResult`]({{ site.dcv_python_api }}capture-vision-router/auxiliary-classes/captured-result.html)
- [`ImageSourceStateListener`]({{ site.dcv_python_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)
- [`SimplifiedCaptureVisionSettings`]({{ site.dcv_python_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

### Enums

- [`EnumCaptureState`]({{ site.dcv_enumerations }}capture-vision-router/capture-state.html?lang=python)
- [`EnumImageSourceState`]({{ site.dcv_enumerations }}capture-vision-router/image-source-state.html?lang=python)
- [`EnumPresetTemplate`]({{ site.dcv_enumerations }}capture-vision-router/preset-template.html?lang=python)

## DynamsoftLabelRecognizer

### Classes

- [`BufferedCharacterItemSet`]({{ site.dlr_python_api }}buffered-character-item-set.html)
- [`BufferedCharacterItem`]({{ site.dlr_python_api }}buffered-character-item.html)
- [`CharacterCluster`]({{ site.dlr_python_api }}character-cluster.html)
- [`CharacterResult`]({{ site.dlr_python_api }}character-result.html)
- [`LabelRecognizerModule`]({{ site.dlr_python_api }}label-recognizer-module.html)
- [`RecognizedTextLinesResult`]({{ site.dlr_python_api }}recognized-text-lines-result.html)
- [`TextLineResultItem`]({{ site.dlr_python_api }}text-line-result-item.html)
- [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_python_api }}simplified-label-recognizer-settings.html)


## DynamsoftCore

### Classes

- [`CapturedResultItem`]({{ site.dcv_python_api }}core/basic-classes/captured-result-item.html)
- [`CoreModule`]({{ site.dcv_python_api }}core/basic-classes/core-module.html)
- [`FileImageTag`]({{ site.dcv_python_api }}core/basic-classes/file-image-tag.html)
- [`ImageData`]({{ site.dcv_python_api }}core/basic-classes/image-data.html)
- [`ImageSourceAdapter`]({{ site.dcv_python_api }}core/basic-classes/image-source-adapter.html)
- [`ImageSourceErrorListener`]({{ site.dcv_python_api }}core/basic-classes/image-source-error-listener.html)
- [`ImageTag`]({{ site.dcv_python_api }}core/basic-classes/image-tag.html)
- [`OriginalImageResultItem`]({{ site.dcv_python_api }}core/basic-classes/original-image-result-item.html)
- [`PDFReadingParameter`]({{ site.dcv_python_api }}core/basic-classes/pdf-reading-parameter.html)
- [`Point`]({{ site.dcv_python_api }}core/basic-classes/point.html)
- [`Quadrilateral`]({{ site.dcv_python_api }}core/basic-classes/quadrilateral.html)
- [`Rect`]({{ site.dcv_python_api }}core/basic-classes/rect.html)
- [`VideoFrameTag`]({{ site.dcv_python_api }}core/basic-classes/video-frame-tag.html)

### Enums

- [`EnumBufferOverflowProtectionMode`]({{ site.dcv_enumerations }}core/buffer-overflow-protection-mode.html?lang=python)
- [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=python)
- [`EnumColourChannelUsageType`]({{ site.dcv_enumerations }}core/colour-channel-usage-type.html?lang=python)
- [`EnumErrorCode`]({{ site.dcv_enumerations }}core/error-code.html?lang=python)
- [`EnumGrayscaleEnhancementMode`]({{ site.dcv_enumerations }}core/grayscale-enhancement-mode.html?lang=python)
- [`EnumGrayscaleTransformationMode`]({{ site.dcv_enumerations }}core/grayscale-transformation-mode.html?lang=python)
- [`EnumImageCaptureDistanceMode`]({{ site.dcv_enumerations }}core/image-capture-distance-mode.html?lang=python)
- [`EnumImagePixelFormat`]({{ site.dcv_enumerations }}core/image-pixel-format.html?lang=python)
- [`EnumImageTagType`]({{ site.dcv_enumerations }}core/image-tag-type.html?lang=python)
- [`EnumPDFReadingMode`]({{ site.dcv_enumerations }}core/pdf-reading-mode.html?lang=python)                
- [`EnumRasterDataSource`]({{ site.dcv_enumerations }}core/raster-data-source.html?lang=python)
- [`EnumVideoFrameQuality`]({{ site.dcv_enumerations }}core/video-frame-quality.html?lang=python)

## DynamsoftUtility

- [`DirectoryFetcher`]({{ site.dcv_python_api }}utility/directory-fetcher.html)
- [`FileFetcher`]({{ site.dcv_python_api }}utility/file-fetcher.html)
- [`ImageManager`]({{ site.dcv_python_api }}utility/image-manager.html)
- [`MultiFrameResultCrossFilter`]({{ site.dcv_python_api }}utility/multi-frame-result-cross-filter.html)
- [`ProactiveImageSourceAdapter`]({{ site.dcv_python_api }}utility/proactive-image-source-adapter.html)
- [`UtilityModule`]({{ site.dcv_python_api }}utility/utility-module.html)

## DynamsoftLicense

- [`LicenseManager`]({{ site.dcv_python_api }}license/license-manager.html)
- [`LicenseModule`]({{ site.dcv_python_api }}license/license-module.html)

## DynamsoftImageProcessing

- [`ImageProcessingModule`]({{ site.dcv_python_api }}image-processing/image-processing-module.html)

