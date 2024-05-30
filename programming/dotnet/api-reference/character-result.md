---
layout: default-layout
title: CharacterResult Class - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: Definition of the CharacterResult class in Dynamsoft Label Recognizer Module .NET Edition.
keywords: Character result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CharacterResult

The `CharacterResult` class represents the result of a character recognition process. It contains the characters recognized (high, medium, and low confidence), their respective confidences, and the location of the character in a quadrilateral shape.

## Definition

*Namespace:* Dynamsoft.DLR

*Assembly:* Dynamsoft.LabelRecognizer.dll

```csharp
public class CharacterResult
```

## Attributes
  
| Attribute | Type |
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

```csharp
char characterH;
```

### characterM

The character with medium confidence.

```csharp
char characterM;
```

### characterL

The character with low confidence.

```csharp
char characterL;
```

### location

The location of the character in a quadrilateral shape.

```csharp
Quadrilateral location;
```

**See Also**

[Quadrilateral]({{ site.dcv_dotnet_api }}core/basic-classes/quadrilateral.html)

### characterHConfidence

The confidence of the character with high confidence.

```csharp
int characterHConfidence;
```

### characterMConfidence

The confidence of the character with medium confidence.

```csharp
int characterMConfidence;
```

### characterLConfidence

The confidence of the character with low confidence.

```csharp
int characterLConfidence;
```
