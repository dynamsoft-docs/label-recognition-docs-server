---
layout: default-layout
title: DLRRuntimeSettings - Dynamsoft Label Recognition C & C++ Struct
description: This page shows the DLRRuntimeSettings struct of Dynamsoft Label Recognition for C & C++ Language.
keywords: DLRRuntimeSettings, struct, c, c++
needAutoGenerateSidebar: true
permalink: /programming/c-cplusplus/api-reference/structs/dlr-runtime-settings.html
---


# DLRRuntimeSettings
Defines a struct to configure the text recognizer runtime settings. These settings control the text recognition process.

## Typedefs

```cpp
typedef struct tagDLRRuntimeSettings  DLRRuntimeSettings
```  
  
---
  

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`maxThreadCount`](#maxthreadcount) | *int* |
| [`characterModelName`](#charactermodelname) | *char\[64\]* |
| [`linesCount`](#linescount) | *int* |
| [`regionPredetectionModes`](#regionpredetectionmodes) | [`DLRRegionPredetectionMode`]({{ site.dlr_enumerations }}parameter-mode-enums.html#dlrregionpredetectionmode)\[8\] |
| [`referenceRegion`](#referenceregion) | [`DLRReferenceRegion`](dlr-reference-region.html) |
| [`textArea`](#textarea) | [`DLRQuadrilateral`](dlr-quadrilateral.html) |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | [`DLRGrayscaleTransformationMode`]({{ site.dlr_enumerations }}parameter-mode-enums.html#dlrgrayscaletransformationmode)\[8\] |
| [`reserved`](#reserved) | *char\[64\]* |


### maxThreadCount
Sets the number of threads the algorithm will use to recognize label.
```cpp
int tagDLRRuntimeSettings::maxThreadCount
```

**Value Range**

[1, 4]

**Default value**

4

**Remarks**

To keep a balance between speed and quality, the library concurrently runs four different threads by default.

### characterModelName
The name of the CharacterModel.
```cpp
char tagDLRRuntimeSettings::characterModelName[64]
```

### linesCount
Sets the text lines count of the text area.
```cpp
int tagDLRRuntimeSettings::linesCount
```

**Value Range**

[0, 200]

**Default value**

0

**Remarks**

0: line count is not certain.


### regionPredetectionModes
Sets the region pre-detection mode.
```cpp
DLRRegionPredetectionMode tagDLRRuntimeSettings::regionPredetectionModes[8]
```

**Value Range**

Each array item can be any one of the [`DLRRegionPredetectionMode`]({{ site.dlr_enumerations }}parameter-mode-enums.html#dlrregionpredetectionmode) Enumeration items.

**Default value**

`[DLR_RPM_SKIP,DLR_RPM_SKIP,DLR_RPM_SKIP,DLR_RPM_SKIP,DLR_RPM_SKIP,DLR_RPM_SKIP,DLR_RPM_SKIP,DLR_RPM_SKIP]`

**Remarks**

The array index represents the priority of the item. The smaller index is, the higher priority is.


### referenceRegion
Sets the reference region to search for text.
```cpp
DLRReferenceRegion tagDLRRuntimeSettings::referenceRegion
```

### textArea
Sets the text area relative to the reference region.
```cpp
DLRQuadrilateral tagDLRRuntimeSettings::textArea
```

### grayscaleTransformationModes
Sets the grayscale transformation mode.
```cpp
DLRGrayscaleTransformationMode tagDLRRuntimeSettings::grayscaleTransformationModes[8]
```

**Value Range**

Each array item can be any one of the [`DLRGrayscaleTransformationMode`]({{ site.dlr_enumerations }}parameter-mode-enums.html#dlrgrayscaletransformationmode) Enumeration items.

**Default value**

`[DLR_GTM_ORIGINAL,DLR_GTM_SKIP,DLR_GTM_SKIP,DLR_GTM_SKIP,DLR_GTM_SKIP,DLR_GTM_SKIP,DLR_GTM_SKIP,DLR_GTM_SKIP]`

**Remarks**

The array index represents the priority of the item. The smaller index is, the higher priority is.
  
### reserved
Reserved memory for struct. The length of this array indicates the size of the memory reserved for this struct.
```cpp
char tagDLRRuntimeSettings::reserved[64]
```

