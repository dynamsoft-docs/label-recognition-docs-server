---
layout: default-layout
title: BufferedCharacterItem Class - Dynamsoft Label Recognizer Module Python Edition API Reference
description: Definition of the BufferedCharacterItem class in Dynamsoft Label Recognizer Module Python Edition.
keywords: BufferedCharacterItem
---

# BufferedCharacterItem

The `BufferedCharacterItem` class represents a text line result item recognized by the library. It is derived from `CapturedResultItem`.

## Definition

*Module:* dynamsoft_label_recognizer

```python
class BufferedCharacterItem
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_character`](#get_character) | Gets the buffered character value. |
| [`get_image`](#get_image) | Gets the image data of the buffered character. |
| [`get_features`](#get_features) | Gets all the features formatted with id and value of the buffered character. |

### get_character

Gets the buffered character value.

```python
def get_character(self) -> str:
```

**Return Value**

Returns the buffered character value.

### get_image

Gets the image data of the buffered character.

```python
def get_image(self) -> ImageData:
```

**Return Value**

Returns the image data of the buffered character.

**See Also**

[ImageData]({{ site.dcv_python_api }}core/basic-classes/image-data.html)

### get_features

Gets all the features formatted with id and value of the buffered character.

```python
def get_features(self) -> List[Tuple[int, float]]:
```

**Return Value**

Returns a tuple list while each item contains following elements.
- `feature_id` <*int*>: The feature id.
- `feature_value` <*float*>: The feature value.


