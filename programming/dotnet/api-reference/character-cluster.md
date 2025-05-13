---
layout: default-layout
title: CharacterCluster - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: The class CharacterCluster represents a character cluster for .NET Edition.
keywords: character cluster
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CharacterCluster

The `CharacterCluster` class represents a character cluster generated from the buffered character items. These buffered items will be clustered based on feature similarity to obtain cluster centers.

## Definition

*Namespace:* Dynamsoft.DLR


```csharp
class CharacterCluster
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCharacter`](#getcharacter) | Gets the character value of the cluster. |
| [`GetMean`](#getmean) | Gets the mean of the cluster. |

### GetCharacter

Gets the character value of the cluster

```csharp
int GetCharacter()
```

**Return value**

Returns the character value of the cluster.

### GetMean

Gets the mean of the cluster.

```csharp
BufferedCharacterItem GetMean()
```

**Return value**

Returns the mean of the cluster.

**See Also**

[BufferedCharacterItem]({{ site.dlr_dotnet_api }}buffered-character-item.html)
