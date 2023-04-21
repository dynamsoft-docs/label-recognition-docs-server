---
layout: default-layout
title: DM_LTSConnectionParameters - Dynamsoft Label Recognition C & C++ Struct
description: This page shows the DM_LTSConnectionParameters struct of Dynamsoft Label Recognition for C & C++ Language.
keywords: DM_LTSConnectionParameters, struct, c, c++
needAutoGenerateSidebar: true
permalink: /programming/c-cplusplus/api-reference/structs/dm-lts-connection-parameters.html
---


# DM_LTSConnectionParameters
Defines a struct to configure the parameters to connect to license tracking server.  

## Typedefs

```cpp
typedef struct tagDM_LTSConnectionParameters  DM_LTSConnectionParameters
```

---

## Attributes
    
| Attribute | Type |
|---------- | ---- |
| [`mainServerURL`](#mainserverurl) | *char\** |
| [`standbyServerURL`](#standbyserverurl) | *char\** |
| [`handshakeCode`](#handshakecode) | *char\** |
| [`sessionPassword`](#sessionpassword) | *char\** |
| [`deploymentType`](#deploymenttype) | [`DM_DeploymentType`]({{ site.enumerations_old }}other-enums.html#dm_deploymenttype) |
| [`chargeWay`](#chargeway) | [`DM_ChargeWay`]({{ site.enumerations_old }}other-enums.html#dm_chargeway) |
| [`UUIDGenerationMethod`](#uuidgenerationmethod) | [`DM_UUIDGenerationMethod`]({{ site.enumerations_old }}other-enums.html#dm_uuidgenerationmethod) |
| [`maxBufferDays`](#maxbufferdays) | *int* |
| [`limitedLicenseModulesCount`](#limitedlicensemodulescount) | *int* |
| [`limitedLicenseModules`](#limitedlicensemodules) | [`DM_LicenseModule*`]({{ site.enumerations_old }}other-enums.html#dm_licensemodule) |
| [`maxConcurrentInstanceCount`](#maxconcurrentinstancecount) | *int* |
| [`organizationID`](#organizationID) | *char\** |
| [`products`](#products) | *int* |
| [`reserved`](#reserved) | *char\[52\]* |


### mainServerURL
The URL of the license tracking server.
```cpp
char*  DM_LTSConnectionParameters::mainServerURL
```

**Value Range**

Any string value   

**Default value**

NULL

**Remarks**

If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to NULL (default value), it will connect to Dynamsoft's license tracking servers for online verification.   


### standbyServerURL
The URL of the standby license tracking server.
```cpp
char*  DM_LTSConnectionParameters::standbyServerURL
```

**Value Range**

Any string value   

**Default value**

NULL

**Remarks**

If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to NULL (default value), it will connect to Dynamsoft's license tracking servers for online verification.   


### handshakeCode
The handshake code.
```cpp
char*  DM_LTSConnectionParameters::handshakeCode
```

**Value Range**

Any string value   

**Default value**

NULL

### sessionPassword
The session password of the handshake code set in license tracking server.
```cpp
char*  DM_LTSConnectionParameters::sessionPassword
```

**Value Range**

Any string value   

**Default value**

NULL

### deploymentType
Sets the deployment type.
```cpp
DM_DeploymentType DM_LTSConnectionParameters::deploymentType
```

**Value Range**

A value of [`DM_DeploymentType`]({{ site.enumerations_old }}other-enums.html#dm_deploymenttype) Enumeration items.

**Default value**

`DM_DT_DESKTOP`

**See also**

[`DM_DeploymentType`]({{ site.enumerations_old }}other-enums.html#dm_deploymenttype)
      

### chargeWay
Sets the charge way.
```cpp
DM_ChargeWay DM_LTSConnectionParameters::chargeWay
```

**Value Range**

A value of [`DM_ChargeWay`]({{ site.enumerations_old }}other-enums.html#dm_chargeway) Enumeration items.

**Default value**

`DM_CW_AUTO`

**See also**

[`DM_ChargeWay`]({{ site.enumerations_old }}other-enums.html#dm_chargeway)
      

### UUIDGenerationMethod
Sets the method to generate UUID.
```cpp
DM_UUIDGenerationMethod DM_LTSConnectionParameters::UUIDGenerationMethod
```

**Value Range**

A value of [`DM_UUIDGenerationMethod`]({{ site.enumerations_old }}other-enums.html#dm_uuidgenerationmethod) Enumeration items.

**Default value**

`DM_UUIDGM_RANDOM`

**See also**

[`DM_UUIDGenerationMethod`]({{ site.enumerations_old }}other-enums.html#dm_uuidgenerationmethod)
      

### maxBufferDays
Sets the max days to buffer the license info.
```cpp
int DM_LTSConnectionParameters::maxBufferDays
```

**Value Range**

[0,0x7fffffff]   

**Default value**

0

### limitedLicenseModulesCount
Sets the count of license modules to use.
```cpp
int DM_LTSConnectionParameters::limitedLicenseModulesCount
```

**Value Range**

[0,0x7fffffff]   

**Default value**

0

### limitedLicenseModules
Sets the license modules to use.
```cpp
DM_LicenseModule* DM_LTSConnectionParameters::limitedLicenseModules
```

**Value Range**

Each array item can be any one of the [`DM_LicenseModule`]({{ site.enumerations_old }}other-enums.html#dm_licensemodule) Enumeration items.

**Default value**

NULL

**See also**

[`DM_LicenseModule`]({{ site.enumerations_old }}other-enums.html#dm_licensemodule)

### maxConcurrentInstanceCount
Sets the max concurrent instance count.
```cpp
int DM_LTSConnectionParameters::maxConcurrentInstanceCount
```

**Value Range**

[1,0x7fffffff]   

**Default value**

1
**Remarks**

It works only when [chargeWay](#chargeway) is setting to DM_CW_CONCURRENT_INSTANCE_COUNT.<br>
    It is the total number of instances used by multiple processes. For example, if there are two .EXE are running on the server and each .EXE may have 10 instances at most, then you should set maxConcurrentInstanceCount to 20.

### organizationID
The organization ID got from Dynamsoft.
```cpp
char* DM_LTSConnectionParameters::organizationID
```

**Value Range**

Any string value   

**Default value**

NULL

### products
Sets the products to get the license for. Product values can be combined.
```cpp
int DM_LTSConnectionParameters::products
```

**Value Range**

A combine value of [`Product`]({{ site.enumerations_old }}other-enums.html#product) Enumeration items.

**Default value**

`PROD_ALL`

**See also**

[`Product`]({{ site.enumerations_old }}other-enums.html#product)

### reserved
Reserved memory for the struct. The length of this array indicates the size of the memory reserved for this struct.
```cpp
char DM_LTSConnectionParameters::reserved[52]
```
