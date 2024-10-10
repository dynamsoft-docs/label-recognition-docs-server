---
layout: default-layout
title: LabelRecognition Class - Dynamsoft Label Recognition .Net API Reference
description: This page shows LabelRecognition methods of Dynamsoft Label Recognition for .Net API Reference.
keywords: api reference, .Net
needAutoGenerateSidebar: false
permalink: /programming/dotnet/api-reference/label-recognition/index-v1.0.html
---


# Dynamsoft Label Recognition - LabelRecognition Class

## General
   
  | Method               | Description |
  |----------------------|-------------|
  | [`GetVersion`](general.html#getversion) | Returns the version number string for the SDK. |
   
&nbsp; 

## Initialization
  
  | Method               | Description |
  |----------------------|-------------|
  | [`LabelRecognition`](initialization.html#labelrecognition) | Initialization of `LabelRecognition` object.|
  | [`Dispose`](initialization.html#dispose) | Destroys an instance of `LabelRecognition` object.|   
  | [`InitLicense`](initialization.html#initlicense) | Sets the license and activates the SDK. |
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
   