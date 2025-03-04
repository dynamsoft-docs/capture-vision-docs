---
layout: default-layout
title: Standard Input - Dynamsoft Capture Vision Architecture
description: This article is about the standard input in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
permalink: /architecture/input.html
---

# Input

![DCV Architecture](assets/dcv-architecture-input.png)

In the Dynamsoft Capture Vision (DCV) architecture, "input" refers to the source supplying images for processing, commonly called the **image source**.

An image source is any object that implements the [Image Source Adapter (ISA)](#image-source-adapter) interface.

## Image Source Adapter

The **Image Source Adapter (ISA)** interface connects an image source to a DCV application. It is designed with the following capabilities:

1. Returns an image when requested by the [Capture Vision Router (CVR)](index.md#capture-vision-router).
2. Maintains an image buffer for instant image access, reducing the time needed to open image files.

### Returning Images on Request

The primary function of an image source is to supply images when requested. To achieve this, ISA requires the following methods:

- A method to return an image, e.g., `getImage()`
- A method to return the total number of available images, e.g., `getImageCount()`
- A method to check if a specific image is available, e.g., `hasImage()`
- A method to set the order in which images are returned, e.g., `setNextImageToReturn()`

### Maintaining an Image Buffer

To facilitate image retrieval, ISA maintains a buffer area. The following methods support this functionality:

- Adding images to the buffer, e.g., `addImageToBuffer()`
- Controlling the buffer size, e.g., `setMaxImageCount()` and `getMaxImageCount()`
- Managing buffer operations, e.g., `startFetching()` and `stopFetching()`
- Handling buffer overflow, e.g., `setBufferOverflowProtectionMode()` and `getBufferOverflowProtectionMode()`
- Additional utility methods, e.g., `isBufferEmpty()` and `hasNextImageToFetch()`

## PreBuilt Implementations

An image source is typically required when developing a DCV application. In most cases, developers can use one of the following prebuilt implementations:

### Dynamsoft Camera Enhancer

The **Dynamsoft Camera Enhancer (DCE)** is available on **web and mobile platforms**. It enables users to:

- Control cameras
- Capture image frames from a live video stream
- Provide basic user interaction

### Directory Fetcher

The **Directory Fetcher** is available on **mobile, desktop, and server platforms**. It allows users to simulate a directory containing images as an image source.

## Custom Implementation

Implementing ISA requires over ten methods, making it a complex task. To simplify development, **Dynamsoft provides a base class** to assist developers in creating custom implementations.

For more information, please [contact us](https://www.dynamsoft.com/company/contact/?utm_source=docs&product=dcv).
