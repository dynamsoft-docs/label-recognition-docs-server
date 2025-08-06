---
layout: default-layout
title: CharacterResult Class - Dynamsoft Label Recognizer Module Java Edition API Reference
description: Definition of the CharacterResult class in Dynamsoft Label Recognizer Module Java Edition.
keywords: Character result
---

# CharacterResult

The `CharacterResult` class represents the result of a character recognition process. It contains the characters recognized (high, medium, and low confidence), their respective confidences, and the location of the character in a quadrilateral shape.

## Definition

*Package:* com.dynamsoft.dlr

```java
public class CharacterResult
```

## Properties
  
| Property  | Type |
|---------- | ---- |
| [`characterH`](#characterh) | *char* |
| [`characterM`](#characterm) | *char* |
| [`characterL`](#characterl) | *char* |
| [`location`](#location) | *Quadrilateral* |
| [`characterHConfidence`](#characterhconfidence) | *int* |
| [`characterMConfidence`](#charactermconfidence) | *int* |
| [`characterLConfidence`](#characterlconfidence) | *int* |

### characterH

The character with high confidence.

### characterM

The character with medium confidence.

### characterL

The character with low confidence.

### location

The location of the character in a quadrilateral shape.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### characterHConfidence

The confidence of the character with high confidence.

### characterMConfidence

The confidence of the character with medium confidence.

### characterLConfidence

The confidence of the character with low confidence.
