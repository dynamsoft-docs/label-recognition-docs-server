---
layout: default-layout
title: TextLineResultItem Class - Dynamsoft Label Recognizer Module Java Edition API Reference
description: Definition of the TextLineResultItem class in Dynamsoft Label Recognizer Module Java Edition.
keywords: Text line result item
---

# TextLineResultItem

The `TextLineResultItem` class represents a text line result item recognized by the library. It is derived from `CapturedResultItem`.

## Definition

*Package:* com.dynamsoft.dlr

*Inheritance:* [CapturedResultItem]({{ site.dcvb_java_api }}core/basic-classes/captured-result-item.html) -> TextLineResultItem

```java
public class TextLineResultItem extends CapturedResultItem
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getText`](#gettext) | Gets the text content of the text line. |
| [`getLocation`](#getlocation) | Gets the location of the text line in the form of a quadrilateral. |
| [`getConfidence`](#getconfidence) | Gets the confidence of the text line recognition result. |
| [`getCharacterResults`](#getcharacterresults) | Gets all the character results. |
| [`getCharacterResult`](#getcharacterresult) | Gets the character result at a specific index. |
| [`getCharacterResultsCount`](#getcharacterresultscount) | Gets the count of character results. |
| [`getSpecificationName`](#getspecificationname) | Gets the name of the text line specification that generated this item. |
| [`getRawText`](#getrawtext) | Gets the recognized raw text, excluding any concatenation separators. |

### getText

Gets the text content of the text line.

```java
public String getText()
```

**Return Value**

Returns the text content of the text line.

### getLocation

Gets the location of the text line in the form of a quadrilateral.

```java
public Quadrilateral getLocation()
```

**Return Value**

Returns the location of the text line in the form of a quadrilateral.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### getConfidence

Gets the confidence of the text line recognition result.

```java
public int getConfidence()
```

**Return Value**

Returns the confidence of the text line recognition result.

### getCharacterResults

Gets all the character results.

```java
public CharacterResult[] getCharacterResults()
```

**Return Value**

Returns all the character results as a `CharacterResult` array.

**See Also**

[CharacterResult]({{ site.dlr_java_api }}character-result.html)

### getCharacterResult

Gets the character result at a specific index.

```java
public CharacterResult getCharacterResult(int index)
```

**Parameters**

`index` The index of the character result to retrieve.

**Return Value**

Returns the `CharacterResult` at the specified index.

**See Also**

[CharacterResult]({{ site.dlr_java_api }}character-result.html)

### getCharacterResultsCount

Gets the count of character results.

```java
public int getCharacterResultsCount()
```

**Return Value**

Returns the count of character results.

### getSpecificationName

Gets the name of the text line specification that generated this item.

```java
public String getSpecificationName()
```

**Return Value**

Returns the name of the text line specification that generated this item.

### getRawText

Gets the recognized raw text, excluding any concatenation separators.

```java
public String getRawText()
```

**Return Value**

Returns the recognized raw text.
