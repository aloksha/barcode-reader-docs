---
layout: default-layout
title: TailModuleRatio - Dynamsoft Barcode Reader Parameter Reference
description: This page shows Dynamsoft Barcode Reader Parameter Reference for TailModuleRatio.
keywords: TailModuleRatio, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/tail-module-ratio.html
---


# TailModuleRatio 

`TailModuleRatio` defines the module count and module size ratio of the barcode tail part. By default, there is no restriction on the tail module count or module size ratio.

| Value Type | Value Range | Default Value | Template Structure Type |
| ---------- | ----------- | ------------- | ----------------------- |
| *string* | N/A | `""` | `FormatSpecification` |
    
## Setting Methods
`TailModuleRatio` can be set via JSON template.

### As JSON Parameter
`TailModuleRatio` as a JSON parameter is a string value defined as below.   

| Key Name | Key Value |
| -------- | --------- |
| TailModuleRatio | a string representing the module count and module size |


**JSON Example**   
```
{
    "TailModuleRatio": "2331112"
}
```


<!--
## Impacts on Performance
### Speed
`TailModuleRatio` has no influence on the Speed.

### Read Rate
Setting `TailModuleRatio` to an appropriate value when detecting non-standard barcode may improve the Read Rate. 

### Accuracy
Setting `TailModuleRatio` to an appropriate value when detecting non-standard barcode may improve the Accuracy.

-->
## Related Articles
- [Use RuntimeSettings or Templates for Configuring Parameters]({{ site.features }}use-runtimesettings-or-templates.html)
- [Configure parameters for a certain barcode format]({{ site.scenario_settings }}format-specification.html)
