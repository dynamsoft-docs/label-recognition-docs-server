---
layout: default-layout
title: BufferedCharacterItemSet - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: The class BufferedCharacterItemSet represents a collection of buffered character items and associated character clusters for .NET Edition.
keywords: Buffered character item set
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BufferedCharacterItemSet

The `BufferedCharacterItemSet` class represents a collection of buffered character items and associated character clusters. Each item in the collection is a [BufferedCharacterItem]({{ site.dlr_dotnet_api }}buffered-character-item.html) object.

## Definition

*Namespace:* Dynamsoft.DLR


```csharp
class BufferedCharacterItemSet : IEnumerable<BufferedCharacterItem>
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetItemsCount`](#getitemscount) | Gets the number of items in the buffered item set. |
| [`GetItem`](#getitem) | Gets the `BufferedCharacterItem` object at the specified index. |
| [`GetItems`](#getitems) | Gets all the `BufferedCharacterItem` objects. |
| [`GetCharacterClustersCount`](#getcharacterclusterscount) | Gets the number of character clusters in the buffered item set.|
| [`GetCharacterCluster`](#getcharactercluster) | Gets the character cluster at the specified index.|
| [`GetCharacterClusters`](#getcharacterclusters) | Gets all the character clusters.|

### GetItemsCount

Gets the number of items in the buffered item set.

```csharp
int GetItemsCount()
```

**Return value**

Returns the number of items in the buffered item set.

### GetItem

Gets the `BufferedCharacterItem` object at the specified index.

```csharp
BufferedCharacterItem GetItem(int index)
```

**Parameters**

`[in] index` The index of the item to retrieve.

**Return value**

Returns the `BufferedCharacterItem` object at the specified index.

**See Also**

[BufferedCharacterItem]({{ site.dlr_dotnet_api }}buffered-character-item.html)

### GetItems

Gets all the `BufferedCharacterItem` objects.

```csharp
BufferedCharacterItem[] GetItems()
```

**Return value**

Returns all the `BufferedCharacterItem` objects.

**See Also**

[BufferedCharacterItem]({{ site.dlr_dotnet_api }}buffered-character-item.html)

### GetCharacterClustersCount

Gets the number of character clusters in the buffered item set.

```csharp
int GetCharacterClustersCount()
```

**Return value**

Returns the number of character clusters in the buffered item set.

### GetCharacterCluster

Gets the character cluster at the specified index.

```csharp
CharacterCluster GetCharacterCluster(int index)
```

**Parameters**

`[in] index` The index of the character cluster to retrieve.

**Return value**

Returns the character cluster at the specified index.

**See Also**

[CharacterCluster]({{ site.dlr_dotnet_api }}character-cluster.html)

### GetCharacterClusters

Gets all the character clusters.

```csharp
CharacterCluster[] GetCharacterClusters()
```

**Return value**

Returns all the character clusters.

**See Also**

[CharacterCluster]({{ site.dlr_dotnet_api }}character-cluster.html)

