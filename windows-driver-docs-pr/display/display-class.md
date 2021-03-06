---
title: Display class
description: Display class DDIs in threading and synchronization first level.
ms.assetid: 439263ec-b28f-41ca-9c69-095216d63f38
keywords:
- display drivers WDK Windows, display class
- threading and synchronization first level
ms.author: windowsdriverdev
ms.date: 04/09/2018
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
---

# Display Class

The Windows Display Driver Model (WDDM) does not permit a call into one of the display class functions in a reentrant fashion. That is, at the most, one thread can be running within one of the following functions at a given time:

-   [*DxgkDdiSetTargetGamma*](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/d3dkmddi/nc-d3dkmddi-dxgkddi_settargetgamma)

-   [*DxgkDdiSetTargetContentType*](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/d3dkmddi/nc-d3dkmddi-dxgkddi_settargetcontenttype)

-   [*DxgkDdiSetTargetAnalogCopyProtection*](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/d3dkmddi/nc-d3dkmddi-dxgkddi_settargetanalogcopyprotection)

-   [*DxgkDdiSetTargetAdjustedColorimetry*](https://docs.microsoft.com/en-us/windows-hardware/drivers/ddi/content/dispmprt/nc-dispmprt-dxgkddi_settargetadjustedcolorimetry)