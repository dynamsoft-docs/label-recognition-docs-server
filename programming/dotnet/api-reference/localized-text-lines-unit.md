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
| [`GetAuxiliaryRegionElements`](#getauxiliaryregionelements) | Gets all auxiliary region elements. |
| [`SetAuxiliaryRegionElement`](#setauxiliaryregionelement) | Sets the auxiliary region element at the specified index. |
| [`AddAuxiliaryRegionElement`](#addauxiliaryregionelement) | Adds a new auxiliary region element to this unit. |
| [`RemoveAuxiliaryRegionElement`](#removeauxiliaryregionelement) | Removes the auxiliary region element at the specified index. |
| [`RemoveAllAuxiliaryRegionElements`](#removeallauxiliaryregionelements) | Removes all auxiliary region elements from this unit. |

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

### GetAuxiliaryRegionElements

Gets all auxiliary region elements.

```csharp
AuxiliaryRegionElement[] GetAuxiliaryRegionElements()
```

**Return value**

Returns an array of `AuxiliaryRegionElement` objects.

**See Also**

[AuxiliaryRegionElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/auxiliary-region-element.html)

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### SetAuxiliaryRegionElement

Sets or replaces the auxiliary region element at the specified index.

```csharp
int SetAuxiliaryRegionElement(int index, AuxiliaryRegionElement element, double[] matrixToOriginalImage)
```

**Parameters**

`[in] index` The zero-based index where the element should be set.

`[in] element` The auxiliary region element to set.

`[in] matrixToOriginalImage` The transformation matrix from the current image to the original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[AuxiliaryRegionElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/auxiliary-region-element.html)

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### AddAuxiliaryRegionElement

Adds a new auxiliary region element to this unit.

```csharp
int AddAuxiliaryRegionElement(AuxiliaryRegionElement element, double[] matrixToOriginalImage)
```

**Parameters**

`[in] element` The auxiliary region element to add.

`[in] matrixToOriginalImage` The transformation matrix from the current image to the original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[AuxiliaryRegionElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/auxiliary-region-element.html)

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### RemoveAuxiliaryRegionElement

Removes the auxiliary region element at the specified index.

```csharp
int RemoveAuxiliaryRegionElement(int index)
```

**Parameters**

`[in] index` The zero-based index of the auxiliary region element to remove.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### RemoveAllAuxiliaryRegionElements

Removes all auxiliary region elements from this unit.

```csharp
void RemoveAllAuxiliaryRegionElements()
```

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

