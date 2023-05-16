---
layout: default-layout
title: HeadModuleRatio - Dynamsoft Barcode Reader Parameter Reference
description: This page shows Dynamsoft Barcode Reader Parameter Reference for HeadModuleRatio.
keywords: HeadModuleRatio, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/head-module-ratio.html
---


# HeadModuleRatio 

`HeadModuleRatio` defines the module count and module size ratio of the barcode head section. By default, there is no restriction on the head module count or module size ratio.

| Value Type | Value Range | Default Value | Template Structure Type |
| ---------- | ----------- | ------------- | ----------------------- |
| *string* | N/A | `""` | `FormatSpecification` |
    
## Setting Methods
`HeadModuleRatio` can be set via JSON template.

### As JSON Parameter
`HeadModuleRatio` as a JSON parameter is a string value defined as below.   

| Key Name | Key Value |
| -------- | --------- |
| HeadModuleRatio | a string representing the module count and module size |


**JSON Example**   
```
{
    "HeadModuleRatio": "211412"
}
```


<!--
## Impacts on Performance
### Speed
`HeadModuleRatio` has no influence on the Speed.

### Read Rate
Setting `HeadModuleRatio` to an appropriate value when detecting non-standard barcode may improve the Read Rate. 

### Accuracy
Setting `HeadModuleRatio` to an appropriate value when detecting non-standard barcode may improve the Accuracy.

-->
## Related Articles
- [Use RuntimeSettings or Templates for Configuring Parameters]({{ site.features }}use-runtimesettings-or-templates.html)
- [Configure parameters for a certain barcode format]({{ site.scenario_settings }}format-specification.html)
