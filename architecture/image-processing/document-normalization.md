---
layout: default-layout
title: Document Normalization Section - Dynamsoft Capture Vision Architecture
description: This article introduces Document Normalization Section in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /architecture/image-processing/document-normalization.html
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
     F---I[3.Document Deskewing]
     I---J[4.Image Enhancement]
     style I fill:#f96,stroke:#333,stroke-width:4px
```

In this article, we'll discuss the section **Document Deskewing** which is usually the 3rd section of a "Normalize-a-Document" task.

# Section 3 - Document Deskewing

The purpose of this section is to generate a standard rectangular image of the "document" localized in the section "Document Detection".

> A document is an object that exhibit clear boundaries.

## Constituting Stages

This section consists of just one stage:

- Document-deskewing: to deskew the document which may involve one or several of these actions:
  - Deskew
  - Perspective correction

## Output and Parameters

| Stage | Intermediate Result Type | Related Parameter |
| ----- | ------------------------ | ----------------- |
| Document-deskewing | `IRUT_DESKEWED_IMAGE`  | [`PageSize`](../../parameters/reference/document-normalizer-task-settings/page-size.md), [`DeskewMode`](../../parameters/reference/document-normalizer-task-settings/deskew-mode.md) |
