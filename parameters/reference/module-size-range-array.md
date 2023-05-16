---
layout: default-layout
title: ModuleSizeRangeArray - Dynamsoft Barcode Reader Parameter Reference
description: This page shows Dynamsoft Barcode Reader Parameter Reference for ModuleSizeRangeArray.
keywords: ModuleSizeRangeArray, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/module-size-range-array.html
---


# ModuleSizeRangeArray 

`ModuleSizeRangeArray` defines the range of module size (in pixels) while barcode searching and result filtering. It is not set by default which means there is no limitation on the barcode module size.
    
## Setting Methods
`ModuleSizeRangeArray` can be set via JSON template.

### As JSON Parameter
`ModuleSizeRangeArray` as a JSON parameter is a JSON Object array defined as below.   

| Key Name | Key Value |
| -------- | --------- |
| ModuleSizeRangeArray | A JSON Object array while each Object is defined as below. |

| Key Name | Key Value | Description |
| -------- | --------- | ----------- |
| MinValue | A number from [0, 0x7fffffff] | Sets the minimum barcode module size.  |
| MaxValue | A number from [0, 0x7fffffff] | Sets the maximum barcode module size. |


**JSON Example**   
```
{
    "ModuleSizeRangeArray": [
    {
        "MinValue": 3,
        "MaxValue": 20
    }
    ]
}
```


<!--
## Impacts on Performance
### Speed
Enabling `ModuleSizeRangeArray` for filtering may speed up the process.

### Read Rate
Enabling `ModuleSizeRangeArray` to filter out results may reduce the Read Rate. 

### Accuracy
Enabling `ModuleSizeRangeArray` to filter out barcodes with small module size may improve the Accuracy.

-->
## Related Articles
- [Use RuntimeSettings or Templates for Configuring Parameters]({{ site.features }}use-runtimesettings-or-templates.html)
- [Configure parameters for a certain barcode format]({{ site.scenario_settings }}format-specification.html)
