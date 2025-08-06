---
layout: default-layout
title: RecognizedTextLinesUnit - Dynamsoft Label Recognizer Classes
description: The class RecognizedTextLinesUnit of Dynamsoft Label Recognizer represents an intermediate result unit containing recognized text lines.
keywords: Recognized text lines unit
---

# RecognizedTextLinesUnit

The `RecognizedTextLinesUnit` class represents an intermediate result unit containing recognized text lines. It inherits from the `IntermediateResultUnit` class.

## Definition

*Package:* com.dynamsoft.dlr.intermediate_results

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html) -> RecognizedTextLinesUnit

```java
public class RecognizedTextLinesUnit extends IntermediateResultUnit
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`getCount`](#getcount) | Gets the number of recognized text lines in the unit.|
| [`getRecognizedTextLine`](#getrecognizedtextline) | Gets the RecognizedTextLineElement object at the specified index. |
| [`getRecognizedTextLines`](#getrecognizedtextlines) | Gets all RecognizedTextLineElement objects in the unit. |
| [`removeAllRecognizedTextLines`](#removeallrecognizedtextlines) | Removes all recognized text lines. |
| [`removeRecognizedTextLine`](#removerecognizedtextline) | Removes the recognized text line at the specified index. |
| [`addRecognizedTextLine`](#addrecognizedtextline) | Adds a recognized text line. |
| [`setRecognizedTextLine`](#setrecognizedtextline) | Sets the recognized text line at the specified index. |

### getCount

Gets the number of recognized text lines in the unit.

```java
public int getCount()
```

**Return value**

Returns the number of recognized text lines in the unit.

### getRecognizedTextLine

Gets the RecognizedTextLineElement object at the specified index.

```java
public RecognizedTextLineElement getRecognizedTextLine(int index)
```

**Parameters**

`index` The index of the recognized text line element to retrieve.

**Return value**

Returns the RecognizedTextLineElement object at the specified index.

**See Also**

[RecognizedTextLineElement]({{ site.dlr_java_api }}recognized-text-line-element.html)

### getRecognizedTextLines

Gets all RecognizedTextLineElement objects in the unit.

```java
public RecognizedTextLineElement[] getRecognizedTextLines()
```

**Return value**

Returns an array of RecognizedTextLineElement objects.

**See Also**

[RecognizedTextLineElement]({{ site.dlr_java_api }}recognized-text-line-element.html)

### removeAllRecognizedTextLines

Removes all recognized text lines.

```java
public void removeAllRecognizedTextLines()
```

### removeRecognizedTextLine

Removes the recognized text line at the specified index.

```java
public void removeRecognizedTextLine(int index) throws LabelRecognizerException
```

**Parameters**

`index` The index of the recognized text line to remove.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

### addRecognizedTextLine

Adds a recognized text line.

```java
public void addRecognizedTextLine(RecognizedTextLineElement element) throws LabelRecognizerException
public void addRecognizedTextLine(RecognizedTextLineElement element, double[] matrixToOriginalImage) throws LabelRecognizerException
```

**Parameters**

`element` The recognized text line element to add.
`matrixToOriginalImage` The transformation matrix to the original image (optional).

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

**See Also**

[RecognizedTextLineElement]({{ site.dlr_java_api }}recognized-text-line-element.html)

### setRecognizedTextLine

Sets the recognized text line at the specified index.

```java
public void setRecognizedTextLine(int index, RecognizedTextLineElement element) throws LabelRecognizerException
public void setRecognizedTextLine(int index, RecognizedTextLineElement element, double[] matrixToOriginalImage) throws LabelRecognizerException  
```

**Parameters**

`index` The index where to set the recognized text line.
`element` The recognized text line element to set.
`matrixToOriginalImage` The transformation matrix to the original image (optional).

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

**See Also**

[RecognizedTextLineElement]({{ site.dlr_java_api }}recognized-text-line-element.html)
