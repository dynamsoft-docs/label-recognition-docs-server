---
layout: default-layout
title: Main Page - Dynamsoft Label Recognition .Net API Reference
description: This is the main page of Dynamsoft Label Recognition for .Net API Reference.
keywords: api reference, .Net
needAutoGenerateSidebar: false
permalink: /programming/dotnet/api-reference/index-v1.0.html
---

# Dynamsoft Label Recognition - .Net API Reference

- [`LabelRecognition` Methods](#labelrecognition-methods) 
- [Classes](#classes)  
- [Enumerations](#enumerations)
- [Error Code](#error-code)

## LabelRecognition Methods

### General
   
  | Method               | Description |
  |----------------------|-------------|
  | [`GetVersion`](label-recognition/general.html#getversion) | Returns the version number string for the SDK. |
   
&nbsp; 

### Initialization
  
  | Method               | Description |
  |----------------------|-------------|
  | [`LabelRecognition`](label-recognition/initialization.html#labelrecognition) | Constructor of `LabelRecognition` object.|
  | [`Dispose`](label-recognition/initialization.html#dispose) | Destroys an instance of `LabelRecognition` object.|   
  | [`InitLicense`](label-recognition/initialization.html#initlicense) | Sets the license and activates the SDK. |
  | [`InitLicenseFromLTS`](label-recognition/initialization.html#initlicensefromlts) | Initializes the label recognition license and connects to the specified server for online verification. |

&nbsp; 

### Setting

  | Method               | Description |
  |----------------------|-------------|
  | [`GetRuntimeSettings`](label-recognition/settings.html#getruntimesettings) | Gets the current settings and saves it into a struct. |
  | [`UpdateRuntimeSettings`](label-recognition/settings.html#updateruntimesettings) | Updates runtime settings with a given struct. |
  | [`ResetRuntimeSettings`](label-recognition/settings.html#resetruntimesettings) | Resets the runtime settings. |
  | [`AppendSettingsFromString`](label-recognition/settings.html#appendsettingsfromstring) | Appends LabelRecognitionParameter settings in a string to the SDK object. |
  | [`OutputSettingsToFile`](label-recognition/settings.html#outputsettingstofile) | Outputs LabelRecognitionParameter settings into a file (JSON file). |
  | [`ClearAppendedSettings`](label-recognition/settings.html#clearappendedsettings) | Clear all appended LabelRecognitionParameter settings in the SDK object. |
  | [`UpdateReferenceRegionFromBarcodeResults`](label-recognition/settings.html#updatereferenceregionfrombarcoderesults) | Updates reference region which is defined with source type DLR_LST_BARCODE. |
  | [`GetModeArgument`](label-recognition/settings.html#getmodeargument) | Get argument value for the specified mode parameter. |
  | [`SetModeArgument`](label-recognition/settings.html#setmodeargument) | Set argument value for the specified mode parameter. |

&nbsp; 
   
### Recognizing
   
  | Method               | Description |
  |----------------------|-------------|
  | [`RecognizeByBuffer`](label-recognition/recognizing.html#recognizebybuffer) | Recognizes text from memory buffer containing image pixels in defined format. |
  | [`RecognizeByFile`](label-recognition/recognizing.html#recognizebyfile) | Recognizes text from a specified image file. |
   
&nbsp; 

## [Classes](class/index.html)
- [`DMLTSConnectionParameters`](class/dm-lts-connection-parameters.html)
- [`DLR_CharacterResult`](class/dlr-character-result.html)		
- [`DLR_Exception`](class/label-recognition-exception.html)	
- [`DLR_ImageData`](class/dlr-image-data.html)		
- [`DLR_LineResult`](class/dlr-line-result.html)	
- [`DLR_Quadrilateral`](class/dlr-quadrilateral.html)	
- [`DLR_ReferenceRegion`](class/dlr-reference-region.html)	
- [`DLR_Result`](class/dlr-result.html)		
- [`DLR_RuntimeSettings`](class/dlr-runtime-settings.html)	

&nbsp; 

## [Enumerations]({{ site.dlr_enumerations }})
- [`EnumDLRBarcodeFormat`]({{ site.dlr_enumerations }}other-enums.html#dlrbarcodeformat)
- [`EnumDLRBarcodeFormat_2`]({{ site.dlr_enumerations }}other-enums.html#dlrbarcodeformat_2)
- [`EnumDLRBinarizationMode`]({{ site.dlr_enumerations }}parameter-mode-enums.html#dlrbinarizationmode)
- [`EnumDLRGrayscaleTransformationMode`]({{ site.dlr_enumerations }}parameter-mode-enums.html#dlrgrayscaletransformationmode)
- [`EnumDLRImagePixelFormat`]({{ site.dlr_enumerations }}other-enums.html#dlrimagepixelformat)
- [`EnumDLRLocalizationSourceType`]({{ site.dlr_enumerations }}other-enums.html#dlrlocalizationsourcetype)
- [`EnumDLRRegionPredetectionMode`]({{ site.dlr_enumerations }}parameter-mode-enums.html#dlrregionpredetectionmode)
- [`EnumDMChargeWay`]({{ site.dlr_enumerations }}other-enums.html#dm_chargeway)	
- [`EnumDMDeploymentType`]({{ site.dlr_enumerations }}other-enums.html#dm_deploymenttype)	
- [`EnumDMLicenseModule`]({{ site.dlr_enumerations }}other-enums.html#dm_licensemodule)	
- [`EnumDMUUIDGenerationMethod`]({{ site.dlr_enumerations }}other-enums.html#dm_uuidgenerationmethod)	

&nbsp; 

## [Error Code]({{ site.dlr_enumerations }}error-code.html)
		
