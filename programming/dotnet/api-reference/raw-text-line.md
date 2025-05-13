---
layout: default-layout
title: RawTextLine - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: The class RawTextLine represents a recognized raw text line for .NET Edition.
keywords: Recognized raw text line
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RawTextLine

The class `RawTextLine` represents a recognized raw text line in an image. It can be in one of the following states:

* `RTLS_LOCALIZED`: Localized but recognition not performed.
* `RTLS_RECOGNITION_FAILED`: Recognition failed.
* `RTLS_RECOGNITION_SUCCEEDED`: Successfully recognized.

## Definition

*Namespace:* Dynamsoft.DLR.intermediate_results


```csharp
class RawTextLine : IDisposable
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetText`](#gettext) | Gets the recognized text.|
| [`GetConfidence`](#getconfidence) | Gets the confidence level of the recognized text.|
| [`GetCharacterResultsCount`](#getcharacterresultscount) | Gets the number of individual character recognition results in the line.|
| [`GetCharacterResult`](#getcharacterresult) | Gets the character recognition result at the specified index.|
| [`GetCharacterResults`](#getcharacterresults) | Gets all the character recognition results. |
| [`GetLocation`](#getlocation) | Gets the location of the text line.|
| [`GetRowNumber`](#getrownumber) | Gets the row number of the text line within the image.|
| [`GetSpecificationName`](#getspecificationname) | Gets the name of the text line specification that generated this element.|
| [`GetStatus`](#getstatus) | Gets the status of the text line.|
| [`SetText`](#settext) | Sets the recognized text.|
| [`SetLocation`](#setlocation) | Sets the location of the text line.|
| [`SetRowNumber`](#setrownumber) | Sets the row number of the text line within the image.|
| [`SetSpecificationName`](#setspecificationname) | Sets the name of the text line specification that generated this element.
| [`Clone`](#clone) | Clone the `RawTextLine` object.|
| [`SetCharacterResults`](#setcharacterresults) | Sets the character recognition results.|

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

Returns the character recognition result.

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

### GetLocation

Gets the location of the text line.

```csharp
Quadrilateral GetLocation()
```

**Return value**

Returns a `Quadrilateral` object which represents the location of the text line.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

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

Returns the name of the text line specification.

### GetStatus

Gets the status of the text line.

```csharp
EnumRawTextLineStatus GetStatus()
```

**Return value**

Returns the status of the text line.

**See also**

* [EnumRawTextLineStatus]({{ site.dlr_dotnet_api }}enum-raw-text-line-status.html)

### SetText

Sets the recognized text.

```csharp
void SetText(string text)
```

**Parameters**

`[in] text` The text to be set.


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

### SetRowNumber

Sets the row number of the text line within the image.

```csharp
int SetRowNumber(int rowNumber)
```

**Parameters**

`[in] rowNumber` The row number of the text line within the image.

**Return value**

Returns 0 if successful; otherwise returns an error code.

### SetSpecificationName

Sets the name of the text line specification that generated this element.

```csharp
int SetSpecificationName(string specificationName)
```

**Parameters**

`[in] specificationName` The name of the text line specification.

**Return value**

Returns 0 if successful; otherwise returns an error code.

### Clone

Clone the `RawTextLine` object.

```csharp
RawTextLine Clone()
```

**Return value**

Returns the cloned `RawTextLine` object.

### SetCharacterResults

Sets the character recognition results.

```csharp
int SetCharacterResults(CharacterResult[] charArray)
```

**Parameters**

`[in] charArray` The character result array.

**Return value**

Returns 0 if successful; otherwise returns an error code.