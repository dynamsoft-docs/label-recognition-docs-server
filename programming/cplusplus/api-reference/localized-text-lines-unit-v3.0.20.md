---
layout: default-layout
title: CLocalizedTextLinesUnit - Dynamsoft Label Recognizer Classes
description: The class CLocalizedTextLinesUnit of Dynamsoft Label Recognizer represents a unit that contains localized text lines.
keywords: Localized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CLocalizedTextLinesUnit
permalink: /programming/cplusplus/api-reference/localized-text-lines-unit-v3.0.20.html
---

# CLocalizedTextLinesUnit

The `CLocalizedTextLinesUnit` class represents a unit that contains localized text lines. It inherits from the `CIntermediateResultUnit` class.

## Definition

*Namespace:* dynamsoft::dlr::intermediate_results

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CLocalizedTextLinesUnit : public CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CLocalizedTextLinesUnit

## Methods

| Method                            | Description |
|-----------------------------------|-------------|
| [`GetCount`](#getcount)           | Gets the number of localized text lines in the unit.|
| [`GetLocalizedTextLine`](#getlocalizedtextline) | Gets a pointer to a specific localized text line element.|

### GetCount

Gets the number of localized text lines in the unit.

```cpp
virtual int GetCount() const = 0;
```

**Return value**

Returns the number of localized text lines in the unit.

### GetLocalizedTextLine

Gets a pointer to a specific localized text line element.

```cpp
virtual const CLocalizedTextLineElement* GetLocalizedTextLine(int index) const = 0;
```

**Parameters**

`[in] index` The index of the localized text line element to retrieve.

**Return value**

Returns a const pointer to the localized text line element at the specified index.
