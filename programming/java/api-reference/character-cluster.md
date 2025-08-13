---
layout: default-layout
title: CharacterCluster Class - Dynamsoft Label Recognizer Module Java Edition API Reference
description: Definition of the CharacterCluster class in Dynamsoft Label Recognizer Module Java Edition.
keywords: Character cluster
---

# CharacterCluster

The `CharacterCluster` class represents a character cluster generated from the buffered character items. These buffered items will be clustered based on feature similarity to obtain cluster centers.

## Definition

*Package:* com.dynamsoft.dlr

```java
public class CharacterCluster
```

## Methods
  
| Method  | Description |
|---------- |-------------|
| [`getCharacter`](#getcharacter) | Gets the character value of the cluster. |
| [`getMean`](#getmean) | Gets the mean of the cluster. |

### getCharacter

Gets the character value of the cluster.

```java
public char getCharacter()
```

**Return Value**

Returns the character value of the cluster.

### getMean

Gets the mean of the cluster.

```java
public BufferedCharacterItem getMean()
```

**Return Value**

Returns the mean of the cluster which is a `BufferedCharacterItem` object.

**See Also**

[BufferedCharacterItem]({{ site.dlr_java_api }}buffered-character-item.html)
