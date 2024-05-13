---
layout: default-layout
title: DLR_FurtherModes Struct - Dynamsoft Label Recognizer C&C++ API Reference
description: This page shows the DLR_FurtherModes Struct of Dynamsoft Label Recognizer for C&C++ SDK.
keywords: DLR_FurtherModes, c, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/c-cplusplus/api-reference/dlr-further-modes.html
---


# DLR_FurtherModes
Stores the FurtherModes. 

```cpp
typedef struct tagDLR_FurtherModes DLR_FurtherModes
```  

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`colourConversionModes[8]`](#colourconversionmodes) | [`ColourConversionMode`]({{ site.dlr_enumerations }}colour-conversion-mode.html) |
| [`grayscaleTransformationModes[8]`](#grayscaletransformationmodes) | [`GrayscaleTransformationMode`]({{ site.dlr_enumerations }}grayscale-transformation-mode.html) |
| [`regionPredetectionModes[8]`](#regionpredetectionmodes) | [`RegionPredetectionMode`]({{ site.dlr_enumerations }}region-predetection-mode.html) |
| [`grayscaleEnhancementModes[8]`](#grayscaleenhancementmodes) | [`GrayscaleEnhancementMode`]({{ site.dlr_enumerations }}grayscale-enhancement-mode.html) | 
| [`textureDetectionModes[8]`](#texturedetectionmodes) | [`TextureDetectionMode`]({{ site.dlr_enumerations }}texture-detection-mode.html) |


&nbsp;

### colourConversionModes
Sets the mode and priority for converting a colour image to a grayscale image.

```cpp
ColourConversionMode colourConversionModes[8]
```

**Value Range**
   Each array item can be any one of the [`ColourConversionMode`]({{ site.dlr_enumerations }}colour-conversion-mode.html) Enumeration items. 
 
**Default value**
   `[CICM_GENERAL, CICM_SKIP, CICM_SKIP, CICM_SKIP, CICM_SKIP, CICM_SKIP, CICM_SKIP, CICM_SKIP]`  
 
**Remarks**
   The array index represents the priority of the item. The smaller index is, the higher priority is.  

&nbsp;

### grayscaleTransformationModes
Sets the mode and priority for the grayscale image conversion.

```cpp
GrayscaleTransformationMode grayscaleTransformationModes[8]
```

**Value Range**
   Each array item can be any one of the [`GrayscaleTransformationMode`]({{ site.dlr_enumerations }}grayscale-transformation-mode.html) Enumeration items. 
 
**Default value**
   `[GTM_ORIGINAL, GTM_SKIP, GTM_SKIP, GTM_SKIP, GTM_SKIP, GTM_SKIP, GTM_SKIP, GTM_SKIP]`  
 
**Remarks**
   The array index represents the priority of the item. The smaller index is, the higher priority is.  

&nbsp;

### regionPredetectionModes
Sets the region pre-detection mode.

```cpp
RegionPredetectionMode regionPredetectionModes[8]
```

**Value Range**
   Each array item can be any one of the [`RegionPredetectionMode`]({{ site.dlr_enumerations }}region-predetection-mode.html) Enumeration items.  
 
**Default value**
   `[RPM_GENERAL, RPM_SKIP, RPM_SKIP, RPM_SKIP, RPM_SKIP, RPM_SKIP, RPM_SKIP, RPM_SKIP]`  
 
**Remarks**
   The array index represents the priority of the item. The smaller index is, the higher priority is.

&nbsp;

### grayscaleEnhancementModes
Sets the mode and priority for grayscale image preprocessing algorithms.

```cpp
GrayscaleEnhancementMode grayscaleEnhancementModes[8]
```

**Value Range**
   Each array item can be any one of the [`GrayscaleEnhancementMode`]({{ site.dlr_enumerations }}grayscale-enhancement-mode.html) Enumeration items.  
 
**Default value**
   `[GEM_GENERAL, GEM_SKIP, GEM_SKIP, GEM_SKIP, GEM_SKIP, GEM_SKIP, GEM_SKIP, GEM_SKIP]`  
 
**Remarks**
   The array index represents the priority of the item. The smaller index is, the higher priority is.

&nbsp;

### textureDetectionModes
Sets the mode and priority for texture detection. 

```cpp
TextureDetectionMode textureDetectionModes[8]
```

**Value Range**
   Each array item can be any one of the [`TextureDetectionMode`]({{ site.dlr_enumerations }}texture-detection-mode.html) Enumeration items.  
 
**Default value**
   `[TDM_GENERAL_WIDTH_CONCENTRATION, TDM_SKIP, TDM_SKIP, TDM_SKIP, TDM_SKIP, TDM_SKIP, TDM_SKIP, TDM_SKIP]`  
 
**Remarks**
   The array index represents the priority of the item. The smaller index is, the higher priority is.
