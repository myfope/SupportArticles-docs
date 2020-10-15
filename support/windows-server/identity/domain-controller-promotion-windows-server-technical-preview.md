---
title: Domain controller promotion process shows 
description: Provides a resolution for the issue Domain controller promotion process shows "Windows Server Technical Preview" in the Domain and Forest functional level list
ms.date: 09/14/2020
author: Deland-Han
ms.author: delhan 
manager: dscontentpm
audience: itpro
ms.topic: troubleshooting
ms.prod: windows-server
localization_priority: medium
ms.reviewer: kaushika, warrenw, arrenc
ms.prod-support-area-path: Active Directory domain or forest functional level updates
ms.technology: ActiveDirectory
---
# Domain controller promotion process shows "Windows Server Technical Preview" in the Domain and Forest functional level list

This article provides a resolution for the issue Domain controller promotion process shows "Windows Server Technical Preview" in the Domain and Forest functional level list.

_Original product version:_ &nbsp; Windows Server 2016  
_Original KB number:_ &nbsp; 3202325

## Symptoms

Consider the following scenario:
- You have a computer that's running Windows Server 2016.
- You install the Active Directory Domain Service (AD DS) role.
- After the role is installed, you run the domain controller (DC) promotion process on the server.  

However, on the second page of the DC promotion Wizard, you notice that both the Forest and Domain functional levels show an incorrect version of Windows, as in the following screenshot:

  ![screenshot of dc promotion wizard](./media/domain-controller-promotion-windows-server-technical-preview/dc-options.png)

You expect the DC Promotion Wizard to show **Windows Server 2016**  instead of **Windows Server Technical Preview**.

> [!NOTE]
>  The Windows Server 2016 Domain and Forest functional levels are not affected functionally.

## Cause

This issue occurs because the display string was not updated in the Forest and Domain functional levels before the release of Windows Server 2016. 

## Resolution

To resolve this issue, apply the latest cumulative update for Windows Server 2016 from Windows Update before you promote a computer to a domain controller.