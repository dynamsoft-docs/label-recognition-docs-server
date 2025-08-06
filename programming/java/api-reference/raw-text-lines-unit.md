---
layout: default-layout
title: RawTextLinesUnit - Dynamsoft Label Recognizer Classes
description: The class RawTextLinesUnit of Dynamsoft Label Recognizer represents a unit that contains recognized raw text lines.
keywords: Recognized raw text lines unit
---

# RawTextLinesUnit

The `RawTextLinesUnit` class represents an intermediate result unit containing raw text lines. It inherits from the `IntermediateResultUnit` class.

## Definition

*Package:* com.dynamsoft.dlr.intermediate_results

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html) -> RawTextLinesUnit

```java
public class RawTextLinesUnit extends IntermediateResultUnit
```

## Methods

| Method | Description |
|--------|-------------|
| [`getCount`](#getcount) | Gets the number of raw text lines in the unit.|
| [`getRawTextLine`](#getrawtextline) | Gets a raw text line.|
| [`getRawTextLines`](#getrawtextlines) | Gets all raw text lines.|
| [`removeAllRawTextLines`](#removeallrawtextlines) | Removes all raw text lines.|
| [`removeRawTextLine`](#removerawtextline) | Removes the raw text line at the specified index.|
| [`addRawTextLine`](#addrawtextline) | Adds a raw text line.|
| [`setRawTextLine`](#setrawtextline) | Sets the raw text line at the specified index.|

### getCount

Gets the number of raw text lines in the unit.

```java
public int getCount()
```

**Return value**

Returns the number of raw text lines in the unit.

### getRawTextLine

Gets a raw text line.

```java
public RawTextLine getRawTextLine(int index)
```

**Parameters**

`index` The index of the raw text line to retrieve.

**Return value**

Returns the raw text line at the specified index.

**See Also**

[RawTextLine]({{ site.dlr_java_api }}raw-text-line.html)

### getRawTextLines

Gets all raw text lines.

```java
public RawTextLine[] getRawTextLines()
```

**Return value**

Returns an array of raw text lines.

**See Also**

[RawTextLine]({{ site.dlr_java_api }}raw-text-line.html)

### removeAllRawTextLines

Removes all raw text lines.

```java
public void removeAllRawTextLines()
```

### removeRawTextLine

Removes the raw text line at the specified index.

```java
public void removeRawTextLine(int index)
```

**Parameters**

`index` The index of the raw text line to remove.

### addRawTextLine

Adds a raw text line.

```java
public void addRawTextLine(RawTextLine textLine)
public void addRawTextLine(RawTextLine textLine, double[] matrixToOriginalImage)
```

**Parameters**

`textLine` The raw text line to add.
`matrixToOriginalImage` The transformation matrix to the original image (optional).

**See Also**

[RawTextLine]({{ site.dlr_java_api }}raw-text-line.html)

### setRawTextLine

Sets the raw text line at the specified index.

```java
public void setRawTextLine(int index, RawTextLine textLine)
public void setRawTextLine(int index, RawTextLine textLine, double[] matrixToOriginalImage)
```

**Parameters**

`index` The index of the raw text line to set.
`textLine` The raw text line to set.
`matrixToOriginalImage` The transformation matrix to the original image (optional).

**See Also**

[RawTextLine]({{ site.dlr_java_api }}raw-text-line.html)
