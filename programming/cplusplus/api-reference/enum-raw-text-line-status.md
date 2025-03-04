---
layout: default-layout
title: RawTextLineStatus - Dynamsoft LabelRecognizer Enumerations
description: The enumeration RawTextLineStatus of Dynamsoft LabelRecognizer describes the final status of a raw text line.
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
