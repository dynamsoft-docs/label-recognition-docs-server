---
layout: default-layout
title: CRecognizedTextLinesResultArray - Dynamsoft Label Recognizer Classes
description: The class CRecognizedTextLinesResultArray of Dynamsoft Label Recognizer represents an array of recognized text lines.
keywords: Recognized text lines result array
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CRecognizedTextLinesResultArray
permalink: /programming/cplusplus/api-reference/recognized-text-lines-result-array.html
---

# CRecognizedTextLinesResultArray

The `CRecognizedTextLinesResultArray` class represents an array of recognized text lines. It is an abstract class that provides an interface for accessing the results.

## Definition

*Namespace:* dynamsoft::dlr

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CRecognizedTextLinesResultArray
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the number of recognized text lines in the array.|
| [`GetResult`](#getresult) | Gets the recognized text line at the specified index. |

### GetCount

It is used to get the number of recognized text lines in the array.

```cpp
virtual int GetCount() const = 0;
```

**Return value**

Returns the number of recognized text lines in the array.

### GetResult

It is used to get the recognized text line at the specified index.

```cpp
virtual const CRecognizedTextLinesResult* GetResult(int index) const = 0;
```

**Parameters**

`[in] index` The index of the recognized text line to retrieve.

**Return value**

Returns a pointer to the CRecognizedTextLinesResult object at the specified index.
