---
layout: default-layout
title: CRecognizedTextLineElement - Dynamsoft Label Recognizer Classes
description: The class CRecognizedTextLineElement of Dynamsoft Label Recognizer represents a line of recognized text in an image.
keywords: Recognized text line element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CRecognizedTextLineElement
---

# CRecognizedTextLineElement

The `CRecognizedTextLineElement` class represents a line of recognized text in an image. It inherits from the `CRegionObjectElement` class.

## Definition

*Namespace:* dynamsoft::dlr::intermediate_results

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CRecognizedTextLineElement : public CRegionObjectElement
```

*Inheritance:* [CRegionObjectElement]({{ site.dcvb_cpp_api }}core/intermediate-results/region-object-element.html) -> CRecognizedTextLineElement

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetText`](#gettext) | Gets the recognized text. |
| [`GetConfidence`](#getconfidence) | Gets the confidence level of the recognized text. |
| [`GetCharacterResultsCount`](#getcharacterresultscount) | Gets the number of individual character recognition results in the line. |
| [`GetCharacterResult`](#getcharacterresult) | Gets the character recognition result at the specified index. |
| [`GetRowNumber`](#getrownumber) | Gets the row number of the text line within the image. |
| [`GetSpecificationName`](#getspecificationname) | Gets the name of the text line specification that generated this element. |
| [`GetRawText`](#getrawtext) | Gets the recognized raw text, excluding any concatenation separators. |

### GetText

Gets the recognized text.

```cpp
virtual const char* GetText() const = 0;
```

**Return value**

Returns a pointer to the recognized text.

### GetConfidence

Gets the confidence level of the recognized text.

```cpp
virtual int GetConfidence() const = 0;
```

**Return value**

Returns an integer value representing the confidence level of the recognized text.

### GetCharacterResultsCount

Gets the number of individual character recognition results in the line.

```cpp
virtual int GetCharacterResultsCount() const = 0;
```

**Return value**

Returns an integer value representing the number of individual character recognition results.

### GetCharacterResult

Gets the character recognition result at the specified index.

```cpp
virtual const CCharacterResult* GetCharacterResult(int index) const = 0;
```

**Parameters**

`[in] index` The index of the character recognition result to retrieve.

**Return value**

Returns a pointer to a CCharacterResult object to store the result in.

### GetRowNumber

Gets the row number of the text line within the image.

```cpp
virtual int GetRowNumber() const = 0;
```

**Return value**

Returns an integer value representing the row number of the text line within the image.

### GetSpecificationName

Gets the name of the text line specification that generated this element.

```cpp
virtual const char* GetSpecificationName() const = 0;
```

**Return value**

Returns the name of the text line specification that generated this element.

### GetRawText

Gets the recognized raw text, excluding any concatenation separators.

```cpp
virtual const char* GetRawText() const = 0;
```

**Return value**

Returns a pointer to the recognized raw text.
