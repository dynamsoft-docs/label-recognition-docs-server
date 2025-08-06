---
layout: default-layout
title: LocalizedTextLineElement - Dynamsoft Label Recognizer Classes
description: The class LocalizedTextLineElement of Dynamsoft Label Recognizer represents a localized text line element.
keywords: Localized text line element
---

# LocalizedTextLineElement

The `LocalizedTextLineElement` class represents a localized text line element. It inherits from the `RegionObjectElement` class.

## Definition

*Package:* com.dynamsoft.dlr.intermediate_results

*Inheritance:* [RegionObjectElement]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html) -> LocalizedTextLineElement

```java
public class LocalizedTextLineElement extends RegionObjectElement
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`LocalizedTextLineElement`](#localizedtextlineelement) | Initializes a new instance of the `LocalizedTextLineElement` class. |
| [`getCharacterQuadsCount`](#getcharacterquadscount) | Gets the number of character quads in the text line.|
| [`getCharacterQuad`](#getcharacterquad) | Gets the quadrilateral of a specific character in the text line. |
| [`getCharacterQuads`](#getcharacterquads) | Gets all character quadrilaterals in the text line. |
| [`getRowNumber`](#getrownumber) | Gets the row number of the text line. |
| [`setLocation`](#setlocation) | Sets the location of the text line element. |

### LocalizedTextLineElement

Initializes a new instance of the `LocalizedTextLineElement` class.

```java
public LocalizedTextLineElement()
```

### getCharacterQuadsCount

Gets the number of character quads in the text line.

```java
public int getCharacterQuadsCount()
```

**Return value**

Returns the number of character quads in the text line.

### getCharacterQuad

Gets the quadrilateral of a specific character in the text line.

```java
public Quadrilateral getCharacterQuad(int index) throws LabelRecognizerException
```

**Parameters**

`index` The index of the character quad to retrieve.

**Return value**

Returns the quadrilateral of the specified character.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### getCharacterQuads

Gets all character quadrilaterals in the text line.

```java
public Quadrilateral[] getCharacterQuads()
```

**Return value**

Returns an array of quadrilaterals representing all characters in the text line.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### getRowNumber

Gets the row number of the text line.

```java
public int getRowNumber()
```

**Return value**

Returns the row number of the text line.

### setLocation

Sets the location of the text line element.

```java
public void setLocation(Quadrilateral location) throws LabelRecognizerException
```

**Parameters**

`location` The location to set as a Quadrilateral object.

**Exceptions**

[`LabelRecognizerException`]({{ site.dlr_java_api }}label-recognizer-exception.html)

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)
