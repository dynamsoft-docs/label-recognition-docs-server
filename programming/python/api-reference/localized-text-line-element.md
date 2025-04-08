---
layout: default-layout
title: LocalizedTextLineElement - Dynamsoft Label Recognizer Classes
description: The class LocalizedTextLineElement of Dynamsoft Label Recognizer represents a localized text line element.
keywords: Localized text line element
---

# LocalizedTextLineElement

The `LocalizedTextLineElement` class represents a localized text line element. It inherits from the `RegionObjectElement` class.

## Definition

*Module:* dynamsoft_label_recognizer

```python
class LocalizedTextLineElement(RegionObjectElement)
```

*Inheritance:* [RegionObjectElement]({{ site.dcv_cpp_api }}core/intermediate-results/region-object-element.html) -> LocalizedTextLineElement

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `LocalizedTextLineElement` class. |
| [`get_character_quads_count`](#get_character_quads_count) | Gets the number of character quads in the text line.|
| [`get_character_quad`](#get_character_quad) | Gets the quadrilateral of a specific character in the text line. |
| [`get_row_number`](#get_row_number) | Gets the row number of the text line. |

### \_\_init\_\_

Initializes a new instance of the `LocalizedTextLineElement` class.

```python
def __init__(self, *args, **kwargs):
```

### get_character_quads_count

Gets the number of character quads in the text line.

```python
def get_character_quads_count(self) -> int:
```

**Return value**

Returns the number of character quads in the text line.

### get_character_quad

Gets the quadrilateral of a specific character in the text line.

```python
def get_character_quad(self, index: int) -> Tuple[int, Quadrilateral]:
```

**Parameters**

`index` The index of the character.

**Return value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `quad` <*Quadrilateral*>: The quadrilateral of the character.

### get_row_number

Gets the row number of the text line.

```python
def get_row_number(self) -> int:
```

**Return value**

Returns the row number of the text line.
