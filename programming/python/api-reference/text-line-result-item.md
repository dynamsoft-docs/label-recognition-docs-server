---
layout: default-layout
title: TextLineResultItem Class - Dynamsoft Label Recognizer Module Python Edition API Reference
description: Definition of the TextLineResultItem class in Dynamsoft Label Recognizer Module Python Edition.
keywords: Text line result item
---

# TextLineResultItem

The `TextLineResultItem` class represents a text line result item recognized by the library. It is derived from `CapturedResultItem`.

## Definition

*Module:* dynamsoft_label_recognizer

*Inheritance:* [CapturedResultItem]({{ site.dcv_python_api }}core/basic-classes/captured-result-item.html) -> TextLineResultItem

```python
class TextLineResultItem(dynamsoft_core.CapturedResultItem)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_text`](#get_text) | Gets the text content of the text line. |
| [`get_location`](#get_location) | Gets the location of the text line in the form of a quadrilateral. |
| [`get_confidence`](#get_confidence) | Gets the confidence of the text line recognition result. |
| [`get_character_results`](#get_character_results) | Gets all the character results. |
| [`get_specification_name`](#get_specification_name) | Gets the name of the text line specification that generated this item. |
| [`get_raw_text`](#get_raw_text) | Gets the recognized raw text, excluding any concatenation separators. |

### get_text

Gets the text content of the text line.

```python
def get_text(self) -> str:
```

**Return Value**

Returns the text content of the text line.

### get_location

Gets the location of the text line in the form of a quadrilateral.

```python
def get_location(self) -> Quadrilateral:
```

**Return Value**

Returns the location of the text line in the form of a quadrilateral.

**See Also**

[Quadrilateral]({{ site.dcv_python_api }}core/basic-classes/quadrilateral.html)

### get_confidence

Gets the confidence of the text line recognition result.

```python
def get_confidence(self) -> int:
```

**Return Value**

Returns the confidence of the text line recognition result.

### get_character_results

Gets all the character results.

```python
def get_character_results(self) -> List[CharacterResult]:
```

**Return Value**

Returns all the character results as a `CharacterResult` list.

**See Also**

[CharacterResult]({{ site.dlr_python_api }}character-result.html)

### get_specification_name

Gets the name of the text line specification that generated this item.

```python
def get_specification_name(self) -> str:
```

**Return Value**

Returns the name of the text line specification that generated this item.

### get_raw_text

Gets the recognized raw text, excluding any concatenation separators.

```python
def get_raw_text(self) -> str:
```

**Return Value**

Returns the recognized raw text.
