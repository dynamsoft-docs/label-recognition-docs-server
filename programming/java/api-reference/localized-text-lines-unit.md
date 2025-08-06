---
layout: default-layout
title: LocalizedTextLinesUnit - Dynamsoft Label Recognizer Classes
description: The class LocalizedTextLinesUnit of Dynamsoft Label Recognizer represents a unit that contains localized text lines.
keywords: Localized text lines unit
---

# LocalizedTextLinesUnit

The `LocalizedTextLinesUnit` class represents a unit that contains localized text lines. It inherits from the `IntermediateResultUnit` class.

## Definition

*Package:* com.dynamsoft.dlr.intermediate_results

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html) -> LocalizedTextLinesUnit

```java
public class LocalizedTextLinesUnit extends IntermediateResultUnit
```

## Methods

| Method                            | Description |
|-----------------------------------|-------------|
| [`getCount`](#getcount)           | Gets the number of localized text lines in the unit.|
| [`getLocalizedTextLine`](#getlocalizedtextline) | Gets a localized text line element.|
| [`getLocalizedTextLines`](#getlocalizedtextlines) | Gets all localized text line elements.|
| [`removeAllLocalizedTextLines`](#removealllocalizedtextlines) | Removes all localized text lines.|
| [`removeLocalizedTextLine`](#removelocalizedtextline) | Removes the localized text line at the specified index.|
| [`addLocalizedTextLine`](#addlocalizedtextline) | Adds a localized text line.|
| [`setLocalizedTextLine`](#setlocalizedtextline) | Sets the localized text line at the specified index.|

### getCount

Gets the number of localized text lines in the unit.

```java
public int getCount()
```

**Return value**

Returns the number of localized text lines in the unit.

### getLocalizedTextLine

Gets a localized text line element.

```java
public LocalizedTextLineElement getLocalizedTextLine(int index)
```

**Parameters**

`index` The index of the localized text line element to retrieve.

**Return value**

Returns the localized text line element at the specified index.

**See Also**

[LocalizedTextLineElement]({{ site.dlr_java_api }}localized-text-line-element.html)

### getLocalizedTextLines

Gets all localized text line elements.

```java
public LocalizedTextLineElement[] getLocalizedTextLines()
```

**Return value**

Returns an array of localized text line elements.

**See Also**

[LocalizedTextLineElement]({{ site.dlr_java_api }}localized-text-line-element.html)

### removeAllLocalizedTextLines

Removes all localized text lines.

```java
public void removeAllLocalizedTextLines()
```

### removeLocalizedTextLine

Removes the localized text line at the specified index.

```java
public void removeLocalizedTextLine(int index) throws LabelRecognizerException
```

**Parameters**

`index` The index of the localized text line to remove.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

### addLocalizedTextLine

Adds a localized text line.

```java
public void addLocalizedTextLine(LocalizedTextLineElement element) throws LabelRecognizerException
public void addLocalizedTextLine(LocalizedTextLineElement element, double[] matrixToOriginalImage) throws LabelRecognizerException
```

**Parameters**

`element` The localized text line element to add.
`matrixToOriginalImage` The transformation matrix to the original image (optional).

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

**See Also**

[LocalizedTextLineElement]({{ site.dlr_java_api }}localized-text-line-element.html)

### setLocalizedTextLine

Sets the localized text line at the specified index.

```java
public void setLocalizedTextLine(int index, LocalizedTextLineElement element) throws LabelRecognizerException
public void setLocalizedTextLine(int index, LocalizedTextLineElement element, double[] matrixToOriginalImage) throws LabelRecognizerException  
```

**Parameters**

`index` The index where to set the localized text line.
`element` The localized text line element to set.
`matrixToOriginalImage` The transformation matrix to the original image (optional).

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

**See Also**

[LocalizedTextLineElement]({{ site.dlr_java_api }}localized-text-line-element.html)

`matrix_to_original_image` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[LocalizedTextLineElement]({{ site.dlr_java_api }}localized-text-line-element.html)
