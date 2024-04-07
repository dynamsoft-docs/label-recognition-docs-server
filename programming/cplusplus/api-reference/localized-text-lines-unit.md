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

*Inheritance:* [CIntermediateResultUnit]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CLocalizedTextLinesUnit

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
