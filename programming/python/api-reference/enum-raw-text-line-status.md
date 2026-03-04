---
layout: default-layout
title: RawTextLineStatus - Dynamsoft LabelRecognizer Python Enumerations
description: The enumeration RawTextLineStatus in Dynamsoft Label Recognizer Python Edition describes the final status of a raw text line, indicating whether it was recognized successfully or failed.
keywords: Raw Text Line Status
codeAutoHeight: true
---

# Enumeration RawTextLineStatus

`RawTextLineStatus` enumerates the final status of a raw text line.

```python
class EnumRawTextLineStatus(IntEnum):
    # Localized but recognition not performed.
    RTLS_LOCALIZED,
    # Recognition failed.
    RTLS_RECOGNITION_FAILED,
    # Successfully recognized.
    RTLS_RECOGNITION_SUCCEEDED
```
