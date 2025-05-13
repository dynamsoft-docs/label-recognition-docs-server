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


*Inheritance:* [CapturedResultItem]({{ site.dcvb_dotnet_api }}core/basic-classes/captured-result-item.html) -> TextLineResultItem

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
| [`GetCharacterResultsCount`](#getcharacterresultscount) | Gets the number of individual character recognition results in the line.|
| [`GetCharacterResult`](#getcharacterresult) | Gets the character recognition result at the specified index.|
| [`GetSpecificationName`](#getspecificationname) | Gets the name of the text line specification that generated this item.|
| [`GetRawText`](#GetRawText) | Gets the recognized raw text, excluding any concatenation separators.|
| [`SetLocation`](#setlocation) | Sets the location of the text line.|

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

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

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

### GetCharacterResultsCount

Gets the number of individual character recognition results in the line.

```csharp
int GetCharacterResultsCount()
```

**Return value**

Returns an integer value representing the number of individual character recognition results.

### GetCharacterResult

Gets the character recognition result at the specified index.

```csharp
CharacterResult GetCharacterResult(int index)
```

**Parameters**

`[in] index` The index of the character recognition result to retrieve.

**Return value**

Returns the character recognition result.

**See Also**

[CharacterResult]({{ site.dlr_dotnet_api }}character-result.html)

### GetSpecificationName

Gets the name of the text line specification that generated this item.

```csharp
string GetSpecificationName()
```

**Return value**

Returns the name of the text line specification.

### GetRawText

Gets the recognized raw text, excluding any concatenation separators.

```csharp
string GetRawText()
```

**Return Value**

Returns the recognized raw text, excluding any concatenation separators.

### SetLocation

Sets the location of the text line.

```csharp
int SetLocation(Quadrilateral location)
```

**Parameters**

`[in] location` The location of the text line.

**Return value**

Returns 0 if successful; otherwise returns an error code.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

