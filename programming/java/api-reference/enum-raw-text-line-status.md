---
layout: default-layout
title: RawTextLineStatus - Dynamsoft LabelRecognizer Java Enumerations
description: The enumeration RawTextLineStatus of Dynamsoft LabelRecognizer describes the final status of a raw text line.
keywords: Raw Text Line Status
codeAutoHeight: true
---

# Enumeration RawTextLineStatus

`RawTextLineStatus` enumerates the final status of a raw text line.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumRawTextLineStatus {
    //Localized but recognition not performed.
    int RTLS_LOCALIZED = 0;
    //Recognition failed.
    int RTLS_RECOGNITION_FAILED = 1;
    //Successfully recognized.
    int RTLS_RECOGNITION_SUCCEEDED = 2;
}
```
