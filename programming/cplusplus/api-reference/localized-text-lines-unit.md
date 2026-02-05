---
layout: default-layout
title: CLocalizedTextLinesUnit - Dynamsoft Label Recognizer Classes
description: The class CLocalizedTextLinesUnit of Dynamsoft Label Recognizer represents a unit that contains localized text lines.
keywords: Localized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CLocalizedTextLinesUnit
---

# CLocalizedTextLinesUnit

The `CLocalizedTextLinesUnit` class represents a unit that contains localized text lines. It inherits from the `CIntermediateResultUnit` class.

## Definition

*Namespace:* dynamsoft::dlr::intermediate_results

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CLocalizedTextLinesUnit : public CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CLocalizedTextLinesUnit

## Methods

| Method                            | Description |
|-----------------------------------|-------------|
| [`GetCount`](#getcount)           | Gets the number of localized text lines in the unit.|
| [`GetLocalizedTextLine`](#getlocalizedtextline) | Gets a pointer to a specific localized text line element.|
| [`operator[]`](#operator) | Gets a pointer to a specific localized text line element.|
| [`RemoveAllLocalizedTextLines`](#removealllocalizedtextlines) | Removes all localized text lines.|
| [`RemoveLocalizedTextLine`](#removelocalizedtextline) | Removes the localized text line at the specified index.|
| [`AddLocalizedTextLine`](#addlocalizedtextline) | Adds a localized text line.|
| [`SetLocalizedTextLine`](#setlocalizedtextline) | Sets the localized text line at the specified index.|
| [`GetAuxiliaryRegionElementsCount`](#getauxiliaryregionelementscount) | Gets the count of auxiliary region elements in this unit.|
| [`GetAuxiliaryRegionElement`](#getauxiliaryregionelement) | Gets the auxiliary region element at the specified index.|
| [`SetAuxiliaryRegionElement`](#setauxiliaryregionelement) | Sets or replaces the auxiliary region element at the specified index.|
| [`AddAuxiliaryRegionElement`](#addauxiliaryregionelement) | Adds a new auxiliary region element to this unit.|
| [`RemoveAuxiliaryRegionElement`](#removeauxiliaryregionelement) | Removes the auxiliary region element at the specified index.|
| [`RemoveAllAuxiliaryRegionElements`](#removeallauxiliaryregionelements) | Removes all auxiliary region elements from this unit.|
| **Methods Inherited from [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html):** | |
| [`GetHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit.|
| [`GetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the image tag of the original image. |
| [`GetType`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit. |
| [`Clone`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`SetHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#sethashid) | Sets the hash ID of the unit. |
| [`SetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#setoriginalimagehashid) | Sets the hash ID of the original image. |
| [`SetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#setoriginalimagetag) | Sets the image tag of the original image. |
| [`Retain`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#retain) | Increases the reference count of the unit. |
| [`Release`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#release) | Decreases the reference count of the unit. |
| [`GetTransformMatrix`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via TransformMatrixType. |
| [`SetTransformMatrix`]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html#settransformmatrix) | Sets the transformation matrix via TransformMatrixType. |

### GetCount

Gets the number of localized text lines in the unit.

```cpp
virtual int GetCount() const = 0;
```

**Return value**

Returns the number of localized text lines in the unit.

### GetLocalizedTextLine

Gets a pointer to a specific localized text line element.

```cpp
virtual const CLocalizedTextLineElement* GetLocalizedTextLine(int index) const = 0;
```

**Parameters**

`[in] index` The index of the localized text line element to retrieve.

**Return value**

Returns a const pointer to the localized text line element at the specified index.

### operator[]

Gets a pointer to a specific localized text line element.

```cpp
virtual const CLocalizedTextLineElement* operator[](int index) const = 0;
```

**Parameters**

`[in] index` The index of the localized text line element to retrieve.

**Return value**

Returns a const pointer to the localized text line element at the specified index.

### RemoveAllLocalizedTextLines

Removes all localized text lines.

```cpp
virtual void RemoveAllLocalizedTextLines() = 0;
```

### RemoveLocalizedTextLine

Removes the localized text line at the specified index.

```cpp
virtual int RemoveLocalizedTextLine(int index) = 0;
```

**Parameters**

`[in] index` The index of the localized text line to remove.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### AddLocalizedTextLine

Adds a localized text line.

```cpp
virtual int AddLocalizedTextLine(const CLocalizedTextLineElement* element, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] element` The localized text line element to add.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### SetLocalizedTextLine

Sets the localized text line at the specified index.

```cpp
virtual int SetLocalizedTextLine(int index, const CLocalizedTextLineElement* element, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] index` The index of the localized text line to set.

`[in] element` The localized text line element to set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### GetAuxiliaryRegionElementsCount

Gets the count of auxiliary region elements in this unit.

```cpp
virtual int GetAuxiliaryRegionElementsCount() const = 0;
```

**Return value**

Returns the number of auxiliary region elements.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### GetAuxiliaryRegionElement

Gets the auxiliary region element at the specified index.

```cpp
virtual const CAuxiliaryRegionElement* GetAuxiliaryRegionElement(int index) const = 0;
```

**Parameters**

`[in] index` The zero-based index of the auxiliary region element to retrieve.

**Return value**

Returns a pointer to the `CAuxiliaryRegionElement` object, or NULL if the index is out of range.

**See Also**

[CAuxiliaryRegionElement]({{ site.dcvb_cpp_api }}core/intermediate-results/auxiliary-region-element.html)

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### SetAuxiliaryRegionElement

Sets or replaces the auxiliary region element at the specified index.

```cpp
virtual int SetAuxiliaryRegionElement(int index, const CAuxiliaryRegionElement* element, const double matrixToOriginalImage[9] = IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] index` The zero-based index where the element should be set.

`[in] element` The auxiliary region element to set.

`[in] matrixToOriginalImage` The transformation matrix from the current image to the original image.

**Return value**

Returns 0 if successful, otherwise returns an error code.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### AddAuxiliaryRegionElement

Adds a new auxiliary region element to this unit.

```cpp
virtual int AddAuxiliaryRegionElement(const CAuxiliaryRegionElement* element, const double matrixToOriginalImage[9] = IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] element` The auxiliary region element to add.

`[in] matrixToOriginalImage` The transformation matrix from the current image to the original image.

**Return value**

Returns 0 if successful, otherwise returns an error code.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### RemoveAuxiliaryRegionElement

Removes the auxiliary region element at the specified index.

```cpp
virtual int RemoveAuxiliaryRegionElement(int index) = 0;
```

**Parameters**

`[in] index` The zero-based index of the auxiliary region element to remove.

**Return value**

Returns 0 if successful, otherwise returns an error code.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### RemoveAllAuxiliaryRegionElements

Removes all auxiliary region elements from this unit.

```cpp
virtual void RemoveAllAuxiliaryRegionElements() = 0;
```

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

