---
layout: default-layout
title: DLR_LineSpecification Struct - Dynamsoft Label Recognizer .NET API Reference
description: This page shows the DLR_LineSpecification Struct of Dynamsoft Label Recognizer for .NET SDK.
keywords: DLR_LineSpecification, .Net
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/dotnet/api-reference/dlr-line-specification.html
---


# DLR_LineSpecification
Stores the settings of text line.

```csharp
class Dynamsoft.DLR.DLR_LineSpecification
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`GrayscaleEnhancementModes`](#grayscaleenhancementmodes) | [`EnumGrayscaleEnhancementMode`]({{ site.dlr_enumerations }}grayscale-enhancement-mode.html)[] | 
| [`BinarizationModes`](#binarizationmodes) | [`EnumBinarizationMode`]({{ site.dlr_enumerations }}binarization-mode.html)[ ] |


&nbsp;

### GrayscaleEnhancementModes
Sets the mode and priority for grayscale image preprocessing algorithms.

```csharp
EnumGrayscaleEnhancementMode[] GrayscaleEnhancementModes
```

**Value Range**
   Each array item can be any one of the [`EnumGrayscaleEnhancementMode`]({{ site.dlr_enumerations }}grayscale-enhancement-mode.html) Enumeration items.  
 
**Default value**
   `[EnumGrayscaleEnhancementMode.GEM_GENERAL, EnumGrayscaleEnhancementMode.GEM_SKIP, EnumGrayscaleEnhancementMode.GEM_SKIP, EnumGrayscaleEnhancementMode.GEM_SKIP, EnumGrayscaleEnhancementMode.GEM_SKIP, EnumGrayscaleEnhancementMode.GEM_SKIP, EnumGrayscaleEnhancementMode.GEM_SKIP, EnumGrayscaleEnhancementMode.GEM_SKIP]`  
 
**Remarks**
   The array index represents the priority of the item. The smaller index is, the higher priority is.



&nbsp;

### BinarizationModes
Sets the mode and priority for binarization.

```csharp
EnumBinarizationMode[] BinarizationModes
```

**Value Range**

Each array item can be any one of the [`EnumBinarizationMode`]({{ site.dlr_enumerations }}binarization-mode.html) Enumeration items.

**Default value**

`[EnumBinarizationMode.BM_LOCAL_BLOCK, EnumBinarizationMode.BM_SKIP, EnumBinarizationMode.BM_SKIP, EnumBinarizationMode.BM_SKIP, EnumBinarizationMode.BM_SKIP, EnumBinarizationMode.BM_SKIP, EnumBinarizationMode.BM_SKIP, EnumBinarizationMode.BM_SKIP]`

**Remarks**

The array index represents the priority of the item. The smaller index is, the higher priority is.