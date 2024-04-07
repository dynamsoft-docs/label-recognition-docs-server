---
layout: default-layout
title: CBufferedCharacterItemSet - Dynamsoft Label Recognizer Classes
description: The class CBufferedCharacterItemSet of Dynamsoft Label Recognizer represents a collection of buffered character items and associated character clusters.
keywords: Buffered character item set
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CBufferedCharacterItemSet
---

# CBufferedCharacterItemSet

The `CBufferedCharacterItemSet` class represents a collection of buffered character items and associated character clusters. Each item in the collection is a [`CBufferedCharacterItem`](buffered-character-item.md) object.

## Definition

*Namespace:* dynamsoft::dlr

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CBufferedCharacterItemSet
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetItemsCount`](#getitemscount) | Gets the number of items in the buffered item set. |
| [`GetItem`](#getitem) | Gets a pointer to the CBufferedCharacterItem object at the specified index. |
| [`operator[]`](#operator) | Gets a pointer to the CBufferedCharacterItem object at the specified index. |
| [`GetCharacterClustersCount`](#getcharacterclusterscount) | Gets the number of character clusters in the buffered item set.|
| [`GetCharacterCluster`](#getcharactercluster) | Gets the character cluster at the specified index.|
| [`Retain`](#retain) | Increases the reference count of the CBufferedCharacterItemSet object. |
| [`Release`](#release) | Decreases the reference count of the CBufferedCharacterItemSet object. |

### GetItemsCount

Gets the number of items in the buffered item set.

```cpp
virtual int GetItemsCount() const = 0;
```

**Return value**

Returns the number of items in the buffered item set.

### GetItem

Gets a pointer to the CBufferedCharacterItem object at the specified index.

```cpp
virtual const CBufferedCharacterItem* GetItem(int index) const = 0;
```

**Parameters**

`[in] index` The index of the item to retrieve.

**Return value**

Returns a pointer to the CBufferedCharacterItem object at the specified index.

### operator[]

Gets a pointer to the CBufferedCharacterItem object at the specified index.

```cpp
virtual const CBufferedCharacterItem* operator[](int index) const = 0;
```

**Parameters**

`[in] index` The index of the item to retrieve.

**Return value**

Returns a pointer to the CBufferedCharacterItem object at the specified index.

### GetCharacterClustersCount

Gets the number of character clusters in the buffered item set.

```cpp
virtual int GetCharacterClustersCount() const = 0;
```

**Return value**

Returns the number of character clusters in the buffered item set.

### GetCharacterCluster

Gets the character cluster at the specified index.

```cpp
virtual const CCharacterCluster* GetCharacterCluster(int index) const = 0;
```

**Parameters**

`[in] index` The index of the character cluster to retrieve.

**Return value**

Returns the character cluster at the specified index.

### Retain

Increases the reference count of the CBufferedCharacterItemSet object.

```cpp
virtual CBufferedCharacterItemSet* Retain() = 0;
```

**Return value**

An object of CBufferedCharacterItemSet.

### Release

Decreases the reference count of the CBufferedCharacterItemSet object.

```cpp
virtual void Release() = 0;
```
