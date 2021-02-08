---
description: '了解详细信息：函数 (实体 SQL) '
title: 函数 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 52b3d776-5acc-4f69-b614-5a43ce56ef9f
ms.openlocfilehash: c557d264587a1d40194971d756e6b5c75a3856aa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786298"
---
# <a name="functions-entity-sql"></a><span data-ttu-id="284d6-103">函数 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="284d6-103">Functions (Entity SQL)</span></span>

<span data-ttu-id="284d6-104">Entity SQL 支持用户定义函数、规范函数和提供程序特定的函数。</span><span class="sxs-lookup"><span data-stu-id="284d6-104">Entity SQL supports user-defined functions, canonical functions, and provider-specific functions.</span></span> <span data-ttu-id="284d6-105">用户定义函数在概念模型中指定，或在查询中内联指定。</span><span class="sxs-lookup"><span data-stu-id="284d6-105">User-defined functions are specified in the conceptual model or inline in the query.</span></span> <span data-ttu-id="284d6-106">有关详细信息，请参阅 [用户定义函数](user-defined-functions-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="284d6-106">For more information, see [User-Defined Functions](user-defined-functions-entity-sql.md).</span></span>  
  
 <span data-ttu-id="284d6-107">在实体框架中对规范函数进行了预定义，因此数据提供程序将支持规范函数。</span><span class="sxs-lookup"><span data-stu-id="284d6-107">Canonical functions are predefined in the Entity Framework and should be supported by data providers.</span></span> <span data-ttu-id="284d6-108">如果用户调用提供程序不支持的函数，则 Entity SQL 命令将失败。</span><span class="sxs-lookup"><span data-stu-id="284d6-108">Entity SQL commands will fail if a user calls a function that is not supported by a provider.</span></span> <span data-ttu-id="284d6-109">因此，通常建议使用规范函数而不是存储特定的函数，后者位于提供程序特定的命名空间中。</span><span class="sxs-lookup"><span data-stu-id="284d6-109">Therefore, canonical functions are generally recommended over store-specific functions, which are in a provider-specific namespace.</span></span> <span data-ttu-id="284d6-110">有关详细信息，请参阅 [规范函数](canonical-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="284d6-110">For more information, see [Canonical Functions](canonical-functions.md).</span></span>  
  
 <span data-ttu-id="284d6-111">Microsoft SQL 客户端托管访问接口提供了一组提供程序特定的函数。</span><span class="sxs-lookup"><span data-stu-id="284d6-111">The Microsoft SQL Client Managed Provider provides a set of provider-specific functions.</span></span> <span data-ttu-id="284d6-112">有关详细信息，请参阅 [SqlClient for 实体框架函数](../sqlclient-for-ef-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="284d6-112">For more information, see [SqlClient for Entity Framework Functions](../sqlclient-for-ef-functions.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="284d6-113">本节内容</span><span class="sxs-lookup"><span data-stu-id="284d6-113">In This Section</span></span>  

 [<span data-ttu-id="284d6-114">用户定义函数</span><span class="sxs-lookup"><span data-stu-id="284d6-114">User-Defined Functions</span></span>](user-defined-functions-entity-sql.md)  
  
 [<span data-ttu-id="284d6-115">函数重载解析</span><span class="sxs-lookup"><span data-stu-id="284d6-115">Function Overload Resolution</span></span>](function-overload-resolution-entity-sql.md)  
  
 [<span data-ttu-id="284d6-116">聚合函数</span><span class="sxs-lookup"><span data-stu-id="284d6-116">Aggregate Functions</span></span>](../aggregate-functions-sqlclient-for-entity-framework.md)  
  
## <a name="see-also"></a><span data-ttu-id="284d6-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="284d6-117">See also</span></span>

- [<span data-ttu-id="284d6-118">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="284d6-118">Entity SQL Overview</span></span>](entity-sql-overview.md)
