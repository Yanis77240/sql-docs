---
title: "Server Properties (General Page) - SQL Server Management Studio | Microsoft Docs"
description: Become familiar with read-only properties in SQL Server. Examples include the server name, the operating system, the collation, and the SQL Server version.
ms.custom: ""
ms.date: "08/25/2016"
ms.prod: sql
ms.prod_service: high-availability
ms.reviewer: ""
ms.technology: configuration
ms.topic: conceptual
f1_keywords: 
  - "sql13.swb.serverproperties.setsapassword.f1"
  - "sql13.swb.serverproperties.activedirectory.f1"
  - "sql13.swb.serverproperties.prodinfo.f1"
ms.assetid: 10ac57f1-b4bd-4528-bb66-3e47ccf663e7
author: rwestMSFT
ms.author: randolphwest
---
# Server Properties - General Page
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  Use this page to view read-only information about your [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] installation.  
  
## Property Grid  
 View properties for the selected server, such as the server name, server operating system, or number of processors.  
  
 **Name**  
 Displays the name of the server instance.  
  
 **Product**  
 Displays the edition of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] currently running.  
  
 **Operating System**  
 Displays the [!INCLUDE[msCoName](../../includes/msconame-md.md)] Windows operating system currently running.  
  
 **Platform**  
 Describes the operating system and hardware running [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)].  
  
 **Version**  
 Displays the version number of the [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] edition currently running.  
  
 **Language**  
 Displays the language supported by the running instance of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)].  
  
 **Memory**  
 Lists the amount of RAM installed on the server.  
  
 **Processors**  
 Displays the number of CPUs installed.  
  
 **Root Directory**  
 Displays the path to the location of the [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] instance, typically C:\Program Files\Microsoft SQL Server\\.  
  
 **Server Collation**  
 Displays the collation supported by the server. A collation specifies the particular code page and sort order to use for Unicode and non-Unicode data.  
  
 **Is Clustered**  
 Displays **True** if the server instance is configured in a [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] failover cluster or **False** if the server instance is not clustered.  
  
 **Is HADR Enabled**  
 Displays **True** if the [!INCLUDE[ssHADR](../../includes/sshadr-md.md)] feature is enabled or **False** if the [!INCLUDE[ssHADR](../../includes/sshadr-md.md)] feature is disabled. For information about enabling or disabling [!INCLUDE[ssHADR](../../includes/sshadr-md.md)], see [Enable and Disable Always On Availability Groups &#40;SQL Server&#41;](../../database-engine/availability-groups/windows/enable-and-disable-always-on-availability-groups-sql-server.md).  
  
## Description Field  
 View additional information on the server properties.  
  
## See Also  
 [Server Configuration Options &#40;SQL Server&#41;](../../database-engine/configure-windows/server-configuration-options-sql-server.md)  
  
  
