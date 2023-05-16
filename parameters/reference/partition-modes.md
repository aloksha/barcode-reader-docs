---
layout: default-layout
title: PartitionModes - Dynamsoft Barcode Reader Parameter Reference
description: This page shows Dynamsoft Barcode Reader Parameter Reference for PartitionModes.
keywords: PartitionModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/partition-modes.html
---


# PartitionModes 

`PartitionModes` is used to select the mode used to apply partition process when decoding QRCode and DataMatrix. It is defined as below:

| Value Type | Value Range | Default Value | Template Structure Type |
| ---------- | ----------- | ------------- | ----------------------- |
| *string array* | "PM_WHOLE_BARCODE"<br>"PM_ALIGNMENT_PARTITION" | ["PM_WHOLE_BARCODE","PM_ALIGNMENT_PARTITION"] | `FormatSpecification` |

**Remarks**

- PM_WHOLE_BARCODE: Take the whole barcode for decoding.
- PM_ALIGNMENT_PARTITION: Partition the barcode to blocks based on alignment.
- It works only for QRCode and DataMatrix.

## Setting Methods

`PartitionModes` can be set via JSON template.

### As JSON Parameter

`PartitionModes` as a JSON parameter is a string array defined as below.

| Key Name | Key Value |
| -------- | --------- |
| PartitionModes | A string array while each array item can be "PM_WHOLE_BARCODE" or "PM_ALIGNMENT_PARTITION" |

**JSON Example**

```json
{
    "PartitionModes": ["PM_WHOLE_BARCODE"]
}
```
