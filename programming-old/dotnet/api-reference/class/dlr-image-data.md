---
layout: default-layout
title: DLR_ImageData - Dynamsoft Label Recognition .Net Class
description: This page shows the DLR_ImageData struct of Dynamsoft Label Recognition for .Net Language.
keywords: DLR_ImageData, .Net
needAutoGenerateSidebar: true
permalink: /programming/dotnet/api-reference/class/dlr-image-data.html
---


# DLR_ImageData
Stores the image data.  


## Attributes
    
| Attribute | Type |
|---------- | ---- |
| [`Bytes`](#bytes) | *byte[]* |
| [`Width`](#width) | *int* |
| [`Height`](#height) | *int* |
| [`Stride`](#stride) | *int* |
| [`Format`](#format) | [`EnumDLRImagePixelFormat`]({{ site.dlr_enumerations }}other-enums.html#dlrimagepixelformat) |


### Bytes
The image data content in a byte array. 
```csharp
byte[] Dynamsoft.DLR.DLR_ImageData.Bytes
```

### Width
The width of the image in pixels.  
```csharp
int Dynamsoft.DLR.DLR_ImageData.Width
```

### Height
The height of the image in pixels.  
```csharp
int Dynamsoft.DLR.DLR_ImageData.Height
```

### Stride
The stride (or scan width) of the image. 
```csharp
int Dynamsoft.DLR.DLR_ImageData.Stride
```

### Format
The image pixel format used in the image byte array. 
```csharp
EnumDLRImagePixelFormat Dynamsoft.DLR.DLR_ImageData.Format
```
  

