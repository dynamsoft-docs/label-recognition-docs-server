---
layout: default-layout
title: LocalizedTextLinesUnit - Dynamsoft Label Recognizer Classes
description: The class LocalizedTextLinesUnit of Dynamsoft Label Recognizer represents a unit that contains localized text lines.
keywords: Localized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LocalizedTextLinesUnit

The `LocalizedTextLinesUnit` class represents a unit that contains localized text lines. It inherits from the `IntermediateResultUnit` class.

## Definition

*Module:* dynamsoft_label_recognizer

```python
class LocalizedTextLinesUnit(IntermediateResultUnit)
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_python_api }}core/intermediate-results/intermediate-result-unit.html) -> LocalizedTextLinesUnit

## Methods

| Method                            | Description |
|-----------------------------------|-------------|
| [`get_count`](#get_count)           | Gets the number of localized text lines in the unit.|
| [`get_localized_text_line`](#get_localized_text_line) | Gets a localized text line element.|
| [`remove_all_localized_text_lines`](#remove_all_localized_text_lines) | Removes all localized text lines.|
| [`remove_localized_text_line`](#remove_localized_text_line) | Removes the localized text line at the specified index.|
| [`add_localized_text_line`](#add_localized_text_line) | Adds a localized text line.|
| [`set_localized_text_line`](#set_localized_text_line) | Sets the localized text line at the specified index.|

### get_count

Gets the number of localized text lines in the unit.

```python
def get_count(self) -> int:
```

**Return value**

Returns the number of localized text lines in the unit.

### get_localized_text_line

Gets a localized text line element.

```python
def get_localized_text_line(self, index: int) -> LocalizedTextLineElement:
```

**Parameters**

`index` The index of the localized text line element to retrieve.

**Return value**

Returns the localized text line element at the specified index.

**See Also**

[LocalizedTextLineElement]({{ site.dlr_python_api }}localized-text-line-element.html)

### remove_all_localized_text_lines

Removes all localized text lines.

```python
def remove_all_localized_text_lines(self) -> None:
```

### remove_localized_text_line

Removes the localized text line at the specified index.

```python
def remove_localized_text_line(self, index: int) -> int:
```

**Parameters**

`index` The index of the localized text line to remove.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

### add_localized_text_line

Adds a localized text line.

```python
def add_localized_text_line(self, element: LocalizedTextLineElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`element` The localized text line element to add.

`matrix_to_original_image` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[LocalizedTextLineElement]({{ site.dlr_python_api }}localized-text-line-element.html)

### set_localized_text_line

Sets the localized text line at the specified index.

```python
def set_localized_text_line(self, index: int, element: LocalizedTextLineElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The index of the localized text line to set.

`element` The localized text line element to set.

`matrix_to_original_image` The matrix to original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[LocalizedTextLineElement]({{ site.dlr_python_api }}localized-text-line-element.html)
