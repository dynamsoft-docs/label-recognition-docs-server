---
layout: default-layout
title: CharacterCluster Class - Dynamsoft Label Recognizer Module Python Edition API Reference
description: Definition of the CharacterCluster class in Dynamsoft Label Recognizer Module Python Edition.
keywords: Character result
---

# CharacterCluster

The `CharacterCluster` class represents a character cluster generated from the buffered character items. These buffered items will be clustered based on feature similarity to obtain cluster centers.

## Definition

*Module:* dynamsoft_label_recognizer

```python
class CharacterCluster
```

## Properties
  
| Property  | Description |
|---------- |-------------|
| [`get_character`](#get_character) | Gets the character value of the cluster. |
| [`get_mean`](#get_mean) | Gets the mean of the cluster. |

### get_character

Gets the character value of the cluster.

```python
def get_character(self) -> str:
```

**Return Value**

Returns the character value of the cluster.

### get_mean

Gets the mean of the cluster.

```python
def get_mean(self) -> BufferedCharacterItem:
```

**Return Value**

Returns the mean of the cluster which is a `BufferedCharacterItem` object.

**See Also**

[BufferedCharacterItem]({{ site.dlr_python_api }}buffered-character-item.html)
