---
layout: default-layout
title: CLabelRecognition Class - Dynamsoft Label Recognition C++ API Reference
description: This page shows CLabelRecognition methods of Dynamsoft Label Recognition for C++ API Reference.
keywords: api reference, c++
needAutoGenerateSidebar: false
permalink: /programming/c-cplusplus/api-reference/c-label-recognition-class/index-v1.0.html
---


# Dynamsoft Label Recognition - CLabelRecognition Class

## General
   
  | Method               | Description |
  |----------------------|-------------|
  | [`GetErrorString`](general.html#geterrorstring) | Returns the error string. |
  | [`GetVersion`](general.html#getversion) | Returns the version number string for the SDK. |
   
&nbsp; 

## Initialization
  
  | Method               | Description |
  |----------------------|-------------|
  | [`InitLicense`](initialization.html#initlicense) | Sets the license and activates the SDK. |
  | [`InitLTSConnectionParameters`](initialization.html#initltsconnectionparameters) | Initializes a DM_LTSConnectionParameters struct with default values. |
  | [`InitLicenseFromLTS`](initialization.html#initlicensefromlts) | Initializes the label recognition license and connects to the specified server for online verification. |

&nbsp; 

## Setting

  | Method               | Description |
  |----------------------|-------------|
  | [`GetRuntimeSettings`](settings.html#getruntimesettings) | Gets the current settings and saves it into a struct. |
  | [`UpdateRuntimeSettings`](settings.html#updateruntimesettings) | Updates runtime settings with a given struct. |
  | [`ResetRuntimeSettings`](settings.html#resetruntimesettings) | Resets the runtime settings. |
  | [`AppendSettingsFromString`](settings.html#appendsettingsfromstring) | Appends LabelRecognitionParameter settings in a string to the SDK object. |
  | [`OutputSettingsToFile`](settings.html#outputsettingstofile) | Outputs LabelRecognitionParameter settings into a file (JSON file). |
  | [`ClearAppendedSettings`](settings.html#clearappendedsettings) | Clear all appended LabelRecognitionParameter settings in the SDK object. |
  | [`UpdateReferenceRegionFromBarcodeResults`](settings.html#updatereferenceregionfrombarcoderesults) | Updates reference region which is defined with source type DLR_LST_BARCODE. |
  | [`GetModeArgument`](settings.html#getmodeargument) | Get argument value for the specified mode parameter. |
  | [`SetModeArgument`](settings.html#setmodeargument) | Set argument value for the specified mode parameter. |

&nbsp; 
   
## Recognizing
   
  | Method               | Description |
  |----------------------|-------------|
  | [`RecognizeByBuffer`](recognizing.html#recognizebybuffer) | Recognizes text from memory buffer containing image pixels in defined format. |
  | [`RecognizeByFile`](recognizing.html#recognizebyfile) | Recognizes text from a specified image file. |
   
&nbsp; 
   
## Result
   
  | Method               | Description |
  |----------------------|-------------|
  | [`GetAllDLRResults`](result.html#getalldlrresults) | Gets all recognized results. |
  | [`FreeDLRResults`](result.html#freedlrresults) | Frees memory allocated for recognized results. |
   
&nbsp; 

