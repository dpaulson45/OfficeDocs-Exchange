---
title: "ExecutionPolicy GPO is defined [PowerShellExecutionPolicyCheckSet]"
ms.author: dstrome
author: dstrome
manager: serdars
ms.date: 7/22/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- 'ms.exch.setupreadiness.PowerShellExecutionPolicyCheckSet'
ms.prod: exchange-server-it-pro
localization_priority: Normal
ms.assetid: 63de83e2-9a6b-4f57-85b9-df445bea18dd
description: "Microsoft Exchange Server 2016 Setup can't continue because it detected that the ExecutionPolicy Group Policy Object (GPO) defines one or both of the following policies:"
---

# ExecutionPolicy GPO is defined [PowerShellExecutionPolicyCheckSet]

Microsoft Exchange Server 2016 Setup can't continue because it detected that the **ExecutionPolicy** Group Policy Object (GPO) defines one or both of the following policies: 
  
- **MachinePolicy**
    
- **UserPolicy**
    
It doesn't matter how the policies have been defined. It only matters that they have been defined.
  
When you run Exchange 2016 Setup, Exchange stops and disables the Windows Management Instrumentation (WMI) service. When either of these policies are defined, the WMI service needs to be enabled to run a Windows PowerShell script. If the policies are defined and the WMI service is stopped, Setup will fail and the server will be left in an inconsistent state.
  
To allow Setup to continue, you need to temporarily remove any definition of **MachinePolicy** or **UserPolicy** in the **ExecutionPolicy** GPO.
  
For information on how to remove any definitions of **MachinePolicy** or **UserPolicy** in the **ExecutionPolicy** GPO, see [Knowledge Base article KB981474](http://go.microsoft.com/fwlink/?linkid=3052&kbid=981474).
  
> [!NOTE]
> Even though this Knowledge Base article was written for Exchange 2010, it also applies to Exchange 2016 cumulative updates and service packs.
  
Having problems? Ask for help in the Exchange forums. Visit the forums at: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).
