---
layout: default-layout
title: RawTextLine - Dynamsoft Label Recognizer Classes
description: The class RawTextLine of Dynamsoft Label Recognizer represents a recognized raw text line.
keywords: Recognized raw text line
---

# RawTextLine

The class `RawTextLine` represents a recognized raw text line in an image. It can be in one of the following states:

* `RTLS_LOCALIZED`: Localized but recognition not performed.
* `RTLS_RECOGNITION_FAILED`: Recognition failed.
* `RTLS_RECOGNITION_SUCCEEDED`: Successfully recognized.

## Definition

*Package:* com.dynamsoft.dlr.intermediate_results

```java
public class RawTextLine
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`RawTextLine`](#rawtextline) | Initializes a new instance of the `RawTextLine` class. |
| [`getText`](#gettext) | Gets the recognized text.|
| [`getConfidence`](#getconfidence) | Gets the confidence level of the recognized text.|
| [`getCharacterResultsCount`](#getcharacterresultscount) | Gets the number of individual character recognition results in the line.|
| [`getCharacterResult`](#getcharacterresult) | Gets the character recognition result at the specified index.|
| [`getCharacterResults`](#getcharacterresults) | Gets all character recognition results in the line.|
| [`getLocation`](#getlocation) | Gets the location of the text line.|
| [`getRowNumber`](#getrownumber) | Gets the row number of the text line within the image.|
| [`getSpecificationName`](#getspecificationname) | Gets the name of the text line specification that generated this element.|
| [`getStatus`](#getstatus) | Gets the status of the text line.|
| [`setText`](#settext) | Sets the recognized text.|
| [`setLocation`](#setlocation) | Sets the location of the text line.|
| [`setRowNumber`](#setrownumber) | Sets the row number of the text line within the image.|
| [`setSpecificationName`](#setspecificationname) | Sets the name of the text line specification that generated this element. |
| [`setCharacterResults`](#setcharacterresults) | Sets the character recognition results for the text line. |
| [`clone`](#clone) | Clones the `RawTextLine` object.|

### RawTextLine

Initializes a new instance of the `RawTextLine` class.

```java
public RawTextLine()
```

### getText

Gets the recognized text.

```java
public String getText()
```

**Return value**

Returns the recognized text.

### getConfidence

Gets the confidence level of the recognized text.

```java
public int getConfidence()
```

**Return value**

Returns an integer value representing the confidence level of the recognized text.

### getCharacterResultsCount

Gets the number of individual character recognition results in the line.

```java
public int getCharacterResultsCount()
```

**Return value**

Returns an integer value representing the number of individual character recognition results.

### getCharacterResult

Gets the character recognition result at the specified index.

```java
public CharacterResult getCharacterResult(int index)
```

**Parameters**

`index` The index of the character recognition result to retrieve.

**Return value**

Returns the character recognition result.

**See Also**

[CharacterResult]({{ site.dlr_java_api }}character-result.html)

### getCharacterResults

Gets all character recognition results in the line.

```java
public CharacterResult[] getCharacterResults()
```

**Return value**

Returns an array of character recognition results.

**See Also**

[CharacterResult]({{ site.dlr_java_api }}character-result.html)

### getLocation

Gets the location of the text line.

```java
public Quadrilateral getLocation()
```

**Return value**

Returns a `Quadrilateral` object which represents the location of the text line.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### getRowNumber

Gets the row number of the text line within the image.

```java
public int getRowNumber()
```

**Return value**

Returns an integer value representing the row number of the text line within the image.

### getSpecificationName

Gets the name of the text line specification that generated this element.

```java
public String getSpecificationName()
```

**Return value**

Returns the name of the text line specification.

### getStatus

Gets the status of the text line.

```java
public @EnumRawTextLineStatus int getStatus()
```

**Return value**

Returns the status of the text line.

**See Also**

[EnumRawTextLineStatus]({{ site.dlr_java_api }}enum-raw-text-line-status.html)

### setText

Sets the recognized text.

```java
public void setText(String text)
```

**Parameters**

`text` The text to set.

### setLocation

Sets the location of the text line.

```java
public void setLocation(Quadrilateral location) throws LabelRecognizerException
```

**Parameters**

`location` The location of the text line as a Quadrilateral object.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### setRowNumber

Sets the row number of the text line within the image.

```java
public void setRowNumber(int rowNumber) throws LabelRecognizerException
```

**Parameters**

`rowNumber` The row number to set.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

### setSpecificationName

Sets the name of the text line specification that generated this element.

```java
public void setSpecificationName(String specificationName) throws LabelRecognizerException
```

**Parameters**

`specificationName` The specification name to set.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

### setCharacterResults

Sets the character recognition results for the text line.

```java
public void setCharacterResults(CharacterResult[] characterResults) throws LabelRecognizerException
```

**Parameters**

`characterResults` An array of character recognition results.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

**See Also**

[CharacterResult]({{ site.dlr_java_api }}character-result.html)

### clone

Clones the `RawTextLine` object.

```java
public RawTextLine clone()
```

**Return value**

Returns a cloned `RawTextLine` object.

```java
public int getCharacterResultsCount()
```

**Return value**

Returns an integer value representing the number of individual character recognition results.

### getCharacterResult

Gets the character recognition result at the specified index.

```java
public CharacterResult getCharacterResult(int index)
```

**Parameters**

`index` The index of the character recognition result to retrieve.

**Return value**

Returns the character recognition result.

**See Also**

[CharacterResult]({{ site.dlr_java_api }}character-result.html)

### getCharacterResults

Gets all character recognition results in the line.

```java
public CharacterResult[] getCharacterResults()
```

**Return value**

Returns an array of character recognition results.

**See Also**

[CharacterResult]({{ site.dlr_java_api }}character-result.html)

### getLocation

Gets the location of the text line.

```java
public Quadrilateral getLocation()
```

**Return value**

Returns a `Quadrilateral` object which represents the location of the text line.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### getRowNumber

Gets the row number of the text line within the image.

```java
public int getRowNumber()
```

**Return value**

Returns an integer value representing the row number of the text line within the image.

### getSpecificationName

Gets the name of the text line specification that generated this element.

```java
public String getSpecificationName()
```

**Return value**

Returns the name of the text line specification.

### getStatus

Gets the status of the text line.

```java
public @EnumRawTextLineStatus int getStatus()
```

**Return value**

Returns the status of the text line.

**See Also**

[EnumRawTextLineStatus]({{ site.dlr_java_api }}enum-raw-text-line-status.html)

### setText

Sets the recognized text.

```java
public void setText(String text)
```

**Parameters**

`text` The text to set.

### setLocation

Sets the location of the text line.

```java
public void setLocation(Quadrilateral location) throws LabelRecognizerException
```

**Parameters**

`location` The location of the text line as a Quadrilateral object.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### setRowNumber

Sets the row number of the text line within the image.

```java
public void setRowNumber(int rowNumber) throws LabelRecognizerException
```

**Parameters**

`rowNumber` The row number to set.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

### setSpecificationName

Sets the name of the text line specification that generated this element.

```java
public void setSpecificationName(String specificationName) throws LabelRecognizerException
```

**Parameters**

`specificationName` The specification name to set.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

### setCharacterResults

Sets the character recognition results for the text line.

```java
public void setCharacterResults(CharacterResult[] characterResults) throws LabelRecognizerException
```

**Parameters**

`characterResults` An array of character recognition results.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

**See Also**

[CharacterResult]({{ site.dlr_java_api }}character-result.html)

### clone

Clones the `RawTextLine` object.

```java
public RawTextLine clone()
```

**Return value**

Returns a cloned `RawTextLine` object.
