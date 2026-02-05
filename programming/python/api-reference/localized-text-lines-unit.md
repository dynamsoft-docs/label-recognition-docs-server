---
layout: default-layout
title: LocalizedTextLinesUnit - Dynamsoft Label Recognizer Classes
description: The class LocalizedTextLinesUnit of Dynamsoft Label Recognizer represents a unit that contains localized text lines.
keywords: Localized text lines unit
---

# LocalizedTextLinesUnit

The `LocalizedTextLinesUnit` class represents a unit that contains localized text lines. It inherits from the `IntermediateResultUnit` class.

## Definition

*Module:* dlr

```python
class LocalizedTextLinesUnit(IntermediateResultUnit)
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-unit.html) -> LocalizedTextLinesUnit

## Methods

| Method                            | Description |
|-----------------------------------|-------------|
| [`get_count`](#get_count)           | Gets the number of localized text lines in the unit.|
| [`get_localized_text_line`](#get_localized_text_line) | Gets a localized text line element.|
| [`remove_all_localized_text_lines`](#remove_all_localized_text_lines) | Removes all localized text lines.|
| [`remove_localized_text_line`](#remove_localized_text_line) | Removes the localized text line at the specified index.|
| [`add_localized_text_line`](#add_localized_text_line) | Adds a localized text line.|
| [`set_localized_text_line`](#set_localized_text_line) | Sets the localized text line at the specified index.|
| [`get_auxiliary_region_elements_count`](#get_auxiliary_region_elements_count) | Gets the count of auxiliary region elements in the unit. |
| [`get_auxiliary_region_element`](#get_auxiliary_region_element) | Gets the auxiliary region element at the specified index. |
| [`set_auxiliary_region_element`](#set_auxiliary_region_element) | Sets the auxiliary region element at the specified index. |
| [`add_auxiliary_region_element`](#add_auxiliary_region_element) | Adds a new auxiliary region element to this unit. |
| [`remove_auxiliary_region_element`](#remove_auxiliary_region_element) | Removes the auxiliary region element at the specified index. |
| [`remove_all_auxiliary_region_elements`](#remove_all_auxiliary_region_elements) | Removes all auxiliary region elements from this unit. |

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

### get_auxiliary_region_elements_count

Gets the count of auxiliary region elements in the unit.

```python
def get_auxiliary_region_elements_count(self) -> int:
```

**Return value**

Returns the number of auxiliary region elements.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### get_auxiliary_region_element

Gets the auxiliary region element at the specified index.

```python
def get_auxiliary_region_element(self, index: int) -> AuxiliaryRegionElement:
```

**Parameters**

`index` The zero-based index of the auxiliary region element to retrieve.

**Return value**

Returns an `AuxiliaryRegionElement` object, or `None` if the index is out of range.

**See Also**

[AuxiliaryRegionElement]({{ site.dcvb_python_api }}core/intermediate-results/auxiliary-region-element.html)

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### set_auxiliary_region_element

Sets or replaces the auxiliary region element at the specified index.

```python
def set_auxiliary_region_element(self, index: int, element: AuxiliaryRegionElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`index` The zero-based index where the element should be set.

`element` The auxiliary region element to set.

`matrix_to_original_image` The transformation matrix from the current image to the original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[AuxiliaryRegionElement]({{ site.dcvb_python_api }}core/intermediate-results/auxiliary-region-element.html)

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### add_auxiliary_region_element

Adds a new auxiliary region element to this unit.

```python
def add_auxiliary_region_element(self, element: AuxiliaryRegionElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX) -> int:
```

**Parameters**

`element` The auxiliary region element to add.

`matrix_to_original_image` The transformation matrix from the current image to the original image.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**See Also**

[AuxiliaryRegionElement]({{ site.dcvb_python_api }}core/intermediate-results/auxiliary-region-element.html)

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### remove_auxiliary_region_element

Removes the auxiliary region element at the specified index.

```python
def remove_auxiliary_region_element(self, index: int) -> int:
```

**Parameters**

`index` The zero-based index of the auxiliary region element to remove.

**Return value**

Returns 0 if successful, otherwise returns a negative value.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

### remove_all_auxiliary_region_elements

Removes all auxiliary region elements from this unit.

```python
def remove_all_auxiliary_region_elements(self) -> None:
```

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

