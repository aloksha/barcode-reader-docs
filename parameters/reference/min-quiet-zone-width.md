---
layout: default-layout
title: MinQuietZoneWidth - Dynamsoft Barcode Reader Parameter Reference
description: This page shows Dynamsoft Barcode Reader Parameter Reference for MinQuietZoneWidth.
keywords: MinQuietZoneWidth, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/min-quiet-zone-width.html
---


# MinQuietZoneWidth 

`MinQuietZoneWidth` defines the minimum width (in moduleSize) of the barcode quiet zone. It is defined as below:

| Value Type | Value Range | Default Value | Template Structure Type |
| ---------- | ----------- | ------------- | ----------------------- |
| *int* | [0, 0x7fffffff] | 4 | `FormatSpecification` |


**Remarks**  
- The unit is a multiplier of the barcode module size. For example, if barcode module is 2px and MinQuietZoneWidth is 4, then the width of quiet zone is 8px.

    
## Setting Methods
`MinQuietZoneWidth` can be set via JSON template.

### As JSON Parameter
`MinQuietZoneWidth` as a JSON parameter is a number value defined as below.   

| Key Name | Key Value |
| -------- | --------- |
| MinQuietZoneWidth | A number from [0, 0x7fffffff] |


**JSON Example**   
```
{
    "MinQuietZoneWidth": 1
}
```


<!--
## Impacts on Performance
### Speed
`MinQuietZoneWidth` has no influence on the Speed.

### Read Rate
Setting `MinQuietZoneWidth` to a appropriate number for barcodes with narrow quiet zone may improve the Read Rate.

### Accuracy
`MinQuietZoneWidth` has no influence on the Accuracy.

-->
## Related Articles
- [Use RuntimeSettings or Templates for Configuring Parameters]({{ site.features }}use-runtimesettings-or-templates.html)
- [Configure parameters for a certain barcode format]({{ site.scenario_settings }}format-specification.html#minquietzonewidth)
