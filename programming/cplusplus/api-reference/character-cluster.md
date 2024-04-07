---
layout: default-layout
title: CCharacterCluster - Dynamsoft Label Recognizer Classes
description: The class CCharacterCluster of Dynamsoft Label Recognizer represents a character cluster.
keywords: character cluster
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CCharacterCluster
---

# CCharacterCluster

The `CCharacterCluster` class represents a character cluster generated from the buffered character items. These buffered items will be clustered based on feature similarity to obtain cluster centers.

## Definition

*Namespace:* dynamsoft::dlr

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CCharacterCluster
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCharacter`](#getcharacter) | Gets the character value of the cluster. |
| [`GetMean`](#getmean) | Gets the mean of the cluster. |

### GetCharacter

Gets the character value of the cluster

```cpp
virtual char GetCharacter() const = 0;
```

**Return value**

Returns the character value of the cluster.

### GetMean

Gets the mean of the cluster.

```cpp
virtual const CBufferedCharacterItem* GetMean() const = 0;
```

**Return value**

Returns the mean of the cluster.
