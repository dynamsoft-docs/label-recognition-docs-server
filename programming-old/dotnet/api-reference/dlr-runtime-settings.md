---
layout: default-layout
title: DLR_RuntimeSettings - Dynamsoft Label Recognizer .Net Class
description: This page shows the DLR_RuntimeSettings struct of Dynamsoft Label Recognizer for .Net Language.
keywords: DLR_RuntimeSettings, struct, .Net
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/dotnet/api-reference/dlr-runtime-settings.html
---


# DLR_RuntimeSettings
Defines a struct to configure the text recognizer runtime settings. These settings control the text recognition process.
  
```csharp
class Dynamsoft.DLR.DLR_RuntimeSettings
```   

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`MaxThreadCount`](#maxthreadcount) | *int* |
| [`CharacterModelName`](#charactermodelname) | *string* |
| [`ReferenceRegion`](#referenceregion) | [`DLR_ReferenceRegion`](dlr-reference-region.html) |
| [`TextArea`](#textarea) | [`Quadrilateral`](quadrilateral.html) |
| [`DictionaryPath`](#dictionarypath) | *string* |
| [`DictionaryCorrectionThreshold`](#dictionarycorrectionthreshold) | [`DLR_DictionaryCorrectionThreshold`](dlr-dictionary-correction-threshold.html) |
| [`BinarizationModes`](#binarizationmodes) | [`EnumBinarizationMode`]({{ site.dlr_enumerations }}binarization-mode.html)[ ] |
| [`FurtherModes`](#furthermodes) | [`DLR_FurtherModes`](dlr-further-modes.html)|


&nbsp;

### MaxThreadCount
Sets the number of threads the algorithm will use to recognize label.
```csharp
int MaxThreadCount
```

**Value Range**

[1, 4]

**Default value**

4

**Remarks**

To keep a balance between speed and quality, the library concurrently runs four different threads by default.

&nbsp;

### CharacterModelName
The name of the CharacterModel.

```csharp
string CharacterModelName
```


&nbsp;

### ReferenceRegion
Sets the reference region to search for text.
```csharp
DLR_ReferenceRegion ReferenceRegion
```

&nbsp;

### TextArea
Sets the text area relative to the reference region.
```csharp
Quadrilateral TextArea
```

&nbsp;

### DictionaryPath
Sets the path of the dictionary file.
```csharp
string DictionaryPath
```

&nbsp;

### DictionaryCorrectionThreshold
Sets the threshold of dictionary error correction.
```csharp
DLR_DictionaryCorrectionThreshold DictionaryCorrectionThreshold
```

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


&nbsp;

### FurtherModes
Sets further modes.

```csharp
DLR_FurtherModes FurtherModes
```

**See also**

[`DLR_FurtherModes`](dlr-further-modes.html)

