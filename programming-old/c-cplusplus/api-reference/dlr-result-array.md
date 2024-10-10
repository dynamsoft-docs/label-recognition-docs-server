---
layout: default-layout
title: DLR_ResultArray - Dynamsoft Label Recognizer C & C++ Struct
description: This page shows the DLR_ResultArray struct of Dynamsoft Label Recognizer for C & C++ Language.
keywords: DLR_ResultArray, struct, c, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/c-cplusplus/api-reference/dlr-result-array.html
---

# DLR_ResultArray
Stores the DLR_ResultArray array.  


```cpp
typedef struct tagDLR_ResultArray  DLR_ResultArray
```  
  

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`results`](#results) | [`PDLR_Result`](dlr-result.html)\* |
| [`resultsCount`](#resultscount) | *int* |



&nbsp;

### results
The DLR_Result array.
```cpp
PDLR_Result* results
```

&nbsp;

### resultsCount
The total count of DLR_Result.
```cpp
int resultsCount
```
