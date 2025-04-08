---
layout: default-layout
title: CharacterResult Class - Dynamsoft Label Recognizer Module Python Edition API Reference
description: Definition of the CharacterResult class in Dynamsoft Label Recognizer Module Python Edition.
keywords: Character result
---

# CharacterResult

The `CharacterResult` class represents the result of a character recognition process. It contains the characters recognized (high, medium, and low confidence), their respective confidences, and the location of the character in a quadrilateral shape.

## Definition

*Module:* dynamsoft_label_recognizer

```python
class CharacterResult
```

## Properties
  
| Property  | Type |
|---------- | ---- |
| [`character_h`](#character_h) | *str* |
| [`character_m`](#character_m) | *str* |
| [`character_l`](#character_l) | *str* |
| [`location`](#location) | *Quadrilateral* |
| [`character_h_confidence`](#character_h_confidence) | *int* |
| [`character_m_confidence`](#character_m_confidence) | *int* |
| [`character_l_confidence`](#character_l_confidence) | *int* |

### character_h

The character with high confidence.

### character_m

The character with medium confidence.

### character_l

The character with low confidence.

### location

The location of the character in a quadrilateral shape.

**See Also**

[Quadrilateral]({{ site.dcv_python_api }}core/basic-classes/quadrilateral.html)

### character_h_confidence

The confidence of the character with high confidence.

### character_m_confidence

The confidence of the character with medium confidence.

### character_l_confidence

The confidence of the character with low confidence.
