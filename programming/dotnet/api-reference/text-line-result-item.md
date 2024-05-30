---
layout: default-layout
title: TextLineResultItem Class - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: Definition of the TextLineResultItem class in Dynamsoft Label Recognizer Module .NET Edition.
keywords: Text line result item
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextLineResultItem

The `TextLineResultItem` class represents a text line result item recognized by the library. It is derived from `CapturedResultItem`.

## Definition

*Namespace:* Dynamsoft.DLR

*Assembly:* Dynamsoft.LabelRecognizer.dll

*Inheritance:* [CapturedResultItem]({{ site.dcv_dotnet_api }}core/basic-classes/captured-result-item.html) -> TextLineResultItem

```csharp
public class TextLineResultItem : CapturedResultItem
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetText`](#gettext) | Gets the text content of the text line. |
| [`GetLocation`](#getlocation) | Gets the location of the text line in the form of a quadrilateral. |
| [`GetConfidence`](#getconfidence) | Gets the confidence of the text line recognition result. |
| [`GetCharacterResults`](#getcharacterresults) | Gets all the character results. |
| [`GetCapturedResultItemType`](#getcapturedresultitemtype) | Gets the type of the captured result item. |
| [`GetReferenceItem`](#getreferenceitem) | Gets the referenced item in the captured result item. |

### GetText

Gets the text content of the text line.

```csharp
string GetText()
```

**Return Value**

Returns the text content of the text line.

### GetLocation

Gets the location of the text line in the form of a quadrilateral.

```csharp
Quadrilateral GetLocation()
```

**Return Value**

Returns the location of the text line in the form of a quadrilateral.

**See Also**

[Quadrilateral]({{ site.dcv_dotnet_api }}core/basic-classes/quadrilateral.html)

### GetConfidence

Gets the confidence of the text line recognition result.

```csharp
int GetConfidence()
```

**Return Value**

Returns the confidence of the text line recognition result.

### GetCharacterResults

Gets all the character results.

```csharp
CharacterResult[] GetCharacterResults()
```

**Return Value**

Returns all the character results as a `CharacterResult` array.

**See Also**

[CharacterResult]({{ site.dlr_dotnet_api }}character-result.html)

### GetCapturedResultItemType

Gets the type of the captured result item.

```csharp
EnumCapturedResultItemType GetCapturedResultItemType()
```

**Return Value**

Returns the type of the captured result item.

**See Also**

[EnumCapturedResultItemType]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=dotnet)

### GetReferenceItem

Gets the referenced item in the captured result item.

```csharp
CapturedResultItem GetReferenceItem()
```

**Return Value**

Returns the referenced item in the captured result item.

**See Also**

[CapturedResultItem]({{ site.dcv_dotnet_api }}core/basic-classes/captured-result-item.html)
