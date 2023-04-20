---
layout: default-layout
title: Class DMDLSConnectionParameters - Dynamsoft Label Recognizer Java Edition
description: This page shows the DMDLSConnectionParameters Class of Dynamsoft Core for Java Language.
keywords: DMDLSConnectionParameters, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---


# DMDLSConnectionParameters
Defines a struct to configure the parameters to connect to license tracking server.  

```java
class com.dynamsoft.core.DMDLSConnectionParameters
```  

## Attributes
    
| Attribute | Type |
|---------- | ---- |
| [`mainServerURL`](#mainserverurl) | *String* |
| [`standbyServerURL`](#standbyserverurl) | *String* |
| [`handshakeCode`](#handshakecode) | *String* |
| [`sessionPassword`](#sessionpassword) | *String* |
| [`deploymentType`](#deploymenttype) | *int* |
| [`chargeWay`](#chargeway) | *int* |
| [`UUIDGenerationMethod`](#uuidgenerationmethod) | *int* |
| [`maxBufferDays`](#maxbufferdays) | *int* |
| [`limitedLicenseModules`](#limitedlicensemodules) | *int[]* |
| [`maxConcurrentInstanceCount`](#maxconcurrentinstancecount) | *int* |
| [`organizationID`](#organizationid) | *String* |
| [`products`](#products) | *int* |


&nbsp;

### mainServerURL
The URL of the license tracking server.

```java
String  mainServerURL
```

**Value Range**

Any string value   

**Default value**

""

**Remarks**

If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to null (default value), it will connect to Dynamsoft's license tracking servers for online verification.   


&nbsp;

### standbyServerURL
The URL of the standby license tracking server.

```java
String  standbyServerURL
```

**Value Range**

Any string value   

**Default value**

""

**Remarks**

If you choose "Dynamsoft-hosting", then no need to change the value of MainServerURL and StandbyServerURL. When both are set to null (default value), it will connect to Dynamsoft's license tracking servers for online verification.   


&nbsp;

### handshakeCode
The handshake code.

```java
String  handshakeCode
```

**Value Range**

Any string value   

**Default value**

""

&nbsp;

### sessionPassword
The session password of the handshake code set in license tracking server.

```java
String  sessionPassword
```

**Value Range**

Any string value   

**Default value**

""

&nbsp;

### deploymentType

Sets the deployment type.

```java
int deploymentType
```

**Value Range**

Any one of the [`EnumDMDeploymentType`]({{ site.enumerations_old }}dm-deployment-type.html) Enumeration items.   

**Default value**

DM_DT_DESKTOP   

**See also**

[`EnumDMDeploymentType`]({{ site.enumerations_old }}dm-deployment-type.html)  


&nbsp;

### chargeWay
Sets the charge way.

```java
int chargeWay
```

**Value Range**

A value of [`EnumDMChargeWay`]({{ site.enumerations_old }}dm-charge-way.html) Enumeration items.

**Default value**

`DM_CW_AUTO`

**See also**

[`EnumDMChargeWay`]({{ site.enumerations_old }}dm-charge-way.html)
      

&nbsp;

### UUIDGenerationMethod
Sets the method to generate UUID.

```java
int UUIDGenerationMethod
```

**Value Range**

A value of [`EnumDMUUIDGenerationMethod`]({{ site.enumerations_old }}dm-uuid-generation-method.html) Enumeration items.

**Default value**

`DM_UUIDGM_RANDOM`

**See also**

[`EnumDMUUIDGenerationMethod`]({{ site.enumerations_old }}dm-uuid-generation-method.html)
      

&nbsp;

### maxBufferDays
Sets the max days to buffer the license info.

```java
int maxBufferDays
```

**Value Range**

[0,0x7fffffff]   

**Default value**

7

&nbsp;

### limitedLicenseModules
Sets the license modules to use.

```java
int[] limitedLicenseModules
```

**Value Range**

A list of the [`EnumDMLicenseModule`]({{ site.enumerations_old }}dm-license-module.html) Enumeration items.   

**Default value**

null

**See also**

[`EnumDMLicenseModule`]({{ site.enumerations_old }}dm-license-module.html)    
      

&nbsp;

### maxConcurrentInstanceCount
Sets the max concurrent instance count.

```java
int maxConcurrentInstanceCount
```

**Value Range**

[1,0x7fffffff]   

**Default value**

1
**Remarks**

It works only when [chargeWay](#chargeway) is setting to DM_CW_CONCURRENT_INSTANCE_COUNT
    It is the total number of instances used by multiple processes. For example, if there are two .EXE are running on the server and each .EXE may have 10 instances at most, then you should set maxConcurrentInstanceCount to 20.


&nbsp;

### organizationID
The organization ID got from Dynamsoft.

```java
String organizationID
```

**Value Range**

Any string value   

**Default value**

""

&nbsp;

### products
Sets the products to get the license for. Product values can be combined.

```java
int products
```

**Value Range**

A combine value of [`EnumProduct`]({{ site.enumerations_old }}product.html) Enumeration items.

**Default value**

`PROD_ALL`

**See also**

[`EnumProduct`]({{ site.enumerations_old }}product.html)