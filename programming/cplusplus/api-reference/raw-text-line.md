
---
layout: default-layout
title: CRawTextLine - Dynamsoft Label Recognizer Classes
description: The class CRawTextLine of Dynamsoft Label Recognizer represents a recognized raw text line.
keywords: Recognized raw text line
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CRawTextLine
---

# CRawTextLine

The class `CRawTextLine` of Dynamsoft Label Recognizer represents a recognized raw text line in an image. It can be in one of the following states:

* `RTLS_LOCALIZED`: Localized but recognition not performed.
* `RTLS_RECOGNITION_FAILED`: Recognition failed.
* `RTLS_RECOGNITION_SUCCEEDED`: Successfully recognized.

## Definition

*Namespace:* dynamsoft::dlr::intermediate_results

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CRawTextLine
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetText`](#gettext) | Gets the recognized text.|
| [`GetConfidence`](#getconfidence) | Gets the confidence level of the recognized text.|
| [`GetCharacterResultsCount`](#getcharacterresultscount) | Gets the number of individual character recognition results in the line.|
| [`GetCharacterResult`](#getcharacterresult) | Gets the character recognition result at the specified index.|
| [`GetLocation`](#getlocation) | Gets the location of the text line.|
| [`GetRowNumber`](#getrownumber) | Gets the row number of the text line within the image.|
| [`GetSpecificationName`](#getspecificationname) | Gets the name of the text line specification that generated this element.|
| [`GetStatus`](#getstatus) | Gets the status of the text line.|
| [`SetText`](#settext) | Sets the recognized text.|
| [`SetLocation`](#setlocation) | Set the location of the text line.|
| [`SetRowNumber`](#setrownumber) | Set the row number of the text line within the image.|
| [`SetSpecificationName`](#setspecificationname) | Sets the name of the text line specification that generated this element.
| [`Release`](#release) | Decreases the reference count of the CRawTextLine object.|
| [`Clone`](#clone) | Clone the CRawTextLine object.|
| [`SetCharacterResults`](#setcharacterresults) | Sets the character recognition results.|

### GetText

Gets the recognized text.

```cpp
const char* GetText() const
```

**Return value**

Returns a pointer to the recognized text.

### GetConfidence

Gets the confidence level of the recognized text.

```cpp
int GetConfidence() const
```

**Return value**

Returns an integer value representing the confidence level of the recognized text.

### GetCharacterResultsCount

Gets the number of individual character recognition results in the line.

```cpp
int GetCharacterResultsCount() const
```

**Return value**

Returns an integer value representing the number of individual character recognition results.

### GetCharacterResult

Gets the character recognition result at the specified index.

```cpp
const CCharacterResult* GetCharacterResult(int index) const
```

**Parameters**

`[in] index` The index of the character recognition result to retrieve.

**Return value**

Returns a pointer to the character recognition result.

### GetLocation

Gets the location of the text line.

```cpp
CQuadrilateral GetLocation() const
```

**Return value**

Returns a CQuadrilateral object which represents the location of the text line.

### GetRowNumber

Gets the row number of the text line within the image.

```cpp
int GetRowNumber() const
```

**Return value**

Returns an integer value representing the row number of the text line within the image.

### GetSpecificationName

Gets the name of the text line specification that generated this element.

```cpp
const char* GetSpecificationName() const
```

**Return value**

Returns the name of the text line specification.

### GetStatus

Gets the status of the text line.

```cpp
RawTextLineStatus GetStatus() const
```

**Return value**

Returns the status of the text line.

**See also**

* [RawTextLineStatus](enum-raw-text-line-status.md)

### SetText

Sets the recognized text.

```cpp
void SetText(const char* text)
```

**Parameters**

`[in] text` The text to be set.


### SetLocation

Set the location of the text line.

```cpp
int SetLocation(const CQuadrilateral& location)
```

**Parameters**

`[in] location` The location of the text line.

** Return value**

Returns 0 if successful; otherwise returns an error code.

### SetRowNumber

Set the row number of the text line within the image.

```cpp
void SetRowNumber(int rowNumber)
```

**Parameters**

`[in] rowNumber` The row number of the text line within the image.

### SetSpecificationName

Sets the name of the text line specification that generated this element.

```cpp
void SetSpecificationName(const char* specificationName)
```

**Parameters**

`[in] specificationName` The name of the text line specification.

### Release

Decreases the reference count of the CRawTextLine object.

```cpp
void Release()
```

### Clone

Clone the CRawTextLine object.

```cpp
CRawTextLine* Clone() const
```

**Return value**

Returns a pointer to the cloned CRawTextLine object.

**Remarks**

Don't forget to call `Release` after you have finished using the cloned CRawTextLine object.

### SetCharacterResults

Sets the character recognition results.

```cpp
int SetCharacterResults(const CCharacterResult* charArray, int charArrayLength)
```

**Parameters**

`[in] charArray` The character result array.

`[in] charArrayLength` The length of the character result array.

**Return value**

Returns 0 if successful; otherwise returns an error code.