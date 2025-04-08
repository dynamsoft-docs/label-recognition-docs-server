---
layout: default-layout
title: RecognizedTextLinesResult Class - Dynamsoft Label Recognizer Module Python Edition API Reference
description: Definition of the RecognizedTextLinesResult class in Dynamsoft Label Recognizer Module Python Edition.
keywords: Recognized text lines result
---

# RecognizedTextLinesResult

The `RecognizedTextLinesResult` class represents the result of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Module:* dynamsoft_label_recognizer

```python
class RecognizedTextLinesResult
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_original_image_hash_id`](#get_original_image_hash_id) | Gets the hash ID of the original image. |
| [`get_original_image_tag`](#get_original_image_tag) | Gets the tag of the original image. |
| [`get_items`](#get_items) | Gets all the text line result items. |
| [`get_rotation_transform_matrix`](#get_rotation_transform_matrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`get_error_code`](#get_error_code) | Gets the error code of the recognition result, if an error occurred. |
| [`get_error_string`](#get_error_string) | Gets the error message of the recognition result, if an error occurred. |

### get_original_image_hash_id

Gets the hash ID of the original image.

```python
def get_original_image_hash_id(self) -> str:
```

**Return Value**

Returns a string containing the hash ID of the original image.

### get_original_image_tag

Gets the tag of the original image.

```python
def get_original_image_tag(self) -> ImageTag:
```

**Return Value**

Returns an `ImageTag` object representing the tag of the original image.

**See Also**

[ImageTag]({{ site.dcv_python_api }}core/basic-classes/image-tag.html)

### get_items

Gets all the text line result items.

```python
def get_items(self) -> List[TextLineResultItem]:
```

**Return Value**

Returns a `TextLineResultItem` list.

**See Also**

[TextLineResultItem]({{ site.dlr_python_api }}text-line-result-item.html)

### get_rotation_transform_matrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```python
def get_rotation_transform_matrix(self) -> List[float]:
```

**Return Value**

Returns a float list of length 9 which represents a 3x3 rotation matrix.

### get_error_code

Gets the error code of the recognition result, if an error occurred.

```python
def get_error_code(self) -> int:
```

**Return Value**

Returns the error code of the recognition result, or 0 if no error occurred.

**See Also**

[EnumErrorCode]({{ site.dcv_python_api }}core/enum-error-code.html?lang=python)

### get_error_string

Gets the error message of the recognition result, if an error occurred.

```python
def get_error_string(self) -> str:
```

**Return Value**

Returns a string containing the error message of the recognition result, or an empty string if no error occurred.

