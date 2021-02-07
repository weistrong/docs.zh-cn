---
description: 了解详细信息： SQL Server 公共语言运行时集成
title: SQL Server 公共语言运行时集成
ms.date: 03/30/2017
ms.assetid: c7a324c4-160d-44c2-b593-641af06eca61
ms.openlocfilehash: 096bba0d183526ec8e5d272c5ea6a77ad0778e5f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767396"
---
# <a name="sql-server-common-language-runtime-integration"></a>SQL Server 公共语言运行时集成

SQL Server 2005 引入了 Microsoft Windows 的 .NET Framework 的公共语言运行库 (CLR) 组件的集成。 这意味着您可以使用任意 .NET Framework 语言（包括 Microsoft Visual Basic .NET 和 Microsoft Visual C#）编写存储过程、触发器、用户定义类型、用户定义函数、用户定义聚合函数以及流处理表值函数。 <xref:Microsoft.SqlServer.Server> 命名空间包含一组新的应用程序编程接口 (API)，使托管代码可以与 Microsoft SQL Server 环境交互。  
  
 本节介绍 SQL Server 公共语言运行库 (CLR) 集成特定的功能和行为以及 SQL Server 进程中专用的 ADO.NET 扩展。  
  
 本节只是为了提供足够的信息，以便开始使用 SQL Server CLR 集成编程，而并非为了提供完整的信息。 有关更多详细信息，请参见您正在使用的 SQL Server 版本的“SQL Server 联机丛书”版本。  
  
 **SQL Server 文档**  
  
1. [公共语言运行时 (CLR) 集成编程概念](/sql/relational-databases/clr-integration/common-language-runtime-clr-integration-programming-concepts)  
  
## <a name="in-this-section"></a>本节内容  

 [SQL Server CLR 集成简介](introduction-to-sql-server-clr-integration.md)  
 简介 SQL Server CLR 集成。 提供指向其他主题的链接。  
  
 [CLR 用户定义函数](clr-user-defined-functions.md)  
 说明如何实现和使用各种类型的 CLR 函数：表值、标量和用户定义的聚合函数。  
  
 [CLR 用户定义的类型](clr-user-defined-types.md)  
 说明如何实现和使用 CLR 用户定义类型。 提供指向其他主题的链接。  
  
 [CLR 存储过程](clr-stored-procedures.md)  
 说明如何实现和使用 CLR 存储过程。 提供指向其他主题的链接。  
  
 [CLR 触发器](clr-triggers.md)  
 说明如何实现和使用 CLR 触发器。 提供指向其他主题的链接。  
  
 [上下文连接](the-context-connection.md)  
 介绍了上下文连接。  
  
 [ADO.NET 的 SQL Server 进程内特定行为](sql-server-in-process-specific-behavior-of-adonet.md)  
 介绍 SQL Server 进程中专用的 ADO.NET 扩展以及上下文连接。 提供指向其他主题的链接。  
  
## <a name="see-also"></a>请参阅

- [SQL Server 和 ADO.NET](index.md)
- [ADO.NET 概述](../ado-net-overview.md)
