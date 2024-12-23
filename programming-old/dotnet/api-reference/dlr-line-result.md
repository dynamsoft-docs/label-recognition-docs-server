---
layout: default-layout
title: DLR_LineResult - Dynamsoft Label Recognizer .Net Class
description: This page shows the DLR_LineResult struct of Dynamsoft Label Recognizer for .Net Language.
keywords: DLR_LineResult, struct, .Net
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/dotnet/api-reference/dlr-line-result.html
---


# DLR_LineResult
Stores the line result.
  
```csharp
class Dynamsoft.DLR.DLR_LineResult
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`LineSpecificationName`](#linespecificationname) | *string* |
| [`Text`](#text) | *string* |
| [`CharacterModelName`](#charactermodelname) | *string* |
| [`Location`](#location) | [`Quadrilateral`](quadrilateral.html) |
| [`Confidence`](#confidence) | *int* |
| [`CharacterResults`](#characterresults) | [`DLR_CharacterResult[]`](dlr-character-result.html) |


&nbsp;

### LineSpecificationName
The name of the line specification used to recognize current line result.
```csharp
string LineSpecificationName
```

&nbsp;

### Text
The recognized text, ends by '\0'.
```csharp
string Text
```

&nbsp;

### CharacterModelName
The character model used to recognize the text.
```csharp
string CharacterModelName
```

&nbsp;

### Location
The location of current line.
```csharp
Quadrilateral Location
```


&nbsp;

### Confidence
The confidence of the result. It ranges from 0 to 100.
```csharp
int Confidence
```

&nbsp;

### CharacterResults
The character results array.
```csharp
DLR_CharacterResult[] CharacterResults
```

