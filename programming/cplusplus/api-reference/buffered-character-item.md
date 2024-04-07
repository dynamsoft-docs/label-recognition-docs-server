---
layout: default-layout
title: CBufferedCharacterItem - Dynamsoft Label Recognizer Classes
description: The class CBufferedCharacterItem of Dynamsoft Label Recognizer represents a buffered character item.
keywords: buffered character item, C++
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CBufferedCharacterItem
---

# CBufferedCharacterItem

The `CBufferedCharacterItem` class represents a buffered character item. Each buffered character item represents a recognized character along with its image and features.

## Definition

*Namespace:* dynamsoft::dlr

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CBufferedCharacterItem
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCharacter`](#getcharacter) | Gets the buffered character value. |
| [`GetImage`](#getimage) | Gets the image data of the buffered character. |
| [`GetFeaturesCount`](#getfeaturescount) | Gets the number of features of the buffered character. |
| [`GetFeature`](#getfeature) | Gets the feature id and value of the buffered character at the specified index. |

### GetCharacter

Gets the buffered character value.

```cpp
virtual char GetCharacter() const = 0;
```

**Return value**

Returns the buffered character value.

### GetImage

Gets the image data of the buffered character.

```cpp
virtual const CImageData* GetImage() const = 0;
```

**Return value**

Returns the image data of the buffered character.

### GetFeaturesCount

Gets the number of features of the buffered character.

```cpp
virtual int GetFeaturesCount() const = 0;
```

**Return value**

Returns the number of features of the buffered character.

### GetFeature

Gets the feature id and value of the buffered character at the specified index.

```cpp
virtual int GetFeature(int index, int* pFeatureId, float* pFeatureValue) const = 0;
```

**Parameters**

`[in] index` The index of the feature to retrieve.

`[out] pFeatureId` The feature id.

`[out] pFeatureValue` The feature value.

**Return value**

Returns 0 if successful, otherwise returns a negative value.
