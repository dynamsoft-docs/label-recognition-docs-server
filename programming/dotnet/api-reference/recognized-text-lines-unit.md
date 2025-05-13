---
layout: default-layout
title: RecognizedTextLinesUnit - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: The class RecognizedTextLinesUnit represents an intermediate result unit containing recognized text lines for .NET Edition.
keywords: Recognized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RecognizedTextLinesUnit

The `RecognizedTextLinesUnit` class represents an intermediate result unit containing recognized text lines. It inherits from the `IntermediateResultUnit` class.

## Definition

*Namespace:* Dynamsoft.DLR.intermediate_results


```csharp
class RecognizedTextLinesUnit : IntermediateResultUnit, IEnumerable<RecognizedTextLineElement>
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) -> RecognizedTextLinesUnit

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the number of recognized text lines in the unit.|
| [`GetRecognizedTextLine`](#getrecognizedtextline) | Gets the `RecognizedTextLineElement` object at the specified index. |
| [`GetRecognizedTextLines`](#getrecognizedtextlines) | Gets all the `RecognizedTextLineElement` objects. |
| [`RemoveAllRecognizedTextLines`](#removeallrecognizedtextlines) | Removes all recognized text lines. |
| [`RemoveRecognizedTextLine`](#removerecognizedtextline) | Removes the recognized text line at the specified index. |
| [`AddRecognizedTextLine`](#addrecognizedtextline) | Adds a recognized text line. |
| [`SetRecognizedTextLine`](#setrecognizedtextline) | Sets the recognized text line at the specified index. |


### GetCount

Gets the number of recognized text lines in the unit.

```csharp
int GetCount()
```

**Return value**

Returns the number of recognized text lines in the unit.

### GetRecognizedTextLine

Gets the `RecognizedTextLineElement` object at the specified index.

```csharp
RecognizedTextLineElement GetRecognizedTextLine(int index)
```

**Parameters**

`[in] index` The index of the desired `RecognizedTextLineElement` object.

**Return value**

Returns the `RecognizedTextLineElement` object at the specified index.

**See Also**

[RecognizedTextLineElement]({{ site.dlr_dotnet_api }}recognized-text-line-element.html)

### GetRecognizedTextLines

Gets all the `RecognizedTextLineElement` objects.

```csharp
RecognizedTextLineElement[] GetRecognizedTextLines()
```

**Return value**

Returns all the `RecognizedTextLineElement` objects.

**See Also**

[RecognizedTextLineElement]({{ site.dlr_dotnet_api }}recognized-text-line-element.html)

### RemoveAllRecognizedTextLines

Removes all recognized text lines.

```csharp
void RemoveAllRecognizedTextLines()
```

### RemoveRecognizedTextLine

Removes the recognized text line at the specified index.

```csharp
int RemoveRecognizedTextLine(int index)
```

**Parameters**

`[in] index` The index of the recognized text line to remove.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### AddRecognizedTextLine

Adds a recognized text line.

```csharp
int AddRecognizedTextLine(RecognizedTextLineElement recognizedTextLine, double[] matrixToOriginalImage)
```

**Parameters**

`[in] recognizedTextLine` The recognized text line to add.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[RecognizedTextLineElement]({{ site.dlr_dotnet_api }}recognized-text-line-element.html)

### SetRecognizedTextLine

Sets the recognized text line at the specified index.

```csharp
int SetRecognizedTextLine(int index, RecognizedTextLineElement recognizedTextLine, double[] matrixToOriginalImage)
```

**Parameters**

`[in] index` The index of the recognized text line to set.

`[in] recognizedTextLine` The recognized text line to set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[RecognizedTextLineElement]({{ site.dlr_dotnet_api }}recognized-text-line-element.html)
