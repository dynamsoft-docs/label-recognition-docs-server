---
layout: default-layout
title: CRecognizedTextLinesUnit - Dynamsoft Label Recognizer Classes
description: The class CRecognizedTextLinesUnit of Dynamsoft Label Recognizer represents an intermediate result unit containing recognized text lines.
keywords: Recognized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CRecognizedTextLinesUnit
---

# CRecognizedTextLinesUnit

The `CRecognizedTextLinesUnit` class represents an intermediate result unit containing recognized text lines. It inherits from the `CIntermediateResultUnit` class.

## Definition

*Namespace:* dynamsoft::dlr::intermediate_results

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CRecognizedTextLinesUnit : public CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CRecognizedTextLinesUnit

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the number of recognized text lines in the unit.|
| [`GetRecognizedTextLine`](#getrecognizedtextline) | Gets a pointer to the CRecognizedTextLineElement object at the specified index. |
| [`operator[]`](#operator) | Gets a pointer to the CRecognizedTextLineElement object at the specified index. |
| [`RemoveAllRecognizedTextLines`](#removeallrecognizedtextlines) | Removes all recognized text lines. |
| [`RemoveRecognizedTextLine`](#removerecognizedtextline) | Removes the recognized text line at the specified index. |
| [`AddRecognizedTextLine`](#addrecognizedtextline) | Adds a recognized text line. |
| [`SetRecognizedTextLine`](#setrecognizedtextline) | Sets the recognized text line at the specified index. |
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

Gets the number of recognized text lines in the unit.

```cpp
virtual int GetCount() const = 0;
```

**Return value**

Returns the number of recognized text lines in the unit.

### GetRecognizedTextLine

Gets a pointer to the CRecognizedTextLineElement object at the specified index.

```cpp
virtual const CRecognizedTextLineElement* GetRecognizedTextLine(int index) const = 0;
```

**Parameters**

`[in] index` The index of the desired CRecognizedTextLineElement object.

**Return value**

Returns a pointer to the CRecognizedTextLineElement object at the specified index.

### operator[]

Gets a pointer to the CRecognizedTextLineElement object at the specified index.

```cpp
virtual const CRecognizedTextLineElement* operator[](int index) const = 0;
```

**Parameters**

`[in] index` The index of the desired CRecognizedTextLineElement object.

**Return value**

Returns a pointer to the CRecognizedTextLineElement object at the specified index.

### RemoveAllRecognizedTextLines

Removes all recognized text lines.

```cpp
virtual void RemoveAllRecognizedTextLines() = 0;
```

### RemoveRecognizedTextLine

Removes the recognized text line at the specified index.

```cpp
virtual int RemoveRecognizedTextLine(int index) = 0;
```

**Parameters**

`[in] index` The index of the recognized text line to remove.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### AddRecognizedTextLine

Adds a recognized text line.

```cpp
virtual int AddRecognizedTextLine(const CRecognizedTextLineElement* element, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] element` The recognized text line to add.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### SetRecognizedTextLine

Sets the recognized text line at the specified index.

```cpp
virtual int SetRecognizedTextLine(int index, const CRecognizedTextLineElement* element, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`[in] index` The index of the recognized text line to set.

`[in] element` The recognized text line to set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.
