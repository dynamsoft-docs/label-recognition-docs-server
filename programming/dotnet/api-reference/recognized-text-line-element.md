---
layout: default-layout
title: RecognizedTextLineElement - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: The class RecognizedTextLineElement represents a line of recognized text in an image for .NET Edition.
keywords: Recognized text line element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RecognizedTextLineElement

The `RecognizedTextLineElement` class represents a line of recognized text in an image. It inherits from the `RegionObjectElement` class.

## Definition

*Namespace:* Dynamsoft.DLR.intermediate_results


```csharp
class RecognizedTextLineElement : RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html) -> RecognizedTextLineElement

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetText`](#gettext) | Gets the recognized text. |
| [`GetConfidence`](#getconfidence) | Gets the confidence level of the recognized text. |
| [`GetCharacterResultsCount`](#getcharacterresultscount) | Gets the number of individual character recognition results in the line. |
| [`GetCharacterResult`](#getcharacterresult) | Gets the character recognition result at the specified index. |
| [`GetCharacterResults`](#getcharacterresults) | Gets all the character recognition results. |
| [`GetRowNumber`](#getrownumber) | Gets the row number of the text line within the image. |
| [`GetSpecificationName`](#getspecificationname) | Gets the name of the text line specification that generated this element. |
| [`GetRawText`](#getrawtext) | Gets the recognized raw text, excluding any concatenation separators. |
| [`SetLocation`](#setlocation) | Sets the location of the current object. |
| [`SetText`](#settext) | Sets the recognized text. |

### GetText

Gets the recognized text.

```csharp
string GetText()
```

**Return value**

Returns the recognized text.

### GetConfidence

Gets the confidence level of the recognized text.

```csharp
int GetConfidence()
```

**Return value**

Returns an integer value representing the confidence level of the recognized text.

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

Returns a `CharacterResult` object stores the result.

**See Also**

[CharacterResult]({{ site.dlr_dotnet_api }}character-result.html)

### GetCharacterResults

Gets all the character recognition results.

```csharp
CharacterResult[] GetCharacterResults()
```

**Return value**

Returns a `CharacterResult` object array stores the results.

**See Also**

[CharacterResult]({{ site.dlr_dotnet_api }}character-result.html)

### GetRowNumber

Gets the row number of the text line within the image.

```csharp
int GetRowNumber()
```

**Return value**

Returns an integer value representing the row number of the text line within the image.

### GetSpecificationName

Gets the name of the text line specification that generated this element.

```csharp
string GetSpecificationName()
```

**Return value**

Returns the name of the text line specification that generated this element.

### GetRawText

Gets the recognized raw text, excluding any concatenation separators.

```csharp
string GetRawText()
```

**Return value**

Returns the recognized raw text.

### SetLocation

Sets the location of the current object.

```csharp
int SetLocation(Quadrilateral location)
```

**Parameters**

`[in] location` The location of the barcode.

**Return value**

Returns the row number of the text line.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### SetText

Sets the recognized text.

```csharp
void SetText(string text)
```

**Parameters**

`[in] text` The text to set.

