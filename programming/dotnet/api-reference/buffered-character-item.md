---
layout: default-layout
title: BufferedCharacterItem - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: The class BufferedCharacterItem represents a buffered character item for .NET Edition.
keywords: buffered character item, .NET
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BufferedCharacterItem

The `BufferedCharacterItem` class represents a buffered character item. Each buffered character item represents a recognized character along with its image and features.

## Definition

*Namespace:* Dynamsoft.DLR


```csharp
class BufferedCharacterItem
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCharacter`](#getcharacter) | Gets the buffered character value. |
| [`GetImage`](#getimage) | Gets the image data of the buffered character. |
| [`GetFeaturesCount`](#getfeaturescount) | Gets the number of features of the buffered character. |
| [`GetFeature`](#getfeature) | Gets the feature id and value of the buffered character at the specified index. |
| [`GetFeatures`](#getfeatures) | Gets all the features of the buffered characters. |

### GetCharacter

Gets the buffered character value.

```csharp
char GetCharacter()
```

**Return value**

Returns the buffered character value.

### GetImage

Gets the image data of the buffered character.

```csharp
ImageData GetImage()
```

**Return value**

Returns the image data of the buffered character.

**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

### GetFeaturesCount

Gets the number of features of the buffered character.

```csharp
int GetFeaturesCount()
```

**Return value**

Returns the number of features of the buffered character.

### GetFeature

Gets the feature id and value of the buffered character at the specified index.

```csharp
int GetFeature(int index, out int featureId, out float featureValue)
```

**Parameters**

`[in] index` The index of the feature to retrieve.

`[out] featureId` The feature id.

`[out] featureValue` The feature value.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### GetFeatures

Gets all the features of the buffered characters.

```csharp
int GetFeatures(out int[] featureIds, out float[] featureValues)
```

**Parameters**

`[out] featureIds` The feature ids.

`[out] featureValues` The feature values.

**Return value**

Returns 0 if successful, otherwise returns a negative value.
