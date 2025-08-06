---
layout: default-layout
title: RecognizedTextLinesResult Class - Dynamsoft Label Recognizer Module Java Edition API Reference
description: Definition of the RecognizedTextLinesResult class in Dynamsoft Label Recognizer Module Java Edition.
keywords: Recognized text lines result
---

# RecognizedTextLinesResult

The `RecognizedTextLinesResult` class represents the result of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Package:* com.dynamsoft.dlr

*Inheritance:* [CapturedResultBase]({{ site.dcvb_java_api }}core/basic-classes/captured-result-base.html) -> RecognizedTextLinesResult

```java
public class RecognizedTextLinesResult extends CapturedResultBase
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`getOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image. |
| [`getItems`](#getitems) | Gets all the text line result items. |
| [`getItem`](#getitem) | Gets the text line result item at a specific index. |
| [`getItemsCount`](#getitemscount) | Gets the count of text line result items. |
| [`getRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`getErrorCode`](#geterrorcode) | Gets the error code of the recognition result, if an error occurred. |
| [`getErrorString`](#geterrorstring) | Gets the error message of the recognition result, if an error occurred. |

### getOriginalImageHashId

Gets the hash ID of the original image.

```java
public String getOriginalImageHashId()
```

**Return Value**

Returns a string containing the hash ID of the original image.

### getOriginalImageTag

Gets the tag of the original image.

```java
public ImageTag getOriginalImageTag()
```

**Return Value**

Returns an `ImageTag` object representing the tag of the original image.

**See Also**

[ImageTag]({{ site.dcvb_java_api }}core/basic-classes/image-tag.html)

### getItems

Gets all the text line result items.

```java
public TextLineResultItem[] getItems()
```

**Return Value**

Returns a `TextLineResultItem` array.

**See Also**

[TextLineResultItem]({{ site.dlr_java_api }}text-line-result-item.html)

### getItem

Gets the text line result item at a specific index.

```java
public TextLineResultItem getItem(int index)
```

**Parameters**

`index` The index of the text line result item to retrieve.

**Return Value**

Returns the `TextLineResultItem` at the specified index.

**See Also**

[TextLineResultItem]({{ site.dlr_java_api }}text-line-result-item.html)

### getItemsCount

Gets the count of text line result items.

```java
public int getItemsCount()
```

**Return Value**

Returns the count of text line result items.

### getRotationTransformMatrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```java
public float[] getRotationTransformMatrix()
```

**Return Value**

Returns a float array of length 9 which represents a 3x3 rotation matrix.

### getErrorCode

Gets the error code of the recognition result, if an error occurred.

```java
public int getErrorCode()
```

**Return Value**

Returns the error code of the recognition result, or 0 if no error occurred.

### getErrorString

Gets the error message of the recognition result, if an error occurred.

```java
public String getErrorString()
```

**Return Value**

Returns the error message of the recognition result, or an empty string if no error occurred.

**See Also**

[EnumErrorCode]({{ site.dcvb_java_api }}core/enum-error-code.html)

