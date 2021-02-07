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
# <a name="sql-server-common-language-runtime-integration"></a><span data-ttu-id="8fd9d-103">SQL Server 公共语言运行时集成</span><span class="sxs-lookup"><span data-stu-id="8fd9d-103">SQL Server Common Language Runtime Integration</span></span>

<span data-ttu-id="8fd9d-104">SQL Server 2005 引入了 Microsoft Windows 的 .NET Framework 的公共语言运行库 (CLR) 组件的集成。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-104">SQL Server 2005 introduced the integration of the common language runtime (CLR) component of the .NET Framework for Microsoft Windows.</span></span> <span data-ttu-id="8fd9d-105">这意味着您可以使用任意 .NET Framework 语言（包括 Microsoft Visual Basic .NET 和 Microsoft Visual C#）编写存储过程、触发器、用户定义类型、用户定义函数、用户定义聚合函数以及流处理表值函数。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-105">This means that you can write stored procedures, triggers, user-defined types, user-defined functions, user-defined aggregates, and streaming table-valued functions, using any .NET Framework language, including Microsoft Visual Basic .NET and Microsoft Visual C#.</span></span> <span data-ttu-id="8fd9d-106"><xref:Microsoft.SqlServer.Server> 命名空间包含一组新的应用程序编程接口 (API)，使托管代码可以与 Microsoft SQL Server 环境交互。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-106">The <xref:Microsoft.SqlServer.Server> namespace contains a set of new application programming interfaces (APIs) so that managed code can interact with the Microsoft SQL Server environment.</span></span>  
  
 <span data-ttu-id="8fd9d-107">本节介绍 SQL Server 公共语言运行库 (CLR) 集成特定的功能和行为以及 SQL Server 进程中专用的 ADO.NET 扩展。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-107">This section describes features and behaviors that are specific to SQL Server common language runtime (CLR) integration and the SQL Server in-process specific extensions to ADO.NET.</span></span>  
  
 <span data-ttu-id="8fd9d-108">本节只是为了提供足够的信息，以便开始使用 SQL Server CLR 集成编程，而并非为了提供完整的信息。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-108">This section is meant to provide only enough information to get started programming with SQL Server CLR integration, and is not meant to be comprehensive.</span></span> <span data-ttu-id="8fd9d-109">有关更多详细信息，请参见您正在使用的 SQL Server 版本的“SQL Server 联机丛书”版本。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-109">For more detailed information, see the version of SQL Server Books Online for the version of SQL Server you are using.</span></span>  
  
 <span data-ttu-id="8fd9d-110">**SQL Server 文档**</span><span class="sxs-lookup"><span data-stu-id="8fd9d-110">**SQL Server documentation**</span></span>  
  
1. [<span data-ttu-id="8fd9d-111">公共语言运行时 (CLR) 集成编程概念</span><span class="sxs-lookup"><span data-stu-id="8fd9d-111">Common Language Runtime (CLR) Integration Programming Concepts</span></span>](/sql/relational-databases/clr-integration/common-language-runtime-clr-integration-programming-concepts)  
  
## <a name="in-this-section"></a><span data-ttu-id="8fd9d-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="8fd9d-112">In This Section</span></span>  

 [<span data-ttu-id="8fd9d-113">SQL Server CLR 集成简介</span><span class="sxs-lookup"><span data-stu-id="8fd9d-113">Introduction to SQL Server CLR Integration</span></span>](introduction-to-sql-server-clr-integration.md)  
 <span data-ttu-id="8fd9d-114">简介 SQL Server CLR 集成。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-114">Provides an introduction to SQL Server CLR integration.</span></span> <span data-ttu-id="8fd9d-115">提供指向其他主题的链接。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-115">Provides links to additional topics.</span></span>  
  
 [<span data-ttu-id="8fd9d-116">CLR 用户定义函数</span><span class="sxs-lookup"><span data-stu-id="8fd9d-116">CLR User-Defined Functions</span></span>](clr-user-defined-functions.md)  
 <span data-ttu-id="8fd9d-117">说明如何实现和使用各种类型的 CLR 函数：表值、标量和用户定义的聚合函数。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-117">Describes how to implement and use the various types of CLR functions: table-valued, scalar, and user-defined aggregate functions.</span></span>  
  
 [<span data-ttu-id="8fd9d-118">CLR 用户定义的类型</span><span class="sxs-lookup"><span data-stu-id="8fd9d-118">CLR User-Defined Types</span></span>](clr-user-defined-types.md)  
 <span data-ttu-id="8fd9d-119">说明如何实现和使用 CLR 用户定义类型。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-119">Describes how to implement and use CLR user-defined types.</span></span> <span data-ttu-id="8fd9d-120">提供指向其他主题的链接。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-120">Provides links to additional topics.</span></span>  
  
 [<span data-ttu-id="8fd9d-121">CLR 存储过程</span><span class="sxs-lookup"><span data-stu-id="8fd9d-121">CLR Stored Procedures</span></span>](clr-stored-procedures.md)  
 <span data-ttu-id="8fd9d-122">说明如何实现和使用 CLR 存储过程。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-122">Describes how to implement and use CLR stored procedures.</span></span> <span data-ttu-id="8fd9d-123">提供指向其他主题的链接。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-123">Provides links to additional topics.</span></span>  
  
 [<span data-ttu-id="8fd9d-124">CLR 触发器</span><span class="sxs-lookup"><span data-stu-id="8fd9d-124">CLR Triggers</span></span>](clr-triggers.md)  
 <span data-ttu-id="8fd9d-125">说明如何实现和使用 CLR 触发器。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-125">Describes how to implement and use CLR triggers.</span></span> <span data-ttu-id="8fd9d-126">提供指向其他主题的链接。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-126">Provides links to additional topics.</span></span>  
  
 [<span data-ttu-id="8fd9d-127">上下文连接</span><span class="sxs-lookup"><span data-stu-id="8fd9d-127">The Context Connection</span></span>](the-context-connection.md)  
 <span data-ttu-id="8fd9d-128">介绍了上下文连接。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-128">Describes the context connection.</span></span>  
  
 [<span data-ttu-id="8fd9d-129">ADO.NET 的 SQL Server 进程内特定行为</span><span class="sxs-lookup"><span data-stu-id="8fd9d-129">SQL Server In-Process-Specific Behavior of ADO.NET</span></span>](sql-server-in-process-specific-behavior-of-adonet.md)  
 <span data-ttu-id="8fd9d-130">介绍 SQL Server 进程中专用的 ADO.NET 扩展以及上下文连接。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-130">Describes the SQL Server in-process specific extensions to ADO.NET, and the context connection.</span></span> <span data-ttu-id="8fd9d-131">提供指向其他主题的链接。</span><span class="sxs-lookup"><span data-stu-id="8fd9d-131">Provides links to additional topics.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8fd9d-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="8fd9d-132">See also</span></span>

- [<span data-ttu-id="8fd9d-133">SQL Server 和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="8fd9d-133">SQL Server and ADO.NET</span></span>](index.md)
- [<span data-ttu-id="8fd9d-134">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="8fd9d-134">ADO.NET Overview</span></span>](../ado-net-overview.md)
