---
layout: default-layout
title: Class DLRImageData - Dynamsoft Label Recognizer Java Edition
description: This page shows the DLRImageData struct of Dynamsoft Label Recognition for Java Language.
keywords: DLRImageData, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/java/api-reference/dlr-image-data.html
---


# DLRImageData
Stores the image data.  

```java
class com.dynamsoft.dlr.DLRImageData
```

## Attributes
    
| Attribute | Type |
|---------- | ---- |
| [`bytes`](#bytes) | *byte[]* |
| [`width`](#width) | *int* |
| [`height`](#height) | *int* |
| [`stride`](#stride) | *int* |
| [`format`](#format) | [`DLRImagePixelFormat`]({{ site.enumerations_old }}other-enums.html#dlrimagepixelformat) |


&nbsp;

### bytes
The image data content in a byte array. 
```java
byte[] bytes
```

&nbsp;

### width
The width of the image in pixels.  
```java
int width
```

&nbsp;

### height
The height of the image in pixels.  
```java
int height
```

&nbsp;

### stride
The stride (or scan width) of the image. 
```java
int stride
```

&nbsp;

### format
The image pixel format used in the image byte array. 
```java
DLRImagePixelFormat format
```
  

