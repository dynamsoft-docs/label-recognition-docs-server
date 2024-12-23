---
layout: default-layout
title: C Functions - Dynamsoft Label Recognition C API Reference
description: This page shows all methods of Dynamsoft Label Recognition for C API Reference.
keywords: api reference, c
needAutoGenerateSidebar: false
permalink: /programming/c-cplusplus/api-reference/c-functions/index-v1.0.html
---


# Dynamsoft Label Recognition - C Functions
  
## General
   
  | Method               | Description |
  |----------------------|-------------|
  | [`DLR_GetErrorString`](general.html#dlr_geterrorstring) | Returns the error string. |
  | [`DLR_GetVersion`](general.html#dlr_getversion) | Returns the version number string for the SDK. |
   
&nbsp; 

## Initialization
  
  | Method               | Description |
  |----------------------|-------------|
  | [`DLR_CreateInstance`](initialization.html#dlr_createinstance) | Creates a Dynamsoft Label Recognition instance. |
  | [`DLR_DestroyInstance`](initialization.html#dlr_destroyinstance) | Destroys an instance of Dynamsoft Label Recognition. |
  | [`DLR_InitLicense`](initialization.html#dlr_initlicense) | Sets the license and activates the SDK. |
  | [`DLR_InitLTSConnectionParameters`](initialization.html#dlr_initltsconnectionparameters) | Initializes a DM_LTSConnectionParameters struct with default values. |
  | [`DLR_InitLicenseFromLTS`](initialization.html#dlr_initlicensefromlts) | Initializes the label recognition license and connects to the specified server for online verification. |

&nbsp; 

## Setting

  | Method               | Description |
  |----------------------|-------------|
  | [`DLR_GetRuntimeSettings`](settings.html#dlr_getruntimesettings) | Gets the current settings and saves it into a struct. |
  | [`DLR_UpdateRuntimeSettings`](settings.html#dlr_updateruntimesettings) | Updates runtime settings with a given struct. |
  | [`DLR_ResetRuntimeSettings`](settings.html#dlr_resetruntimesettings) | Resets the runtime settings. |
  | [`DLR_AppendSettingsFromString`](settings.html#dlr_appendsettingsfromstring) | Appends LabelRecognitionParameter settings in a string to the SDK object. |
  | [`DLR_OutputSettingsToFile`](settings.html#dlr_outputsettingstofile) | Outputs LabelRecognitionParameter settings into a file (JSON file). |
  | [`DLR_ClearAppendedSettings`](settings.html#dlr_appendsettingsfromstring) | Clears appended LabelRecognitionParameter settings. |
  | [`DLR_UpdateReferenceRegionFromBarcodeResults`](settings.html#dlr_updatereferenceregionfrombarcoderesults) | Updates reference region which is defined with source type DLR_LST_BARCODE. |
  | [`DLR_GetModeArgument`](settings.html#dlr_getmodeargument) | Get argument value for the specified mode parameter. |
  | [`DLR_SetModeArgument`](settings.html#dlr_setmodeargument) | Set argument value for the specified mode parameter. |

&nbsp; 
   
## Recognizing
   
  | Method               | Description |
  |----------------------|-------------|
  | [`DLR_RecognizeByBuffer`](recognizing.html#dlr_recognizebybuffer) | Recognizes text from memory buffer containing image pixels in defined format. |
  | [`DLR_RecognizeByFile`](recognizing.html#dlr_recognizebyfile) | Recognizes text from a specified image file. |
   
&nbsp; 
   
## Result
   
  | Method               | Description |
  |----------------------|-------------|
  | [`DLR_GetAllDLRResults`](result.html#dlr_getalldlrresults) | Gets all recognized results. |
  | [`DLR_FreeDLRResults`](result.html#dlr_freedlrresults) | Frees memory allocated for recognized results. |
   
&nbsp; 

