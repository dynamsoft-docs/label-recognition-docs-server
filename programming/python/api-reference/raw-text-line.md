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

*Module:* dynamsoft_label_recognizer

```python
class RawTextLine
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `RawTextLine` class. |
| [`get_text`](#get_text) | Gets the recognized text.|
| [`get_confidence`](#get_confidence) | Gets the confidence level of the recognized text.|
| [`get_character_results_count`](#get_character_results_count) | Gets the number of individual character recognition results in the line.|
| [`get_character_result`](#get_character_result) | Gets the character recognition result at the specified index.|
| [`get_location`](#get_location) | Gets the location of the text line.|
| [`get_row_number`](#get_row_number) | Gets the row number of the text line within the image.|
| [`get_specification_name`](#get_specification_name) | Gets the name of the text line specification that generated this element.|
| [`get_status`](#get_status) | Gets the status of the text line.|
| [`set_text`](#set_text) | Sets the recognized text.|
| [`set_location`](#set_location) | Sets the location of the text line.|
| [`set_row_number`](#set_row_number) | Sets the row number of the text line within the image.|
| [`set_specification_name`](#set_specification_name) | Sets the name of the text line specification that generated this element. |
| [`set_character_results`](#set_character_results) | Sets the character recognition results for the text line. |
| [`clone`](#clone) | Clones the `RawTextLine` object.|

### \_\_init\_\_

Initializes a new instance of the `RawTextLine` class.

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

Returns the character recognition result.

**See Also**

[CharacterResult]({{ site.dlr_python_api }}character-result.html)

### get_location

Gets the location of the text line.

```python
def get_location(self) -> Quadrilateral:
```

**Return value**

Returns a `Quadrilateral` object which represents the location of the text line.

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

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

Returns the name of the text line specification.

### get_status

Gets the status of the text line.

```python
def get_status(self) -> int:
```

**Return value**

Returns the status of the text line. This is one of the values of the `EnumRawTextLineStatus` enumeration.

**See also**

[EnumRawTextLineStatus]({{ site.dlr_python_api }}enum-raw-text-line-status.html)

### set_text

Sets the recognized text.

```python
def set_text(self, text: str) -> None:
```

**Parameters**

`text` The text to be set.


### set_location

Sets the location of the text line.

```python
def set_location(self, location: Quadrilateral) -> int:
```

**Parameters**

`location` The location of the text line.

**Return value**

Returns 0 if successful; otherwise returns an error code.

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### set_row_number

Sets the row number of the text line within the image.

```python
def set_row_number(self, row_number: int) -> int:
```

**Parameters**

`row_number` The row number of the text line within the image.

**Return value**

Returns 0 if successful; otherwise returns an error code.

### set_specification_name

Sets the name of the text line specification that generated this element.

```python
def set_specification_name(self, specification_name: str) -> int:
```

**Parameters**

`specification_name` The name of the text line specification.

**Return value**

Returns 0 if successful; otherwise returns an error code.

### clone

Clones the `RawTextLine` object.

```python
def clone(self) -> "RawTextLine":
```

**Return value**

Returns the cloned `RawTextLine` object.

### set_character_results

Sets the character recognition results for the text line..

```python
def set_character_results(self, char_array: List[CharacterResult]) -> int:
```

**Parameters**

`char_array` The character recognition results to set.

**Return value**

Returns 0 if successful; otherwise returns an error code.
