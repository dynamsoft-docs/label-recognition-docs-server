---
layout: default-layout
title: class CLabelRecognizerModule - Dynamsoft Label Recognizer Classes
description: API reference for the CLabelRecognizerModule class in Dynamsoft Label Recognizer C++ Edition, which provides general functions for the Label Recognizer module.
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

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [GetVersion](#getversion)                                     | Returns the version of the label recognizer module. |
| [CreateRecognizedTextLineElement](#createrecognizedtextlineelement) | Create a Recognized Text Line Element object.          |
| [CreateLocalizedTextLineElement](#createlocalizedtextlineelement) | Create a Localized Text Line Element object.          |
| [CreateRawTextLine](#createrawtextline)                       | Create a Raw Text Line object.                       |

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

### CreateRawTextLine

Create a Raw Text Line object.

```cpp
static intermediate_results::CRawTextLine* CreateRawTextLine();
```

**Return Value**

Returns an instance of CRawTextLine.
