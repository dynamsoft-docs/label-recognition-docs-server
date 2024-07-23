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

*Inheritance:* [CIntermediateResultUnit]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CRawTextLinesUnit

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
