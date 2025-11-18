---
layout: default-layout
title: CRawTextLinesUnit - Dynamsoft Label Recognizer Classes
description: The class CRawTextLinesUnit of Dynamsoft Label Recognizer represents a unit that contains recognized raw text lines.
keywords: Recognized raw text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CRawTextLinesUnit
---

# CRawTextLinesUnit

The `CRawTextLinesUnit` class represents an intermediate result unit containing raw text lines. It inherits from the `CIntermediateResultUnit` class.

## Definition

*Namespace:* dynamsoft::dlr::intermediate_results

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CRawTextLinesUnit : public CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CRawTextLinesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the number of raw text lines in the unit.|
| [`GetRawTextLine`](#getrawtextline) | Gets a pointer to a specific raw text line.|
| [`operator[]`](#operator) | Gets a pointer to a specific raw text line.|
| [`RemoveAllRawTextLines`](#removeallrawtextlines) | Removes all raw text lines.|
| [`RemoveRawTextLine`](#removerawtextline) | Removes the raw text line at the specified index.|
| [`AddRawTextLine`](#addrawtextline) | Adds a raw text line.|
| [`SetRawTextLine`](#setrawtextline) | Sets the raw text line at the specified index.|
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

Gets the number of raw text lines in the unit.

```cpp
virtual int GetCount() const = 0;
```

**Return value**

Returns the number of raw text lines in the unit.

### GetRawTextLine

Gets a pointer to a specific raw text line.

```cpp
virtual const CRawTextLine* GetRawTextLine(int index) const = 0;
```

**Parameters**

`[in] index` The index of the raw text line to retrieve.

**Return value**

Returns a const pointer to the raw text line at the specified index.

### operator[]

Gets a pointer to a specific raw text line.

```cpp
virtual const CRawTextLine* operator[](int index) const = 0;
```

**Parameters**

`[in] index` The index of the raw text line to retrieve.

**Return value**

Returns a const pointer to the raw text line at the specified index.

### RemoveAllRawTextLines

Removes all raw text lines.

```cpp
virtual void RemoveAllRawTextLines() = 0;
```

### RemoveRawTextLine

Removes the raw text line at the specified index.

```cpp
virtual int RemoveRawTextLine(int index) = 0;
```

**Parameters**

`[in] index` The index of the raw text line to remove.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### AddRawTextLine

Adds a raw text line.

```cpp
virtual int AddRawTextLine(const CRawTextLine* textline, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] textline` The raw text line to add.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### SetRawTextLine

Sets the raw text line at the specified index.

```cpp
virtual int SetRawTextLine(int index, const CRawTextLine* textline, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] index` The index of the raw text line to set.

`[in] textline` The raw text line to set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.
