---
description: 了解详细信息： CLR User-Defined 类型
title: CLR 用户定义的类型
ms.date: 03/30/2017
ms.assetid: 9f70e0b0-3a0d-4eb1-b914-07a5d0c167c2
ms.openlocfilehash: f1732c254d3bf3cb8aa4ba727c420c46ef55c2cf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99663360"
---
# <a name="clr-user-defined-types"></a><span data-ttu-id="fa80e-103">CLR 用户定义的类型</span><span class="sxs-lookup"><span data-stu-id="fa80e-103">CLR User-Defined Types</span></span>

<span data-ttu-id="fa80e-104">Microsoft SQL Server 提供了对使用 Microsoft .NET Framework 公共语言运行时 (CLR) 实现的用户定义类型 (UDT) 的支持。</span><span class="sxs-lookup"><span data-stu-id="fa80e-104">Microsoft SQL Server provides support for user-defined types (UDTs) implemented with the Microsoft .NET Framework common language runtime (CLR).</span></span> <span data-ttu-id="fa80e-105">CLR 集成在 SQL Server 中，通过此机制，您可以扩展数据库的类型系统。</span><span class="sxs-lookup"><span data-stu-id="fa80e-105">The CLR is integrated into SQL Server, and this mechanism enables you to extend the type system of the database.</span></span> <span data-ttu-id="fa80e-106">UDT 使用户可以扩展 SQL Server 的数据类型系统，还可以定义复杂的结构化类型。</span><span class="sxs-lookup"><span data-stu-id="fa80e-106">UDTs provide user extensibility of the SQL Server data type system, and also the ability to define complex structured types.</span></span>  
  
 <span data-ttu-id="fa80e-107">从应用程序结构的角度来说，UDT 具有两个重要的优点：</span><span class="sxs-lookup"><span data-stu-id="fa80e-107">UDTs can provide two key benefits from an application architecture perspective:</span></span>  
  
- <span data-ttu-id="fa80e-108">在内部状态和外部行为之间强大的包装（无论在客户端中还是在服务器中）。</span><span class="sxs-lookup"><span data-stu-id="fa80e-108">Strong encapsulation (both in the client and the server) between the internal state and the external behaviors.</span></span>  
  
- <span data-ttu-id="fa80e-109">与其他相关服务器功能的深度集成。</span><span class="sxs-lookup"><span data-stu-id="fa80e-109">Deep integration with other related server features.</span></span> <span data-ttu-id="fa80e-110">定义了自己的 UDT 后，可以在所有可使用 SQL Server 中的系统类型（包括列定义）的上下文中使用，并且可以作为变量、参数、函数结果、游标、触发器和复制使用。</span><span class="sxs-lookup"><span data-stu-id="fa80e-110">Once you define your own UDT, you can use it in all contexts where you can use a system type in SQL Server, including column definitions, and as variables, parameters, function results, cursors, triggers, and replication.</span></span>  
  
 <span data-ttu-id="fa80e-111">有关更多详细信息，请参阅所使用 SQL Server 版本的 [SQL Server 文档](/sql) 。</span><span class="sxs-lookup"><span data-stu-id="fa80e-111">For more detailed information, see the [SQL Server documentation](/sql) for the version of SQL Server you're using.</span></span>
  
 <span data-ttu-id="fa80e-112">**SQL Server 文档**</span><span class="sxs-lookup"><span data-stu-id="fa80e-112">**SQL Server documentation**</span></span>
  
1. [<span data-ttu-id="fa80e-113">CLR 用户定义的类型</span><span class="sxs-lookup"><span data-stu-id="fa80e-113">CLR User-Defined Types</span></span>](/sql/relational-databases/clr-integration-database-objects-user-defined-types/clr-user-defined-types)  
  
## <a name="see-also"></a><span data-ttu-id="fa80e-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="fa80e-114">See also</span></span>

- [<span data-ttu-id="fa80e-115">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="fa80e-115">ADO.NET Overview</span></span>](../ado-net-overview.md)
