---
layout: default-layout
title: Text-line Localization Section - Dynamsoft Capture Vision Architecture
description: This article introduces Text-line Localization Section in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /architecture/image-processing/textline-localization.html
---

The following diagram shows how sections connect to each other to form tasks:

```mermaid
flowchart LR;
     A[1.Region Pre-Detection]-->C[2.1.Shared Detection]
     C---D[2.2.Barcode Localization]
     C---E[2.2.Text-line Localization]
     C---F[2.2.Document Detection]
     D---G[3.Barcode Decoding]
     E---H[3.Text-line Recognition]
     F---I[3.Document Normalization]
     style E fill:#f96,stroke:#333,stroke-width:4px
```

In this article, we'll discuss the section **Text-line Localization** which is the product-specific part of the 2nd section of a "Recognize-Text-Lines" task.

> The 2nd section of a "Recognize-Text-Lines" task consists of [**Shared Detection**](shared-detection.md) and **Text-line Localization**.

# Section 2.2 - Text-line Localization

The purpose of this section is to detect the exact locations of text-lines.

## Constituting Stages

This section consists of only one stage:

- Text-line-locating: to find the exact locations of the text-lines.

## Output and Parameters

| Stage              | Intermediate Result Type    | Related Parameter |
| ------------------ | --------------------------- | ----------------- |
| Text-line-locating | `IRUT_LOCALIZED_TEXT_LINES` | N/A               |
