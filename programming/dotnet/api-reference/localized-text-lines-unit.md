---
layout: default-layout
title: LocalizedTextLinesUnit - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: The class LocalizedTextLinesUnit represents a unit that contains localized text lines for .NET Edition.
keywords: Localized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LocalizedTextLinesUnit

The `LocalizedTextLinesUnit` class represents a unit that contains localized text lines. It inherits from the `IntermediateResultUnit` class.

## Definition

*Namespace:* Dynamsoft.DLR.intermediate_results


```csharp
class LocalizedTextLinesUnit : IntermediateResultUnit, IEnumerable<LocalizedTextLineElement>
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) -> LocalizedTextLinesUnit

## Methods

| Method                            | Description |
|-----------------------------------|-------------|
| [`GetCount`](#getcount)           | Gets the number of localized text lines in the unit.|
| [`GetLocalizedTextLine`](#getlocalizedtextline) | Gets a specific localized text line element.|
| [`GetLocalizedTextLines`](#getlocalizedtextlines) | Gets all localized text line elements.|
| [`RemoveAllLocalizedTextLines`](#removealllocalizedtextlines) | Removes all localized text lines.|
| [`RemoveLocalizedTextLine`](#removelocalizedtextline) | Removes the localized text line at the specified index.|
| [`AddLocalizedTextLine`](#addlocalizedtextline) | Adds a localized text line.|
| [`SetLocalizedTextLine`](#setlocalizedtextline) | Sets the localized text line at the specified index.|

### GetCount

Gets the number of localized text lines in the unit.

```csharp
int GetCount()
```

**Return value**

Returns the number of localized text lines in the unit.

### GetLocalizedTextLine

Gets a specific localized text line element.

```csharp
LocalizedTextLineElement GetLocalizedTextLine(int index)
```

**Parameters**

`[in] index` The index of the localized text line element to retrieve.

**Return value**

Returns the localized text line element at the specified index.

**See Also**

[LocalizedTextLineElement]({{ site.dlr_dotnet_api }}localized-text-line-element.html)

### GetLocalizedTextLines

Gets all localized text line elements.

```csharp
LocalizedTextLineElement[] GetLocalizedTextLines()
```

**Return value**

Returns all the localized text line elements.

**See Also**

[LocalizedTextLineElement]({{ site.dlr_dotnet_api }}localized-text-line-element.html)

### RemoveAllLocalizedTextLines

Removes all localized text lines.

```csharp
void RemoveAllLocalizedTextLines()
```

### RemoveLocalizedTextLine

Removes the localized text line at the specified index.

```csharp
int RemoveLocalizedTextLine(int index)
```

**Parameters**

`[in] index` The index of the localized text line to remove.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### AddLocalizedTextLine

Adds a localized text line.

```csharp
int AddLocalizedTextLine(LocalizedTextLineElement localizedTextLine, double[] matrixToOriginalImage)
```

**Parameters**

`[in] localizedTextLine` The localized text line element to add.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[LocalizedTextLineElement]({{ site.dlr_dotnet_api }}localized-text-line-element.html)

### SetLocalizedTextLine

Sets the localized text line at the specified index.

```csharp
int SetLocalizedTextLine(int index, LocalizedTextLineElement localizedTextLine, double[] matrixToOriginalImage)
```

**Parameters**

`[in] index` The index of the localized text line to set.

`[in] localizedTextLine` The localized text line element to set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[LocalizedTextLineElement]({{ site.dlr_dotnet_api }}localized-text-line-element.html)
