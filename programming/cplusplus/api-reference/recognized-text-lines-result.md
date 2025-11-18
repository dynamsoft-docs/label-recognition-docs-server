---
layout: default-layout
title: CRecognizedTextLinesResult - Dynamsoft Label Recognizer Classes
description: The class CRecognizedTextLinesResult of Dynamsoft Label Recognizer represents the result of a text recognition process.
keywords: Recognized text lines result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CRecognizedTextLinesResult
---

# CRecognizedTextLinesResult

The `CRecognizedTextLinesResult` class represents the result of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Namespace:* dynamsoft::dlr

*Assembly:* DynamsoftLabelRecognizer

*Inheritance:* [CCapturedResultBase]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html) -> CRecognizedTextLinesResult

```cpp
class CRecognizedTextLinesResult : public CCapturedResultBase
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetItemsCount`](#getitemscount) | Gets the number of text line result items in the recognition result. |
| [`GetItem`](#getitem) | Gets the text line result item at the specified index. |
| [`HasItem`](#hasitem) | Checks if the item is present in the array. |
| [`RemoveItem`](#removeitem) | Removes a specific item from the array in the recognition result. |
| [`operator[]`](#operator) | Gets the text line result item at the specified index. |
| [`AddItem`](#additem) | Adds a specific item to the array in the recognized text lines result. |
| [`Retain`](#retain) | Increases the reference count of the CRecognizedTextLinesResult object. |
| [`Release`](#release) | Decreases the reference count of the CRecognizedTextLinesResult object. |
| **Methods Inherited from [CCapturedResultBase]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html):** | |
| [`GetOriginalImageHashId`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html#getoriginalimagetag) | Gets the tag of the original image. |
| [`GetRotationTransformMatrix`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html#getrotationtransformmatrix) | Gets the rotation transformation matrix of the original image relative to the rotated image. |
| [`GetErrorCode`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html#geterrorcode) | Gets the error code of the recognition result, if an error occurred. |
| [`GetErrorString`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-base.html#geterrorstring) | Gets the error message of the recognition result, if an error occurred. |

### GetItemsCount

Gets the number of text line result items in the recognition result.

```cpp
virtual int GetItemsCount() const = 0;
```

**Return value**

Returns the number of text line result items in the recognition result.

### GetItem

Gets the text line result item at the specified index.

```cpp
virtual const CTextLineResultItem* GetItem(int index) const = 0;
```

**Parameters**

`[in] index` The zero-based index of the text line result item to retrieve.

**Return value**

Returns a pointer to the CTextLineResultItem object at the specified index.

### HasItem

Check if the item is present in the array.

```cpp
bool HasItem(const CTextLineResultItem* item) const
```

**Parameters**

`[in] item` The specific item to check.

**Return value**

Returns a bool value indicating whether the item is present in the array or not.

### RemoveItem

Remove a specific item from the array in the recognition result.

```cpp
int RemoveItem(const CTextLineResultItem* item)
```

**Parameters**

`[in] item` The specific item to remove.

**Return value**

Return value indicating whether the deletion was successful or not.

### operator[]

Gets the text line result item at the specified index.

```cpp
virtual const CTextLineResultItem* operator[](int index) const = 0;
```

**Parameters**

`[in] index` The zero-based index of the text line result item to retrieve.

**Return value**

Returns a pointer to the CTextLineResultItem object at the specified index.

### Retain

Increases the reference count of the CRecognizedTextLinesResult object.

```cpp
virtual CRecognizedTextLinesResult* Retain() = 0;
```

**Return value**

An object of CRecognizedTextLinesResult.

### Release

Decreases the reference count of the CRecognizedTextLinesResult object.

```cpp
virtual void Release() = 0;
```

### AddItem

Add a specific item to the array in the recognized text lines result.

```cpp
virtual int AddItem(const CTextLineResultItem* item) = 0;
```

**Parameters**

`[in] item` The specific item to add.

**Return value**

Return value indicating whether the addition was successful or not.
