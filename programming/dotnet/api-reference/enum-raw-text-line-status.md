---
layout: default-layout
title: RawTextLineStatus - Dynamsoft LabelRecognizer .NET Enumerations
description: The enumeration RawTextLineStatus in Dynamsoft Label Recognizer .NET Edition describes the final status of a raw text line, indicating whether it was recognized successfully or failed.
keywords: Raw Text Line Status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration RawTextLineStatus

`RawTextLineStatus` enumerates the final status of a raw text line.

```csharp
public enum EnumRawTextLineStatus
{
    /** Localized but recognition not performed. */
    RTLS_LOCALIZED,
    /** Recognition failed. */
    RTLS_RECOGNITION_FAILED,
    /** Successfully recognized. */
    RTLS_RECOGNITION_SUCCEEDED
}
```
