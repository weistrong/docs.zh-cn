---
description: 了解详细信息：规范函数
title: 规范函数
ms.date: 03/30/2017
ms.assetid: bbcc9928-36ea-4dff-9e31-96549ffed958
ms.openlocfilehash: 6e84c4b5199d38e2efac44cf7e69c72abb1663f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739503"
---
# <a name="canonical-functions"></a><span data-ttu-id="99f62-103">规范函数</span><span class="sxs-lookup"><span data-stu-id="99f62-103">Canonical Functions</span></span>

<span data-ttu-id="99f62-104">本节讨论所有数据提供程序支持的并可由所有查询技术使用的规范函数。</span><span class="sxs-lookup"><span data-stu-id="99f62-104">This section discusses canonical functions that are supported by all data providers, and can be used by all querying technologies.</span></span> <span data-ttu-id="99f62-105">规范函数不能由提供程序扩展。</span><span class="sxs-lookup"><span data-stu-id="99f62-105">Canonical functions cannot be extended by a provider.</span></span>  
  
 <span data-ttu-id="99f62-106">这些规范函数将转换为提供程序的相应数据源功能。</span><span class="sxs-lookup"><span data-stu-id="99f62-106">These canonical functions will be translated to the corresponding data source functionality for the provider.</span></span> <span data-ttu-id="99f62-107">这样，就可以用一种在不同数据源间通用的形式表示函数调用。</span><span class="sxs-lookup"><span data-stu-id="99f62-107">This allows for function invocations expressed in a common form across data sources.</span></span>  
  
 <span data-ttu-id="99f62-108">因为这些规范函数独立于数据源，所以会按概念模型中的类型来定义规范函数的参数和返回类型。</span><span class="sxs-lookup"><span data-stu-id="99f62-108">Because these canonical functions are independent of data sources, argument and return types of canonical functions are defined in terms of types in the conceptual model.</span></span> <span data-ttu-id="99f62-109">但某些数据源可能不支持概念模型中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="99f62-109">However, some data sources might not support all types in the conceptual model.</span></span>  
  
 <span data-ttu-id="99f62-110">当在 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 查询中使用规范函数时，将在数据源中调用适当的函数。</span><span class="sxs-lookup"><span data-stu-id="99f62-110">When canonical functions are used in an [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query, the appropriate function will be called at the data source.</span></span>  
  
 <span data-ttu-id="99f62-111">所有规范函数都同时显式指定 null 输入行为和错误条件。</span><span class="sxs-lookup"><span data-stu-id="99f62-111">All canonical functions have both null-input behavior and error conditions explicitly specified.</span></span> <span data-ttu-id="99f62-112">存储提供程序应符合该行为，但实体框架不强制执行此行为。</span><span class="sxs-lookup"><span data-stu-id="99f62-112">Store providers should comply with that behavior, but Entity Framework does not enforce this behavior.</span></span>  
  
 <span data-ttu-id="99f62-113">对于 LINQ 方案，针对实体框架的查询涉及将 CLR 方法映射到基础数据源中的方法。</span><span class="sxs-lookup"><span data-stu-id="99f62-113">For LINQ scenarios, queries against the Entity Framework involve mapping CLR methods to methods in the underlying data source.</span></span> <span data-ttu-id="99f62-114">CLR 方法映射到规范函数，这样，无论数据源如何，特定的方法集都会正确映射。</span><span class="sxs-lookup"><span data-stu-id="99f62-114">The CLR methods map to canonical functions, so that a specific set of methods will correctly map, regardless of the data source.</span></span>  
  
## <a name="canonical-functions-namespace"></a><span data-ttu-id="99f62-115">规范函数命名空间</span><span class="sxs-lookup"><span data-stu-id="99f62-115">Canonical Functions Namespace</span></span>  

 <span data-ttu-id="99f62-116">规范函数的命名空间是 <xref:System.Data.Metadata.Edm>。</span><span class="sxs-lookup"><span data-stu-id="99f62-116">The namespace for canonical function is <xref:System.Data.Metadata.Edm>.</span></span> <span data-ttu-id="99f62-117"><xref:System.Data.Metadata.Edm> 命名空间自动包含在所有查询中。</span><span class="sxs-lookup"><span data-stu-id="99f62-117">The <xref:System.Data.Metadata.Edm> namespace is automatically included in all queries.</span></span> <span data-ttu-id="99f62-118">但如果导入的另一个命名空间包含与规范函数（在 <xref:System.Data.Metadata.Edm> 命名空间中）同名的函数，则必须指定命名空间。</span><span class="sxs-lookup"><span data-stu-id="99f62-118">However, if another namespace is imported that contains a function with the same name as a canonical function (in the <xref:System.Data.Metadata.Edm> namespace), you must specify the namespace.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="99f62-119">本节内容</span><span class="sxs-lookup"><span data-stu-id="99f62-119">In This Section</span></span>  

 [<span data-ttu-id="99f62-120">聚合规范函数</span><span class="sxs-lookup"><span data-stu-id="99f62-120">Aggregate Canonical Functions</span></span>](aggregate-canonical-functions.md)  
 <span data-ttu-id="99f62-121">讨论 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 聚合规范函数。</span><span class="sxs-lookup"><span data-stu-id="99f62-121">Discusses aggregate [!INCLUDE[esql](../../../../../../includes/esql-md.md)] canonical functions.</span></span>  
  
 [<span data-ttu-id="99f62-122">数学规范函数</span><span class="sxs-lookup"><span data-stu-id="99f62-122">Math Canonical Functions</span></span>](math-canonical-functions.md)  
 <span data-ttu-id="99f62-123">讨论 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 数学规范函数。</span><span class="sxs-lookup"><span data-stu-id="99f62-123">Discusses math [!INCLUDE[esql](../../../../../../includes/esql-md.md)] canonical functions.</span></span>  
  
 [<span data-ttu-id="99f62-124">字符串规范函数</span><span class="sxs-lookup"><span data-stu-id="99f62-124">String Canonical Functions</span></span>](string-canonical-functions.md)  
 <span data-ttu-id="99f62-125">讨论 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 字符串规范函数。</span><span class="sxs-lookup"><span data-stu-id="99f62-125">Discusses string [!INCLUDE[esql](../../../../../../includes/esql-md.md)] canonical functions.</span></span>  
  
 [<span data-ttu-id="99f62-126">日期和时间规范函数</span><span class="sxs-lookup"><span data-stu-id="99f62-126">Date and Time Canonical Functions</span></span>](date-and-time-canonical-functions.md)  
 <span data-ttu-id="99f62-127">讨论 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 日期和时间规范函数。</span><span class="sxs-lookup"><span data-stu-id="99f62-127">Discusses date and time [!INCLUDE[esql](../../../../../../includes/esql-md.md)] canonical functions.</span></span>  
  
 [<span data-ttu-id="99f62-128">按位规范函数</span><span class="sxs-lookup"><span data-stu-id="99f62-128">Bitwise Canonical Functions</span></span>](bitwise-canonical-functions.md)  
 <span data-ttu-id="99f62-129">讨论 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 按位规范函数。</span><span class="sxs-lookup"><span data-stu-id="99f62-129">Discusses bitwise [!INCLUDE[esql](../../../../../../includes/esql-md.md)] canonical functions.</span></span>  
  
 [<span data-ttu-id="99f62-130">空间函数</span><span class="sxs-lookup"><span data-stu-id="99f62-130">Spatial Functions</span></span>](spatial-functions.md)  
 <span data-ttu-id="99f62-131">讨论空间 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 规范函数。</span><span class="sxs-lookup"><span data-stu-id="99f62-131">Discusses Spatial [!INCLUDE[esql](../../../../../../includes/esql-md.md)] canonical functions.</span></span>  
  
 [<span data-ttu-id="99f62-132">其他规范函数</span><span class="sxs-lookup"><span data-stu-id="99f62-132">Other Canonical Functions</span></span>](other-canonical-functions.md)  
 <span data-ttu-id="99f62-133">讨论未分类为按位、日期/时间、字符串、数字或聚合函数的函数。</span><span class="sxs-lookup"><span data-stu-id="99f62-133">Discusses functions not classified as bitwise, date/time, string, math, or aggregate.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99f62-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="99f62-134">See also</span></span>

- [<span data-ttu-id="99f62-135">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="99f62-135">Entity SQL Overview</span></span>](entity-sql-overview.md)
- [<span data-ttu-id="99f62-136">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="99f62-136">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="99f62-137">SQL Server 函数映射的规范化概念模型</span><span class="sxs-lookup"><span data-stu-id="99f62-137">Conceptual Model Canonical to SQL Server Functions Mapping</span></span>](../conceptual-model-canonical-to-sql-server-functions-mapping.md)
- [<span data-ttu-id="99f62-138">用户定义函数</span><span class="sxs-lookup"><span data-stu-id="99f62-138">User-Defined Functions</span></span>](user-defined-functions-entity-sql.md)
