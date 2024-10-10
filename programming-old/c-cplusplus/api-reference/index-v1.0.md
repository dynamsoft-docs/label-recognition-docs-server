---
layout: default-layout
title: Main Page - Dynamsoft Label Recognition C/C++ API Reference
description: This is the main page of Dynamsoft Label Recognition for C/C++ API Reference.
keywords: api reference, c, c++
needAutoGenerateSidebar: false
permalink: /programming/c-cplusplus/api-reference/index-v1.0.html
---

# Dynamsoft Label Recognition - C/C++ API Reference

- [`CLabelRecognition` Class](#clabelrecognition-class) 
- [C Functions](#c-functions)
- [Enumerations](#enumerations)
- [Error Code](#error-code)
- [Structs](#structs)  

## CLabelRecognition Class

### General
   
  | Method               | Description |
  |----------------------|-------------|
  | [`GetErrorString`](c-label-recognition-class/general.html#geterrorstring) | Returns the error string. |
  | [`GetVersion`](c-label-recognition-class/general.html#getversion) | Returns the version number string for the SDK. |
   
&nbsp; 

### Initialization
  
  | Method               | Description |
  |----------------------|-------------|
  | [`InitLicense`](c-label-recognition-class/initialization.html#initlicense) | Sets the license and activates the SDK. |
  | [`InitLTSConnectionParameters`](c-label-recognition-class/initialization.html#initltsconnectionparameters) | Initializes a DM_LTSConnectionParameters struct with default values. |
  | [`InitLicenseFromLTS`](c-label-recognition-class/initialization.html#initlicensefromlts) | Initializes the label recognition license and connects to the specified server for online verification. |

&nbsp; 

### Setting

  | Method               | Description |
  |----------------------|-------------|
  | [`GetRuntimeSettings`](c-label-recognition-class/settings.html#getruntimesettings) | Gets the current settings and saves it into a struct. |
  | [`UpdateRuntimeSettings`](c-label-recognition-class/settings.html#updateruntimesettings) | Updates runtime settings with a given struct. |
  | [`ResetRuntimeSettings`](c-label-recognition-class/settings.html#resetruntimesettings) | Resets the runtime settings. |
  | [`AppendSettingsFromString`](c-label-recognition-class/settings.html#appendsettingsfromstring) | Appends LabelRecognitionParameter settings in a string to the SDK object. |
  | [`OutputSettingsToFile`](c-label-recognition-class/settings.html#outputsettingstofile) | Outputs LabelRecognitionParameter settings into a file (JSON file). |
  | [`ClearAppendedSettings`](c-label-recognition-class/settings.html#clearappendedsettings) | Clear all appended LabelRecognitionParameter settings in the SDK object. |
  | [`UpdateReferenceRegionFromBarcodeResults`](c-label-recognition-class/settings.html#updatereferenceregionfrombarcoderesults) | Updates reference region which is defined with source type DLR_LST_BARCODE. |
  | [`GetModeArgument`](c-label-recognition-class/settings.html#getmodeargument) | Get argument value for the specified mode parameter. |
  | [`SetModeArgument`](c-label-recognition-class/settings.html#setmodeargument) | Set argument value for the specified mode parameter. |

&nbsp; 
   
### Recognizing
   
  | Method               | Description |
  |----------------------|-------------|
  | [`RecognizeByBuffer`](c-label-recognition-class/recognizing.html#recognizebybuffer) | Recognizes text from memory buffer containing image pixels in defined format. |
  | [`RecognizeByFile`](c-label-recognition-class/recognizing.html#recognizebyfile) | Recognizes text from a specified image file. |
   
&nbsp; 
   
### Result
   
  | Method               | Description |
  |----------------------|-------------|
  | [`GetAllDLRResults`](c-label-recognition-class/result.html#getalldlrresults) | Gets all recognized results. |
  | [`FreeDLRResults`](c-label-recognition-class/result.html#freedlrresults) | Frees memory allocated for recognized results. |
   
&nbsp; 

## C Functions
  
### General
   
  | Method               | Description |
  |----------------------|-------------|
  | [`DLR_GetErrorString`](c-functions/general.html#dlr_geterrorstring) | Returns the error string. |
  | [`DLR_GetVersion`](c-functions/general.html#dlr_getversion) | Returns the version number string for the SDK. |
   
&nbsp; 

### Initialization
  
  | Method               | Description |
  |----------------------|-------------|
  | [`DLR_CreateInstance`](c-functions/initialization.html#dlr_createinstance) | Creates a Dynamsoft Label Recognition instance. |
  | [`DLR_DestroyInstance`](c-functions/initialization.html#dlr_destroyinstance) | Destroys an instance of Dynamsoft Label Recognition. |
  | [`DLR_InitLicense`](c-functions/initialization.html#dlr_initlicense) | Sets the license and activates the SDK. |
  | [`DLR_InitLTSConnectionParameters`](c-functions/initialization.html#dlr_initltsconnectionparameters) | Initializes a DM_LTSConnectionParameters struct with default values. |
  | [`DLR_InitLicenseFromLTS`](c-functions/initialization.html#dlr_initlicensefromlts) | Initializes the label recognition license and connects to the specified server for online verification. |

&nbsp; 

### Setting

  | Method               | Description |
  |----------------------|-------------|
  | [`DLR_GetRuntimeSettings`](c-functions/settings.html#dlr_getruntimesettings) | Gets the current settings and saves it into a struct. |
  | [`DLR_UpdateRuntimeSettings`](c-functions/settings.html#dlr_updateruntimesettings) | Updates runtime settings with a given struct. |
  | [`DLR_ResetRuntimeSettings`](c-functions/settings.html#dlr_resetruntimesettings) | Resets the runtime settings. |
  | [`DLR_AppendSettingsFromString`](c-functions/settings.html#dlr_appendsettingsfromstring) | Appends LabelRecognitionParameter settings in a string to the SDK object. |
  | [`DLR_OutputSettingsToFile`](c-functions/settings.html#dlr_outputsettingstofile) | Outputs LabelRecognitionParameter settings into a file (JSON file). |
  | [`DLR_ClearAppendedSettings`](c-functions/settings.html#dlr_appendsettingsfromstring) | Clears appended LabelRecognitionParameter settings. |
  | [`DLR_GetModeArgument`](c-functions/settings.html#dlr_getmodeargument) | Get argument value for the specified mode parameter. |
  | [`DLR_SetModeArgument`](c-functions/settings.html#dlr_setmodeargument) | Set argument value for the specified mode parameter. |

&nbsp; 
   
### Recognizing
   
  | Method               | Description |
  |----------------------|-------------|
  | [`DLR_RecognizeByBuffer`](c-functions/recognizing.html#dlr_recognizebybuffer) | Recognizes text from memory buffer containing image pixels in defined format. |
  | [`DLR_RecognizeByFile`](c-functions/recognizing.html#dlr_recognizebyfile) | Recognizes text from a specified image file. |
   
&nbsp; 
   
### Result
   
  | Method               | Description |
  |----------------------|-------------|
  | [`DLR_GetAllDLRResults`](c-functions/result.html#dlr_getalldlrresults) | Gets all recognized results. |
  | [`DLR_FreeDLRResults`](c-functions/result.html#dlr_freedlrresults) | Frees memory allocated for recognized results. |
   
&nbsp; 

## [Enumerations]({{ site.dlr_enumerations }})
- [`DLRBarcodeFormat`]({{ site.dlr_enumerations }}other-enums.html#dlrbarcodeformat)
- [`DLRBarcodeFormat_2`]({{ site.dlr_enumerations }}other-enums.html#dlrbarcodeformat_2)
- [`DLRBinarizationMode`]({{ site.dlr_enumerations }}parameter-mode-enums.html#dlrbinarizationmode)
- [`DLRGrayscaleTransformationMode`]({{ site.dlr_enumerations }}parameter-mode-enums.html#dlrgrayscaletransformationmode)
- [`DLRImagePixelFormat`]({{ site.dlr_enumerations }}other-enums.html#dlrimagepixelformat)
- [`DLRLocalizationSourceType`]({{ site.dlr_enumerations }}other-enums.html#dlrlocalizationsourcetype)
- [`DLRRegionPredetectionMode`]({{ site.dlr_enumerations }}parameter-mode-enums.html#dlrregionpredetectionmode)
- [`DM_ChargeWay`]({{ site.dlr_enumerations }}other-enums.html#dm_chargeway)	
- [`DM_DeploymentType`]({{ site.dlr_enumerations }}other-enums.html#dm_deploymenttype)	
- [`DM_LicenseModule`]({{ site.dlr_enumerations }}other-enums.html#dm_licensemodule)	
- [`DM_UUIDGenerationMethod`]({{ site.dlr_enumerations }}other-enums.html#dm_uuidgenerationmethod)	


## [Error Code]({{ site.dlr_enumerations }}error-code.html)
		
## [Structs](structs/index.html)
- [`DLRRuntimeSettings`](structs/dlr-runtime-settings.html)	
- [`DLRQuadrilateral`](structs/dlr-quadrilateral.html)	
- [`DLRReferenceRegion`](structs/dlr-reference-region.html)	
- [`DLRResultArray`](structs/dlr-result-array.html)		
- [`DLRResult`](structs/dlr-result.html)		
- [`DLRLineResult`](structs/dlr-line-result.html)	
- [`DLRCharacterResult`](structs/dlr-character-result.html)		
- [`DLRPoint`](structs/dlr-point.html)		
- [`DLRImageData`](structs/dlr-image-data.html)		