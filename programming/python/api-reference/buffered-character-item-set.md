---
layout: default-layout
title: BufferedCharacterItemSet Class - Dynamsoft Label Recognizer Module Python Edition API Reference
description: Definition of the BufferedCharacterItemSet class in Dynamsoft Label Recognizer Module Python Edition.
keywords: BufferedCharacterItemSet
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BufferedCharacterItemSet

The `BufferedCharacterItemSet` class represents a collection of buffered character items and associated character clusters.

## Definition

*Module:* dynamsoft_label_recognizer

```python
class BufferedCharacterItemSet(object)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_items`](#get_items) | Gets all the buffered items. |
| [`get_character_clusters`](#get_character_clusters) | Gets all the character clusters. |

### get_items

Gets all the buffered items.

```python
def get_items(self) -> List[BufferedCharacterItem]:
```

**Return Value**

Returns a `BufferedCharacterItem` list.

**See Also**

[BufferedCharacterItem]({{ site.dlr_python_api }}buffered-character-item.html)

### get_character_clusters

Gets all the character clusters.

```python
def get_character_clusters(self) -> List[CharacterCluster]:
```

**Return Value**

Returns a `CharacterCluster` list.

**See Also**

[CharacterCluster]({{ site.dlr_python_api }}character-cluster.html)

