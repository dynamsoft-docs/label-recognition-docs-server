---
layout: default-layout
title: RawTextLinesUnit - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: The class RawTextLinesUnit represents a unit that contains recognized raw text lines for .NET Edition.
keywords: Recognized raw text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RawTextLinesUnit

The `RawTextLinesUnit` class represents an intermediate result unit containing raw text lines. It inherits from the `IntermediateResultUnit` class.

## Definition

*Namespace:* Dynamsoft.DLR.intermediate_results


```csharp
class RawTextLinesUnit : IntermediateResultUnit, IEnumerable<RawTextLine>
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) -> RawTextLinesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the number of raw text lines in the unit.|
| [`GetRawTextLine`](#getrawtextline) | Gets a specific raw text line.|
| [`GetRawTextLines`](#getrawtextlines) | Gets all raw text lines.|
| [`RemoveAllRawTextLines`](#removeallrawtextlines) | Removes all raw text lines.|
| [`RemoveRawTextLine`](#removerawtextline) | Removes the raw text line at the specified index.|
| [`AddRawTextLine`](#addrawtextline) | Adds a raw text line.|
| [`SetRawTextLine`](#setrawtextline) | Sets the raw text line at the specified index.|

### GetCount

Gets the number of raw text lines in the unit.

```csharp
int GetCount()
```

**Return value**

Returns the number of raw text lines in the unit.

### GetRawTextLine

Gets a specific raw text line.

```csharp
RawTextLine GetRawTextLine(int index)
```

**Parameters**

`[in] index` The index of the raw text line to retrieve.

**Return value**

Returns the raw text line at the specified index.

**See Also**

[RawTextLine]({{ site.dlr_dotnet_api }}raw-text-line.html)

### GetRawTextLines

Gets all raw text lines.

```csharp
RawTextLine[] GetRawTextLines()
```

**Return value**

Returns all the raw text lines.

**See Also**

[RawTextLine]({{ site.dlr_dotnet_api }}raw-text-line.html)

### RemoveAllRawTextLines

Removes all raw text lines.

```csharp
void RemoveAllRawTextLines()
```

### RemoveRawTextLine

Removes the raw text line at the specified index.

```csharp
int RemoveRawTextLine(int index)
```

**Parameters**

`[in] index` The index of the raw text line to remove.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### AddRawTextLine

Adds a raw text line.

```csharp
int AddRawTextLine(RawTextLine textline, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] textline` The raw text line to add.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[RawTextLine]({{ site.dlr_dotnet_api }}raw-text-line.html)

### SetRawTextLine

Sets the raw text line at the specified index.

```csharp
int SetRawTextLine(int index, RawTextLine textline, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] index` The index of the raw text line to set.

`[in] textline` The raw text line to set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[RawTextLine]({{ site.dlr_dotnet_api }}raw-text-line.html)
