---
layout: default-layout
title: BufferedCharacterItem Class - Dynamsoft Label Recognizer Module Java Edition API Reference
description: Definition of the BufferedCharacterItem class in Dynamsoft Label Recognizer Module Java Edition.
keywords: BufferedCharacterItem
---

# BufferedCharacterItem

The `BufferedCharacterItem` class represents a buffered character item recognized by the library.

## Definition

*Package:* com.dynamsoft.dlr

```java
public class BufferedCharacterItem
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getCharacter`](#getcharacter) | Gets the buffered character value. |
| [`getImage`](#getimage) | Gets the image data of the buffered character. |
| [`getFeatures`](#getfeatures) | Gets all the features formatted with id and value of the buffered character. |

### getCharacter

Gets the buffered character value.

```java
public char getCharacter()
```

**Return Value**

Returns the buffered character value.

### getImage

Gets the image data of the buffered character.

```java
public ImageData getImage()
```

**Return Value**

Returns the image data of the buffered character.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### getFeatures

Gets all the features formatted with id and value of the buffered character.

```java
public HashMap<Integer, Float> getFeatures()
```

**Return Value**

Returns all the features as a HashMap where keys are feature IDs and values are feature values.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### getFeatures

Gets all the features formatted with id and value of the buffered character.

```java
public HashMap<Integer, Float> getFeatures()
```

**Return Value**

Returns all the features as a HashMap where keys are feature IDs and values are feature values.


