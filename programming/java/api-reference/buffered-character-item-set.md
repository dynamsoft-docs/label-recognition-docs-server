---
layout: default-layout
title: BufferedCharacterItemSet Class - Dynamsoft Label Recognizer Module Java Edition API Reference
description: Definition of the BufferedCharacterItemSet class in Dynamsoft Label Recognizer Module Java Edition.
keywords: BufferedCharacterItemSet
---

# BufferedCharacterItemSet

The `BufferedCharacterItemSet` class represents a collection of buffered character items and associated character clusters.

## Definition

*Package:* com.dynamsoft.dlr

```java
public class BufferedCharacterItemSet
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getItems`](#getitems) | Gets all the buffered items. |
| [`getCharacterClusters`](#getcharacterclusters) | Gets all the character clusters. |

### getItems

Gets all the buffered items.

```java
public BufferedCharacterItem[] getItems()
```

**Return Value**

Returns a `BufferedCharacterItem` array.

**See Also**

[BufferedCharacterItem]({{ site.dlr_java_api }}buffered-character-item.html)

### getCharacterClusters

Gets all the character clusters.

```java
public CharacterCluster[] getCharacterClusters()
```

**Return Value**

Returns a `CharacterCluster` array.

**See Also**

[CharacterCluster]({{ site.dlr_java_api }}character-cluster.html)

