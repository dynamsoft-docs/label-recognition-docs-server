---
layout: default-layout
title: CTextLineResultItem - Dynamsoft Label Recognizer Classes
description: The class CTextLineResultItem of Dynamsoft Label Recognizer represents a text line result item recognized by a document layout analysis engine.
keywords: Text line result item
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CTextLineResultItem
---

# CTextLineResultItem

The `CTextLineResultItem` class represents a text line result item recognized by the library. It is derived from `CCapturedResultItem`.

## Definition

*Namespace:* dynamsoft::dlr

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CTextLineResultItem : public CCapturedResultItem
```

*Inheritance:* [CCapturedResultItem]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html) -> CTextLineResultItem

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetText`](#gettext) | Gets the text content of the text line. |
| [`GetLocation`](#getlocation) | Gets the location of the text line in the form of a quadrilateral. |
| [`GetConfidence`](#getconfidence) | Gets the confidence of the text line recognition result. |
| [`GetCharacterResultsCount`](#getcharacterresultscount) | Gets the count of character results in the text line. |
| [`GetCharacterResult`](#getcharacterresult) | Gets the character result at the specified index. |
| [`GetSpecificationName`](#getspecificationname) | Gets the name of the text line specification that generated this element. |
| [`GetRawText`](#getrawtext) | Gets the recognized raw text, excluding any concatenation separators. |
| [`SetLocation`](#setlocation) | Set the location of the text line item. |
| **Methods Inherited from [CCapturedResultItem]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html):** | |
| [`GetType`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#gettype) | Gets the type of the captured result item. |
| [`GetReferenceItem`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#getreferenceitem) | Gets a pointer to the referenced item in the captured result. |
| [`GetTargetROIDefName`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#gettargetroidefname) | Gets the name of the target ROI definition. |
| [`GetTaskName`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#gettaskname) | Gets the name of the task. |
| [`Retain`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#retain) | Increases the reference count of the `CCapturedResultItem` object. |
| [`Release`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#release) | Decreases the reference count of the `CCapturedResultItem` object. |
| [`Clone`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#clone) | Clone the captured result item. |

### SetLocation

Set the location of the text line item.

```cpp
virtual int SetLocation(const CQuadrilateral& location) = 0;
```

**Parameters**

`[in] location` The location of the text line item.

**Return value**

Returns 0 if success, otherwise an error code.

### GetText

It is used to get the text content of the text line.

```cpp
virtual const char* GetText() const = 0;
```

**Return value**

Returns the text content of the text line.

### GetLocation

It is used to get the location of the text line in the form of a quadrilateral.

```cpp
virtual CQuadrilateral GetLocation() const = 0;
```

**Return value**

Returns the location of the text line in the form of a quadrilateral.

### GetConfidence

It is used to get the confidence of the text line recognition result.

```cpp
virtual int GetConfidence() const = 0;
```

**Return value**

Returns the confidence of the text line recognition result.

### GetCharacterResultsCount

It is used to get the count of character results in the text line.

```cpp
virtual int GetCharacterResultsCount() const = 0;
```

**Return value**

Returns the count of character results in the text line.

### GetCharacterResult

It is used to get the character result at the specified index.

```cpp
virtual const CCharacterResult* GetCharacterResult(int index) const = 0;
```

**Parameters**

`[in] index` The index of the character result to get.

**Return value**

Returns the character result at the specified index.

### GetSpecificationName

Gets the name of the text line specification that generated this item.

```cpp
virtual const char* GetSpecificationName() const = 0;
```

**Return value**

Returns the name of the text line specification that generated this item.

### GetRawText

Gets the recognized raw text, excluding any concatenation separators.

```cpp
virtual const char* GetRawText() const = 0;
```

**Return value**

Returns a pointer to the recognized raw text.
