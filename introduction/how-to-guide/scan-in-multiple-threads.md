---
layout: default-layout
title: Scan in Multiple Threads - Dynamsoft Barcode Reader How-to Guides
description: This page shows how to use Dynamsoft Barcode Reader in multiple threads.
keywords: multiple threads, how-to guides
needAutoGenerateSidebar: false
permalink: /introduction/how-to-guide/scan-in-multiple-threads.html
---


# How-to Guides - Scan in Multiple Threads    

To scan barcodes in multiple threads using Dynamsoft Barcode Reader, you need to create multiple instances of `BarcodeReader` and run separate instance in each thread. Please don't have multiple threads access the same `BarcodeReader` object.     

We have a sample that shows how to use multiple threads to read barcodes from images using the C++ API.

Get the sample: <a href="https://github.com/Dynamsoft/barcode-reader-c-cpp-samples/tree/main/samples/C%2B%2B/MultiThreadDecoding" target="_blank">MultiThreadDecoding Sample in C++</a> >.
