---
layout: default-layout
title: LocalizedTextLineElement - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: The class LocalizedTextLineElement represents a localized text line element for .NET Edition.
keywords: Localized text line element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LocalizedTextLineElement

The `LocalizedTextLineElement` class represents a localized text line element. It inherits from the `RegionObjectElement` class.

## Definition

*Namespace:* Dynamsoft.DLR.intermediate_results


```csharp
class LocalizedTextLineElement : RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html) -> LocalizedTextLineElement

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetCharacterQuadsCount`](#getcharacterquadscount) | Gets the number of character quads in the text line.|
| [`GetCharacterQuad`](#getcharacterquad) | Gets the quadrilateral of a specific character in the text line. |
| [`GetCharacterQuads`](#getcharacterquads) | Gets all the quadrilaterals of all characters in the text line. |
| [`GetRowNumber`](#getrownumber) | Gets the row number of the text line. |
| [`SetLocation`](#setlocation) | Sets the location of the current object. |

### GetCharacterQuadsCount

Gets the number of character quads in the text line.

```csharp
int GetCharacterQuadsCount()
```

**Return value**

Returns the number of character quads in the text line.

### GetCharacterQuad

Gets the quadrilateral of a specific character in the text line.

```csharp
int GetCharacterQuad(int index, out Quadrilateral quad)
```

**Parameters**

`[in] index` The index of the character.

`[out] quad` The quadrilateral of the character.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### GetCharacterQuads

Gets all the quadrilaterals of all characters in the text line.

```csharp
int GetCharacterQuads(out Quadrilateral[] quads)
```

**Parameters**

`[out] quads` The quadrilaterals of all the characters.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### GetRowNumber

Gets the row number of the text line.

```csharp
int GetRowNumber()
```

**Return value**

Returns the row number of the text line.

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
