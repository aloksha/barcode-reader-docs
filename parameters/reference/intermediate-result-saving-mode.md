---
layout: default-layout
title: IntermediateResultSavingMode - Dynamsoft Barcode Reader Parameter Reference
description: This page shows Dynamsoft Barcode Reader Parameter Reference for IntermediateResultSavingMode.
keywords: IntermediateResultSavingMode, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/intermediate-result-saving-mode.html
---


# IntermediateResultSavingMode 

`IntermediateResultSavingMode` defines how to save the intermediate result(s). It can be one of the follwoing candidate modes.

## Candidate Mode List
- IRSM_MEMORY
- IRSM_FILESYSTEM
- IRSM_BOTH
- IRSM_REFERENCE_MEMORY


### IRSM_MEMORY
Saves intermediate results in memory with public data format.

### IRSM_FILESYSTEM
Saves intermediate results in file system. This mode has the following arguments for further customizing.
- [FolderPath](#folderpath)
- [RecordsetSizeOfLatestImages](#recordsetsizeoflatestimages)

### IRSM_BOTH
Saves intermediate results using IRSM_MEMORY and IRSM_FILESYSTEM. This mode has the following arguments for further customizing.
- [FolderPath](#folderpath)

### IRSM_REFERENCE_MEMORY
Saves intermediate results in memory with internal data format. This mode has the following arguments for further customizing.
- [FolderPath](#folderpath)
- [RecordsetSizeOfLatestImages](#recordsetsizeoflatestimages)

## Setting Methods

### As `PublicRuntimeSettings` Member
`IntermediateResultSavingMode` can be set dynamically during runtime as a member of `PublicRuntimeSettings` struct, it is one of the `IntermediateResultSavingMode` Enumeration items.


**Code Snippet in C++**
```cpp
//...other codes
PublicRuntimeSettings* pSettings = new PublicRuntimeSettings;
int errorCode = reader->GetRuntimeSettings(pSettings);
pSettings->intermediateResultSavingMode = IRSM_MEMORY;
reader->UpdateRuntimeSettings(pSettings);
delete pSettings;
//...other codes
```


**See Also**      
- `PublicRuntimeSettings:` [JavaScript]({{ site.js_api }}interface/RuntimeSettings.html) \| [C]({{ site.structs }}PublicRuntimeSettings.html?src=c) \| [C++]({{ site.structs }}PublicRuntimeSettings.html?src=cpp) \| [.NET]({{ site.dotnet_api }}struct/PublicRuntimeSettings.html) \| [Python]({{ site.python_api }}class/PublicRuntimeSettings.html) \| [Java]({{ site.java_api }}class/PublicRuntimeSettings.html) \| [Java-Android]({{ site.android_api }}auxiliary-PublicRuntimeSettings.html) \| [Objective-C & Swift]({{ site.oc_api }}auxiliary-iPublicRuntimeSettings.html)
- `IntermediateResultSavingMode:` [JavaScript]({{ site.js_enumerations }}EnumIntermediateResultSavingMode.html) \| [C]({{ site.c_cpp_enumerations }}result-enums.html?src=c#intermediateresultsavingmode) \| [C++]({{ site.c_cpp_enumerations }}result-enums.html?src=cpp#intermediateresultsavingmode) \| [.NET]({{ site.dotnet_enumerations }}result-enums.html#intermediateresultsavingmode) \| [Python]({{ site.python_enumerations }}result-enums.html#intermediateresultsavingmode) \| [Java]({{ site.java_enumerations }}result-enums.html#intermediateresultsavingmode) \| [Java-Android]({{ site.mobile_enumerations }}intermediate-result-saving-mode.html?lang=android) \| [Objective-C & Swift]({{ site.mobile_enumerations }}intermediate-result-saving-mode.html?lang=objc,swift)


### As JSON Parameter
`IntermediateResultSavingMode` as a JSON parameter is a JSON object defined as below.   

| Key Name | Key Value | Description |
| -------- | --------- | ----------- |
| Mode | Any one in Candidate Mode List as string | (Required) Sets how to save the intermediate result.  |
| FolderPath | A string from value range of FolderPath | (Optional) Sets the Argument [FolderPath](#folderpath). |
| RecordsetSizeOfLatestImages | A number from value range of RecordsetSizeOfLatestImages | (Optional) Sets the Argument [RecordsetSizeOfLatestImages](#recordsetsizeoflatestimages). |



**JSON Parameter Example**   
```
{
    "IntermediateResultSavingMode": {
            "Mode": "IRSM_FILESYSTEM",
            "FolderPath": "C:\",
            "RecordsetSizeOfLatestImages": 0
        }
}
```


<!--
## Impacts on Performance
### Speed
Saving intermediate results to file system may take more time than saving to memory.

### Read Rate
`IntermediateResultSavingMode` has no influence on the Read Rate.

### Accuracy
`IntermediateResultSavingMode` has no influence on the Accuracy.


-->
## Candidate Argument List
- [FolderPath](#folderpath)
- [RecordsetSizeOfLatestImages](#recordsetsizeoflatestimages)

### FolderPath 
Sets the path of the output folder which stores intermediate results.   

| Value Type | Value Range | Default Value | 
| ---------- | ----------- | ------------- |
| *string* | A string value representing the folder path with max length 480. | "" |         

**Remarks**         
    - "": The library path.    
    - Please make sure the path exists and your application has the appropriate permissions for saving the results.   

### RecordsetSizeOfLatestImages
Sets the maximum count of recordset to store the latest images' intermediate results.

| Value Type | Value Range | Default Value | 
| ---------- | ----------- | ------------- |
| *int* | [0,0x7fffffff]  |  0 | 

**Remarks**         
    - 0: no limitation on the count of recordset.   
    - When the count exceeds, the old recordset will be replaced by the new one.


## Related Articles
- [Use RuntimeSettings or Templates for Configuring Parameters]({{ site.features }}use-runtimesettings-or-templates.html)
- [How to obtain and use intermediate results]({{ site.scenario_settings }}intermediate-result.html)
