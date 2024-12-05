---
layout: default-layout
title: RawTextLinesUnit - Dynamsoft Label Recognizer Classes
description: The class RawTextLinesUnit of Dynamsoft Label Recognizer represents a unit that contains recognized raw text lines.
keywords: Recognized raw text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RawTextLinesUnit

The `RawTextLinesUnit` class represents an intermediate result unit containing raw text lines. It inherits from the `IntermediateResultUnit` class.

## Definition

*Module:* dynamsoft_label_recognizer

```python
class RawTextLinesUnit(IntermediateResultUnit)
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_python_api }}core/intermediate-results/intermediate-result-unit.html) -> RawTextLinesUnit

## Methods

| Method | Description |
|--------|-------------|
| [`get_count`](#get_count) | Gets the number of raw text lines in the unit.|
| [`get_raw_textLine`](#get_raw_textline) | Gets a raw text line.|
| [`operator[]`](#operator) | Gets a raw text line.|
| [`remove_all_raw_text_lines`](#remove_all_raw_text_lines) | Removes all raw text lines.|
| [`remove_raw_text_line`](#remove_raw_text_line) | Removes the raw text line at the specified index.|
| [`add_raw_text_line`](#add_raw_text_line) | Adds a raw text line.|
| [`set_raw_text_line`](#set_raw_text_line) | Sets the raw text line at the specified index.|

### get_count

Gets the number of raw text lines in the unit.

```python
def get_count(self) -> int:
```

**Return value**

Returns the number of raw text lines in the unit.

### get_raw_textLine

Gets a raw text line.

```python
def get_raw_text_line(self, index: int) -> RawTextLine:
```

**Parameters**

`index` The index of the raw text line to retrieve.

**Return value**

Returns the raw text line at the specified index.

**See Also**

[RawTextLine]({{ site.dlr_python_api }}raw-text-line.html)

### remove_all_raw_text_lines

Removes all raw text lines.

```python
def remove_all_raw_text_lines(self) -> None:
```

### remove_raw_text_line

Removes the raw text line at the specified index.

```python
def remove_raw_text_line(self, index: int) -> int:
```

**Parameters**

`index` The index of the raw text line to remove.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### add_raw_text_line

Adds a raw text line.

```python
def add_raw_text_line(self, text_line: RawTextLine, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`text_line` The raw text line to add.

`matrix_to_original_image` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[RawTextLine]({{ site.dlr_python_api }}raw-text-line.html)

### set_raw_text_line

Sets the raw text line at the specified index.

```python
def set_raw_text_line(self, index: int, text_line: RawTextLine, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The index of the raw text line to set.

`text_line` The raw text line to set.

`matrix_to_original_image` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[RawTextLine]({{ site.dlr_python_api }}raw-text-line.html)
