---
layout: default-layout
title: RecognizedTextLinesResult Class - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: Definition of the RecognizedTextLinesResult class in Dynamsoft Label Recognizer Module .NET Edition.
keywords: Recognized text lines result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RecognizedTextLinesResult

The `RecognizedTextLinesResult` class represents the result of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Namespace:* Dynamsoft.DLR

*Assembly:* Dynamsoft.LabelRecognizer.dll

```csharp
public class RecognizedTextLinesResult
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image. |
| [`GetItems`](#getitems) | Gets all the text line result items. |
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`GetErrorCode`](#geterrorcode) | Gets the error code of the recognition result, if an error occurred. |
| [`GetErrorString`](#geterrorstring) | Gets the error message of the recognition result, if an error occurred. |

### GetOriginalImageHashId

Gets the hash ID of the original image.

```csharp
string GetOriginalImageHashId()
```

**Return Value**

Returns a string containing the hash ID of the original image.

### GetOriginalImageTag

Gets the tag of the original image.

```csharp
ImageTag GetOriginalImageTag()
```

**Return Value**

Returns an `ImageTag` object representing the tag of the original image.

**See Also**

[ImageTag]({{ site.dcv_dotnet_api }}core/basic-classes/image-tag.html)

### GetItems

Gets all the text line result items.

```csharp
TextLineResultItem GetItems()
```

**Return Value**

Returns a `TextLineResultItem` array.

**See Also**

[TextLineResultItem]({{ site.dlr_dotnet_api }}text-line-result-item.html)

### GetRotationTransformMatrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```csharp
double[] GetRotationTransformMatrix()
```

**Return Value**

Returns a double array of length 9 which represents a 3x3 rotation matrix.

### GetErrorCode

Gets the error code of the recognition result, if an error occurred.

```csharp
int GetErrorCode()
```

**Return Value**

Returns the error code of the recognition result, or 0 if no error occurred.

**See Also**

[EnumErrorCode]({{ site.dcv_enumerations }}core/error-code.html?lang=dotnet)

### GetErrorString

Gets the error message of the recognition result, if an error occurred.

```csharp
string GetErrorString()
```

**Return Value**

Returns a string containing the error message of the recognition result, or an empty string if no error occurred.

