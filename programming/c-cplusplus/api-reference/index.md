---
layout: default-layout
title: Dynamsoft Label Recognizer C++ API Reference - Main Page
description: This is the main page of Dynamsoft Label Recognizer SDK API Reference for C++ Language.
keywords: label recognition, api reference, C++
permalink: /programming/c-plusplus/api-reference/index.html
permalink: /programming/c-cplusplus/api-reference/index.html
---

# API Reference - C++

## Primary Class

- [`CCaptureVisionRouter`]({{ site.dcv_cpp_api }}capture-vision-router/capture-vision-router.html)

## Input

- [`CDirectoryFetcher`]({{ site.dcv_cpp_api }}utility/directory-fetcher.html)
- [`CImageSourceAdapter`]({{ site.dcv_cpp_api }}core/basic-structures/image-source-adapter.html)
- [`CProactiveImageSourceAdapter`]({{ site.dcv_cpp_api }}utility/proactive-image-source-adapter.html)

## Final Results

- [`CCapturedResultReceiver`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)
- [`CRecognizedTextLinesResult`]({{ site.c-cplusplus-api-reference }}recognized-text-lines-result.html)
- [`CTextLineResultItem`]({{ site.c-cplusplus-api-reference }}text-line-result-item.html)
- [`CCharacterResult`]({{ site.c-cplusplus-api-reference }}character-result.html)
- [`CCapturedResult`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result.html)
- [`CCapturedResultArray`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-array.html)
- [`CCapturedResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html)
- [`CRawImageResultItem`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/raw-image-result-item.html)

## Intermediate Results

- [`CIntermediateResultManager`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-manager.html)
- [`CIntermediateResultReceiver`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-receiver.html)
- [`CLocalizedTextLinesUnit`]({{ site.c-cplusplus-api-reference }}localized-text-lines-unit.html)
- [`CLocalizedTextLineElement`]({{ site.c-cplusplus-api-reference }}localized-text-line-element.html)
- [`CRecognizedTextLinesUnit`]({{ site.c-cplusplus-api-reference }}recognized-text-lines-unit.html)
- [`CRecognizedTextLineElement`]({{ site.c-cplusplus-api-reference }}recognized-text-line-element.html)
- [`CIntermediateResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html)
- [`CBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/binary-image-unit.html)
- [`CColourImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/colour-image-unit.html)
- [`CEnhancedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
- [`CGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/grayscale-image-unit.html)
- [`CPredetectedRegionsUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/predetected-regions-unit.html)
- [`CScaledDownColourImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
- [`CTextZonesUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/text-zones-unit.html)
- [`CTextureDetectionResultUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-detection-result-unit.html)
- [`CTextureRemovedBinaryImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
- [`CTextureRemovedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
- [`CTransformedGrayscaleImageUnit`]({{ site.dcv_cpp_api }}core/intermediate-results/transformed-grayscale-image-unit.html)
- [`CRegionObjectElement`]({{ site.dcv_cpp_api }}core/intermediate-results/region-object-element.html)
- [`CPredetectedRegionElement`]({{ site.dcv_cpp_api }}core/intermediate-results/predetected-region-element.html)

## State Listener

- [`CCaptureStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`CImageSourceStateListener`]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## [`CLicenseManager`]({{ site.dcv_cpp_api }}license/license-manager.html)

## Basic Structure

- [`CPoint`]({{ site.dcv_cpp_api }}core/basic-structures/point.html)
- [`CRect`]({{ site.dcv_cpp_api }}core/basic-structures/rect.html)
- [`CQuadrilateral`]({{ site.dcv_cpp_api }}core/basic-structures/quadrilateral.html)
- [`CImageData`]({{ site.dcv_cpp_api }}core/basic-structures/image-data.html)
- [`CImageTag`]({{ site.dcv_cpp_api }}core/basic-structures/image-tag.html)
- [`CFileImageTag`]({{ site.dcv_cpp_api }}core/basic-structures/file-image-tag.html)
- [`CPDFReadingParameter`]({{ site.dcv_cpp_api }}core/basic-structures/pdf-reading-parameter.html)

## Enumerations

- [`BufferOverflowProtectionMode`]({{ site.dcv_enumerations}}core/buffer-overflow-protection-mode.html?src=cpp&&lang=cpp)
- [`CapturedResultItemType`]({{ site.dcv_enumerations}}core/captured-result-item-type.html?src=cpp&&lang=cpp)
- [`ErrorCode`]({{ site.dcv_enumerations}}core/error-code.html?src=cpp&&lang=cpp)
- [`GrayscaleTransformationMode`]({{ site.dcv_enumerations}}core/grayscale-transformation-mode.html?src=cpp&&lang=cpp)
- [`ImageCaptureDistanceMode`]({{ site.dcv_enumerations}}core/image-capture-distance-mode.html?src=cpp&&lang=cpp)
- [`ImagePixelFormat`]({{ site.dcv_enumerations}}core/image-pixel-format.html?src=cpp&&lang=cpp)
- [`ImageSourceState`]({{ site.dcv_enumerations}}core/image-source-state.html?src=cpp&&lang=cpp)
- [`ImageTagType`]({{ site.dcv_enumerations}}core/image-tag-type.html?src=cpp&&lang=cpp)
- [`IntermediateResultUnitType`]({{ site.dcv_enumerations}}core/intermediate-result-unit-type.html?src=cpp&&lang=cpp)
- [`PDFReadingMode`]({{ site.dcv_enumerations}}core/pdf-reading-mode.html?src=cpp&&lang=cpp)
- [`RegionObjectElementType`]({{ site.dcv_enumerations}}core/region-object-element-type.html?src=cpp&&lang=cpp)
- [`SectionType`]({{ site.dcv_enumerations}}core/section-type.html?src=cpp&&lang=cpp)
- [`TargetType`]({{ site.dcv_enumerations}}core/target-type.html?src=cpp&&lang=cpp)
