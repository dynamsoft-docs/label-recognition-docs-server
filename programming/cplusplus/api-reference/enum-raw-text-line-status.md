---
layout: default-layout
title: RawTextLineStatus Enum – Label Recognizer C++ Ref
description: "Explore RawTextLineStatus values in Dynamsoft Label Recognizer C++ API and learn how they define status, configuration, and processing behavior for modern web."
keywords: Raw Text Line Status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RawTextLineStatus
codeAutoHeight: true
---

# Enumeration RawTextLineStatus

`RawTextLineStatus` enumerates the final status of a raw text line.

```cpp
typedef enum RawTextLineStatus
{
    /** Localized but recognition not performed. */
    RTLS_LOCALIZED,
    /** Recognition failed. */
    RTLS_RECOGNITION_FAILED,
    /** Successfully recognized. */
    RTLS_RECOGNITION_SUCCEEDED
} RawTextLineStatus;
```
