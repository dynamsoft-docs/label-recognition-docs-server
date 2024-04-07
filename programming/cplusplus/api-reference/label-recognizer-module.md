---
layout: default-layout
title: class CLabelRecognizerModule - Dynamsoft Label Recognizer Classes
description: This page shows the C++ edition of the class CLabelRecognizerModule in Label Recognizer Module.
keywords: label recognizer module, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: C++ CLabelRecognizerModule Class
---

# CLabelRecognizerModule

The `CLabelRecognizerModule` class defines general functions in the label recognizer module.

## Definition

*Namespace:* dynamsoft::dlr

*Assembly:* DynamsoftLabelRecognizer

```cpp
class CLabelRecognizerModule 
```

## Methods Summary

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [GetVersion](#getversion)                                     | Returns the version of the label recognizer module. |
| [CreateRecognizedTextLineElement](#createrecognizedtextlineelement) | Create a Recognized Text Line Element object.          |
| [CreateLocalizedTextLineElement](#createlocalizedtextlineelement) | Create a Localized Text Line Element object.          |

## GetVersion

Returns the version of the label recognizer module.

```cpp
static const char* GetVersion();
```

**Parameters**

None.

**Return Value**

Returns a const char pointer representing the version of the label recognizer module.

### CreateRecognizedTextLineElement

Create a Recognized Text Line Element object.

```cpp
static intermediate_results::CRecognizedTextLineElement* CreateRecognizedTextLineElement();
```

**Return Value**

Returns an instance of CRecognizedTextLineElement.

### CreateLocalizedTextLineElement

Create a Localized Text Line Element object.

```cpp
static intermediate_results::CLocalizedTextLineElement* CreateLocalizedTextLineElement();
```

**Return Value**

Returns an instance of CLocalizedTextLineElement.
