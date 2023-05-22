---
layout: default-layout
title: FindUnevenModuleBarcode - Dynamsoft Barcode Reader Parameter Reference
description: This page shows Dynamsoft Barcode Reader Parameter Reference for FindUnevenModuleBarcode.
keywords: FindUnevenModuleBarcode, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/find-uneven-module-barcode.html
---


# FindUnevenModuleBarcode 

`FindUnevenModuleBarcode` defines whether to find barcodes with uneven barcode modules. It is defined as below:

| Value Type | Value Range | Default Value | Template Structure Type |
| ---------- | ----------- | ------------- | ----------------------- |
| *int* | [0, 1] | 1 | `FormatSpecification` |


**Remarks**  
- 0: do not find barcodes with uneven barcode modules.
- 1: find barcodes with uneven barcode modules.


    
## Setting Methods
`FindUnevenModuleBarcode` can be set via JSON template.

### As JSON Parameter
`FindUnevenModuleBarcode` as a JSON parameter is a number value defined as below.   

| Key Name | Key Value |
| -------- | --------- |
| FindUnevenModuleBarcode | A number from [0, 1] |


**JSON Example**   
```
{
    "FindUnevenModuleBarcode": 1
}
```


<!--
## Impacts on Performance
### Speed
`FindUnevenModuleBarcode` has no influence on the Speed.

### Read Rate
Setting `FindUnevenModuleBarcode` to an appropriate value when detecting non-standard barcodes may improve the Read Rate. 

### Accuracy
Setting `FindUnevenModuleBarcode` to an appropriate value when detecting non-standard barcodes may improve the Accuracy.

-->
## Related Articles
- [Use RuntimeSettings or Templates for Configuring Parameters]({{ site.features }}use-runtimesettings-or-templates.html)
- [Configure parameters for a certain barcode format]({{ site.scenario_settings }}format-specification.html)
