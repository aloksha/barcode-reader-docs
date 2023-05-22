---
layout: default-layout
title: Timeout - Dynamsoft Barcode Reader Parameter Reference
description: This page shows Dynamsoft Barcode Reader Parameter Reference for Timeout.
keywords: Timeout, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/time-out.html
---


# Timeout 

`Timeout` defines the maximum amount of time (in milliseconds) that should be spent searching for a barcode per page. It does not include the time taken to load/decode an image (Tiff, PNG, etc) from disk into memory. It is defined as below:

| Value Type | Value Range | Default Value | Template Structure Type |
| ---------- | ----------- | ------------- | ----------------------- |
| *int* | [0, 0x7fffffff] | 10000 | `ImageParameter` |

    
## Setting Methods
`Timeout` is supported to be set through `RuntimeSetting` or JSON template.

### As `PublicRuntimeSettings` Member
`Timeout` can be set dynamically during runtime as a member of `PublicRuntimeSettings` struct.


**Code Snippet in C++**
```cpp
//...other codes
PublicRuntimeSettings* pSettings = new PublicRuntimeSettings;
int errorCode = reader->GetRuntimeSettings(pSettings);
pSettings->timeout = 500;
reader->UpdateRuntimeSettings(pSettings);
delete pSettings;
//...other codes
```


**See Also**      
- `PublicRuntimeSettings:` [JavaScript]({{ site.js_api }}interface/RuntimeSettings.html) \| [C]({{ site.structs }}PublicRuntimeSettings.html?src=c) \| [C++]({{ site.structs }}PublicRuntimeSettings.html?src=cpp) \| [.NET]({{ site.dotnet_api }}struct/PublicRuntimeSettings.html) \| [Python]({{ site.python_api }}class/PublicRuntimeSettings.html) \| [Java]({{ site.java_api }}class/PublicRuntimeSettings.html) \| [Java-Android]({{ site.android_api }}auxiliary-PublicRuntimeSettings.html) \| [Objective-C & Swift]({{ site.oc_api }}auxiliary-iPublicRuntimeSettings.html)


### As JSON Parameter
`Timeout` as a JSON parameter is a number value defined as below.   

| Key Name | Key Value |
| -------- | --------- |
| Timeout | A number from [0, 0x7fffffff] |


**JSON Example**   
```
{
    "Timeout": 500
}
```


<!--
## Impacts on Performance
### Speed
Setting `Timeout` to a smaller value may improve the Speed.

### Read Rate
Setting `Timeout` to a larger value may improve the Read Rate.

### Accuracy
`Timeout` has no influence on the Accuracy.

-->
## Related Articles
- [Use RuntimeSettings or Templates for Configuring Parameters]({{ site.features }}use-runtimesettings-or-templates.html)
- [How to terminate the process]({{ site.scenario_settings }}terminate.html)
