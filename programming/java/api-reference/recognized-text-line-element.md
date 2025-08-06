---
layout: default-layout
title: RecognizedTextLineElement - Dynamsoft Label Recognizer Classes
description: The class RecognizedTextLineElement of Dynamsoft Label Recognizer represents a line of recognized text in an image.
keywords: Recognized text line element
---

# RecognizedTextLineElement

The `RecognizedTextLineElement` class represents a line of recognized text in an image. It inherits from the `RegionObjectElement` class.

## Definition

*Package:* com.dynamsoft.dlr.intermediate_results

*Inheritance:* [RegionObjectElement]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html) -> RecognizedTextLineElement

```java
public class RecognizedTextLineElement extends RegionObjectElement
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`RecognizedTextLineElement`](#recognizedtextlineelement) | Initializes a new instance of the `RecognizedTextLineElement` class. |
| [`getText`](#gettext) | Gets the recognized text. |
| [`getConfidence`](#getconfidence) | Gets the confidence level of the recognized text. |
| [`getCharacterResultsCount`](#getcharacterresultscount) | Gets the number of individual character recognition results in the line. |
| [`getCharacterResult`](#getcharacterresult) | Gets the character recognition result at the specified index. |
| [`getCharacterResults`](#getcharacterresults) | Gets all character recognition results in the line. |
| [`getRowNumber`](#getrownumber) | Gets the row number of the text line within the image. |
| [`getSpecificationName`](#getspecificationname) | Gets the name of the text line specification that generated this element. |
| [`getRawText`](#getrawtext) | Gets the recognized raw text, excluding any concatenation separators. |
| [`setText`](#settext) | Sets the recognized text. |

### RecognizedTextLineElement

Initializes a new instance of the `RecognizedTextLineElement` class.

```java
public RecognizedTextLineElement()
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

Returns a `CharacterResult` object.

**See Also**

[CharacterResult]({{ site.dlr_java_api }}character-result.html)

### getCharacterResults

Gets all character recognition results in the line.

```java
public CharacterResult[] getCharacterResults()
```

**Return value**

Returns an array of `CharacterResult` objects.

**See Also**

[CharacterResult]({{ site.dlr_java_api }}character-result.html)

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

### getRawText

Gets the recognized raw text, excluding any concatenation separators.

```java
public String getRawText()
```

**Return value**

Returns the recognized raw text.

### setText

Sets the recognized text.

```java
public void setText(String text) throws LabelRecognizerException
```

**Parameters**

`text` The text to set.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

