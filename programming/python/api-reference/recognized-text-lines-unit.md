---
layout: default-layout
title: RecognizedTextLinesUnit - Dynamsoft Label Recognizer Classes
description: The class RecognizedTextLinesUnit of Dynamsoft Label Recognizer represents an intermediate result unit containing recognized text lines.
keywords: Recognized text lines unit
---

# RecognizedTextLinesUnit

The `RecognizedTextLinesUnit` class represents an intermediate result unit containing recognized text lines. It inherits from the `IntermediateResultUnit` class.

## Definition

*Module:* dynamsoft_label_recognizer

```python
class RecognizedTextLinesUnit(IntermediateResultUnit)
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_python_api }}core/intermediate-results/intermediate-result-unit.html) -> RecognizedTextLinesUnit

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`get_count`](#get_count) | Gets the number of recognized text lines in the unit.|
| [`get_recognized_text_line`](#get_recognized_text_line) | Gets the RecognizedTextLineElement object at the specified index. |
| [`remove_all_recognized_text_lines`](#remove_all_recognized_text_lines) | Removes all recognized text lines. |
| [`remove_recognized_text_line`](#remove_recognized_text_line) | Removes the recognized text line at the specified index. |
| [`add_recognized_text_line`](#add_recognized_text_line) | Adds a recognized text line. |
| [`set_recognized_text_line`](#set_recognized_text_line) | Sets the recognized text line at the specified index. |


### get_count

Gets the number of recognized text lines in the unit.

```python
def get_count(self) -> int:
```

**Return value**

Returns the number of recognized text lines in the unit.

### get_recognized_text_line

Gets the RecognizedTextLineElement object at the specified index.

```python
def get_recognized_text_line(self, index: int) -> RecognizedTextLineElement:
```

**Parameters**

`index` The index of the desired RecognizedTextLineElement object.

**Return value**

Returns the `RecognizedTextLineElement` object at the specified index.

**See Also**

[RecognizedTextLineElement]({{ site.dlr_python_api }}recognized-text-line-element.html)

### remove_all_recognized_text_lines

Removes all recognized text lines.

```python
def remove_all_recognized_text_lines(self) -> None:
```

### remove_recognized_text_line

Removes the recognized text line at the specified index.

```python
def remove_recognized_text_line(self, index: int) -> int:
```

**Parameters**

`index` The index of the recognized text line to remove.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### add_recognized_text_line

Adds a recognized text line.

```python
def add_recognized_text_line(self, element: RecognizedTextLineElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`element` The recognized text line to add.

`matrix_to_original_image` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[RecognizedTextLineElement]({{ site.dlr_python_api }}recognized-text-line-element.html)

### set_recognized_text_line

Sets the recognized text line at the specified index.

```python
def set_recognized_text_line(self, index: int, element: RecognizedTextLineElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The index of the recognized text line to set.

`element` The recognized text line to set.

`matrix_to_original_image` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[RecognizedTextLineElement]({{ site.dlr_python_api }}recognized-text-line-element.html)
