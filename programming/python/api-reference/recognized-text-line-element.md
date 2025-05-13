---
layout: default-layout
title: RecognizedTextLineElement - Dynamsoft Label Recognizer Classes
description: The class RecognizedTextLineElement of Dynamsoft Label Recognizer represents a line of recognized text in an image.
keywords: Recognized text line element
---

# RecognizedTextLineElement

The `RecognizedTextLineElement` class represents a line of recognized text in an image. It inherits from the `RegionObjectElement` class.

## Definition

*Module:* dynamsoft_label_recognizer

```python
class RecognizedTextLineElement(RegionObjectElement)
```

*Inheritance:* [RegionObjectElement]({{ site.dcvb_python_api }}core/intermediate-results/region-object-element.html) -> RecognizedTextLineElement

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `RecognizedTextLineElement` class. |
| [`get_text`](#get_text) | Gets the recognized text. |
| [`get_confidence`](#get_confidence) | Gets the confidence level of the recognized text. |
| [`get_character_results_count`](#get_character_results_count) | Gets the number of individual character recognition results in the line. |
| [`get_character_result`](#get_character_result) | Gets the character recognition result at the specified index. |
| [`get_row_number`](#get_row_number) | Gets the row number of the text line within the image. |
| [`get_specification_name`](#get_specification_name) | Gets the name of the text line specification that generated this element. |
| [`get_raw_text`](#get_raw_text) | Gets the recognized raw text, excluding any concatenation separators. |
| [`set_text`](#set_text) | Sets the recognized text. |

### \_\_init\_\_

Initializes a new instance of the `RecognizedTextLineElement` class.

```python
def __init__(self, *args, **kwargs):
```

### get_text

Gets the recognized text.

```python
def get_text(self) -> str:
```

**Return value**

Returns the recognized text.

### get_confidence

Gets the confidence level of the recognized text.

```python
def get_confidence(self) -> int:
```

**Return value**

Returns an integer value representing the confidence level of the recognized text.

### get_character_results_count

Gets the number of individual character recognition results in the line.

```python
def get_character_results_count(self) -> int:
```

**Return value**

Returns an integer value representing the number of individual character recognition results.

### get_character_result

Gets the character recognition result at the specified index.

```python
def get_character_result(self, index: int) -> CharacterResult:
```

**Parameters**

`index` The index of the character recognition result to retrieve.

**Return value**

Returns a `CharacterResult` object.

**See Also**

[CharacterResult]({{ site.dlr_python_api }}character-result.html)

### get_row_number

Gets the row number of the text line within the image.

```python
def get_row_number(self) -> int:
```

**Return value**

Returns an integer value representing the row number of the text line within the image.

### get_specification_name

Gets the name of the text line specification that generated this element.

```python
def get_specification_name(self) -> str:
```

**Return value**

Returns the name of the text line specification that generated this element.

### get_raw_text

Gets the recognized raw text, excluding any concatenation separators.

```python
def get_raw_text(self) -> str:
```

**Return value**

Returns the recognized raw text.

### set_text

Sets the recognized text.

```python
def set_text(self, text: str) -> None:
```

**Parameters**

`text` The text to be set.

