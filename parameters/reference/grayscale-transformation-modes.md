---
layout: default-layout
title: GrayscaleTransformationModes - Dynamsoft Barcode Reader Parameter Reference
description: This page shows Dynamsoft Barcode Reader Parameter Reference for GrayscaleTransformationModes.
keywords: GrayscaleTransformationModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/grayscale-transformation-modes.html
---


# GrayscaleTransformationModes 

This parameter helps control the colour mode of the grayscale image. This parameter is very important when trying to read inverted barcodes. Barcodes typically are dark on a light background, but sometimes they might be inverted, resulting in a light barcode on a dark background. By default, the library is configured to detect the former. So if you are working with inverted barcodes, `GrayscaleTransformationModes` is the parameter to deal with them.

It consists of one or more modes, each mode represents a way to transform the grayscale image.


## Candidate Mode List
- GTM_ORIGINAL
- GTM_INVERTED

### GTM_ORIGINAL
Keeps the original grayscale. This mode has the following arguments for further customization.

- [LibraryFileName](#libraryfilename)
- [LibraryParameters](#libraryparameters)

### GTM_INVERTED
Transforms the image to inverted grayscale. This mode is the one to use for inverted barcodes. It also has the following arguments for further customization.

- [LibraryFileName](#libraryfilename)
- [LibraryParameters](#libraryparameters)

    
## Setting Methods

### As `PublicRuntimeSettings` Member
`GrayscaleTransformationModes` can be set dynamically during runtime as a member of `FurtherModes`, which is a member of `PublicRuntimeSettings` struct, it is an array with 8 `GrayscaleTransformationMode` Enumeration items.


**Code Snippet in C++**
```cpp
//...other codes
PublicRuntimeSettings* pSettings = new PublicRuntimeSettings;
int errorCode = reader->GetRuntimeSettings(pSettings);
pSettings->grayscaleTransformationModes[0] = GTM_ORIGINAL;
reader->UpdateRuntimeSettings(pSettings);
delete pSettings;
//...other codes
```


**Remarks**     
`GetModeArgument` and `SetModeArgument` need to be called for getting and setting [`Arguments`](#candidate-argument-list).


**See Also**      
- `FurtherModes:` [C]({{ site.structs }}FurtherModes.html?src=c) \| [C++]({{ site.structs }}FurtherModes.html?src=cpp) \| [.NET]({{ site.dotnet_api }}struct/FurtherModes.html) \| [Java]({{ site.java_api }}class/FurtherModes.html) \| [Java-Android]({{ site.android_api }}auxiliary-FurtherModes.html) \| [Objective-C & Swift]({{ site.oc_api }}auxiliary-iFurtherModes.html)
- `PublicRuntimeSettings:` [JavaScript]({{ site.js_api }}interface/RuntimeSettings.html) \| [C]({{ site.structs }}PublicRuntimeSettings.html?src=c) \| [C++]({{ site.structs }}PublicRuntimeSettings.html?src=cpp) \| [.NET]({{ site.dotnet_api }}struct/PublicRuntimeSettings.html) \| [Python]({{ site.python_api }}class/PublicRuntimeSettings.html) \| [Java]({{ site.java_api }}class/PublicRuntimeSettings.html) \| [Java-Android]({{ site.android_api }}auxiliary-PublicRuntimeSettings.html) \| [Objective-C & Swift]({{ site.oc_api }}auxiliary-iPublicRuntimeSettings.html)
- `GrayscaleTransformationMode:` [JavaScript]({{ site.js_enumerations }}EnumGrayscaleTransformationMode.html) \| [C]({{ site.c_cpp_enumerations }}parameter-mode-enums.html?src=c#grayscaletransformationmode) \| [C++]({{ site.c_cpp_enumerations }}parameter-mode-enums.html?src=cpp#grayscaletransformationmode) \| [.NET]({{ site.dotnet_enumerations }}parameter-mode-enums.html#grayscaletransformationmode) \| [Python]({{ site.python_enumerations }}parameter-mode-enums.html#grayscaletransformationmode) \| [Java]({{ site.java_enumerations }}parameter-mode-enums.html#grayscaletransformationmode) \| [Java-Android]({{ site.mobile_enumerations }}grayscale-transformation-mode.html?lang=android) \| [Objective-C & Swift]({{ site.mobile_enumerations }}grayscale-transformation-mode.html?lang=objc,swift)
- `GetModeArgument:` [JavaScript]({{ site.js_api}}BarcodeReader.html#getmodeargument) \| [C]({{ site.c_methods }}parameter-and-runtime-settings-basic.html#dbr_getmodeargument) \| [C++]({{ site.cpp_methods }}parameter-and-runtime-settings-basic.html#getmodeargument) \| [.NET]({{ site.dotnet_api }}BarcodeReader/parameter-and-runtime-settings-basic.html#getmodeargument) \| [Python]({{ site.python_api }}BarcodeReader/parameter-and-runtime-settings-basic.html#get_mode_argument) \| [Java]({{ site.java_api }}BarcodeReader/parameter-and-runtime-settings-basic.html#getmodeargument) \| [Java-Android]({{ site.android_api }}primary-parameter-and-runtime-settings-basic.html#getmodeargument) \| [Objective-C & Swift]({{ site.oc_api }}primary-parameter-and-runtime-settings-basic.html#getmodeargument)
- `SetModeArgument:` [JavaScript]({{ site.js_api}}BarcodeReader.html#setmodeargument) \| [C]({{ site.c_methods }}parameter-and-runtime-settings-basic.html#dbr_setmodeargument) \| [C++]({{ site.cpp_methods }}parameter-and-runtime-settings-basic.html#setmodeargument) \| [.NET]({{ site.dotnet_api }}BarcodeReader/parameter-and-runtime-settings-basic.html#setmodeargument) \| [Python]({{ site.python_api }}BarcodeReader/parameter-and-runtime-settings-basic.html#set_mode_argument) \| [Java]({{ site.java_api }}BarcodeReader/parameter-and-runtime-settings-basic.html#setmodeargument) \| [Java-Android]({{ site.android_api }}primary-parameter-and-runtime-settings-basic.html#setmodeargument) \| [Objective-C & Swift]({{ site.oc_api }}primary-parameter-and-runtime-settings-basic.html#setmodeargument)


### As JSON Parameter
`GrayscaleTransformationModes` as a JSON parameter is a JSON Object array. Each JSON object is defined as below.   

| Key Name | Key Value | Description |
| -------- | --------- | ----------- |
| Mode | Any one in Candidate Mode List as string | (Required) Specifies a mode for grayscale transformation.  |
| LibraryFileName | A string from value range of LibraryFileName | (Optional) Sets the Argument [LibraryFileName](#libraryfilename). |
| LibraryParameters | A string from value range of LibraryParameters | (Optional) Sets the Argument [LibraryParameters](#libraryparameters). |



**JSON Parameter Example**   
```
{
    "GrayscaleTransformationModes": [
        {
            "Mode": "GTM_ORIGINAL"
        },
        {
            "Mode": "GTM_INVERTED" 
        }
    ]
}
```


<!--
## Impacts on Performance
### Speed
The SDK will loop the setting modes one by one until find as many barcodes as `ExpectedBarcodesCount` specified or timeout. The more modes you set, the more time the process may take. Setting an appropriate mode first in order or setting only necessary modes may speed up the process.

### Read Rate
Setting more modes along with different arguments may improve the Read Rate. 

### Accuracy
`GrayscaleTransformationModes` has no influence on the Accuracy.

-->
## Candidate Argument List
- [LibraryFileName](#libraryfilename)
- [LibraryParameters](#libraryparameters)
 


### LibraryFileName 
Sets the file name of the library to load dynamically.

| Value Type | Value Range | Default Value | Valid For | 
| ---------- | ----------- | ------------- | --------- |
| *string* | A string value representing file name. | "" | All modes |         


**Remarks**         
  The library must be in the same place with Dynamsoft Barcode Reader Library.


### LibraryParameters 
Sets the parameters passed to the library to load dynamically.

| Value Type | Value Range | Default Value | Valid For | 
| ---------- | ----------- | ------------- | ----------- |
| *string* | A string value representing parameters. | "" | All modes |         


## Related Articles
- [Use RuntimeSettings or Templates for Configuring Parameters]({{ site.features }}use-runtimesettings-or-templates.html)
- [How to configure GrayscaleTransformationModes]({{ site.scenario_settings }}image-scale-and-colour-conversion.html#grayscale-colour-inversion-transformation)
