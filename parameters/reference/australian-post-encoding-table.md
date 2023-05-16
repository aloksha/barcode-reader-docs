---
layout: default-layout
title: AustralianPostEncodingTable - Dynamsoft Barcode Reader Parameter Reference
description: This page shows Dynamsoft Barcode Reader Parameter Reference for AustralianPostEncodingTable.
keywords: AustralianPostEncodingTable, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/australian-post-encoding-table.html
---


# AustralianPostEncodingTable 

`AustralianPostEncodingTable` helps specify the encoding table used to code the Customer Information Field of Australian Post Customer Barcode. It is defined as below:

| Value Type | Value Range | Default Value | Template Structure Type |
| ---------- | ----------- | ------------- | ----------------------- |
| *string* | "C"<br>"N" | "C"  | `FormatSpecification` |


    
## Setting Methods
`AustralianPostEncodingTable` can be set via JSON template.

### As JSON Parameter
`AustralianPostEncodingTable` as a JSON parameter is a number value defined as below.   

| Key Name | Key Value |
| -------- | --------- |
| AustralianPostEncodingTable | "C" or "N" as a string |


**JSON Example**   
```
{
    "AustralianPostEncodingTable": "N"
}
```


<!--
## Impacts on Performance
### Speed
`AustralianPostEncodingTable` has no influence on the Speed.

### Read Rate
Setting `AustralianPostEncodingTable` to an appropriate value when detecting Australian Post Customer Barcode may improve the Read Rate. 

### Accuracy
Setting `AustralianPostEncodingTable` to an appropriate value when detecting Australian Post Customer Barcode may improve the Accuracy.

-->
## Related Articles
- [Use RuntimeSettings or Templates for Configuring Parameters]({{ site.features }}use-runtimesettings-or-templates.html)
- [Configure parameters for a certain barcode format]({{ site.scenario_settings }}format-specification.html#australianpostencodingtable)
