---
layout: default-layout
title: RecognizedTextLinesResult Class - Dynamsoft Label Recognizer Module .NET Edition API Reference
description: Definition of the RecognizedTextLinesResult class in Dynamsoft Label Recognizer Module .NET Edition.
keywords: Recognized text lines result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RecognizedTextLinesResult

The `RecognizedTextLinesResult` class represents the result of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Namespace:* Dynamsoft.DLR

*Inheritance:* [CapturedResultBase]({{ site.dcvb_dotnet_api }}core/basic-classes/captured-result-base.html) -> RecognizedTextLinesResult


```csharp
public class RecognizedTextLinesResult : CapturedResultBase, IEnumerable<TextLineResultItem>
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetItems`](#getitems) | Gets all the text line result items. |
| [`GetItemsCount`](#getitemscount) | Gets the number of text line result items in current result object. |
| [`GetItem`](#getitem) | Gets a specific text line result item. |

### GetItems

Gets all the text line result items.

```csharp
TextLineResultItem GetItems()
```

**Return Value**

Returns a `TextLineResultItem` array.

**See Also**

[TextLineResultItem]({{ site.dlr_dotnet_api }}text-line-result-item.html)

### GetItemsCount

Gets the number of text line result items in current result object.

```csharp
int GetItemsCount()
```

**Return value**

Returns the number of text line result items in current result object.

### GetItem

Gets a specific text line result item.

```csharp
TextLineResultItem GetItem(int index)
```

**Parameters**

`[in] index` The index of specific text line result item.

**Return value**

Returns the specific text line result item.

**See Also**

[TextLineResultItem]({{ site.dlr_dotnet_api }}text-line-result-item.html)
