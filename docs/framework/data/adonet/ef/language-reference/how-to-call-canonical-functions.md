---
description: 了解详细信息：如何：调用规范函数
title: 如何：调用规范函数
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b3d84873-7403-4957-8e20-b4ae39f50214
ms.openlocfilehash: d1e2310bccd6cc60177dba9a2e4c3a104702ba0c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696836"
---
# <a name="how-to-call-canonical-functions"></a><span data-ttu-id="14b45-103">如何：调用规范函数</span><span class="sxs-lookup"><span data-stu-id="14b45-103">How to: Call Canonical Functions</span></span>

<span data-ttu-id="14b45-104"><xref:System.Data.Objects.EntityFunctions> 类包含公开要在 LINQ to Entities 查询中使用的规范函数的方法。</span><span class="sxs-lookup"><span data-stu-id="14b45-104">The <xref:System.Data.Objects.EntityFunctions> class contains methods that expose canonical functions to use in LINQ to Entities queries.</span></span> <span data-ttu-id="14b45-105">有关规范函数的信息，请参阅[规范函数](canonical-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="14b45-105">For information about canonical functions, see [Canonical Functions](canonical-functions.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="14b45-106"><xref:System.Data.Objects.EntityFunctions.AsUnicode%2A> 类中的 <xref:System.Data.Objects.EntityFunctions.AsNonUnicode%2A> 和 <xref:System.Data.Objects.EntityFunctions> 方法不具有规范函数等效性。</span><span class="sxs-lookup"><span data-stu-id="14b45-106">The <xref:System.Data.Objects.EntityFunctions.AsUnicode%2A> and <xref:System.Data.Objects.EntityFunctions.AsNonUnicode%2A> methods in the <xref:System.Data.Objects.EntityFunctions> class do not have canonical function equivalents.</span></span>  
  
 <span data-ttu-id="14b45-107">可以直接调用对一组值执行计算并返回单个值的规范函数（也成为聚合规范函数）。</span><span class="sxs-lookup"><span data-stu-id="14b45-107">Canonical functions that perform a calculation on a set of values and return a single value (also known as aggregate canonical functions) can be directly invoked.</span></span> <span data-ttu-id="14b45-108">其他规范函数只能作为 LINQ to Entities 查询的一部分调用。</span><span class="sxs-lookup"><span data-stu-id="14b45-108">Other canonical functions can only be called as part of a LINQ to Entities query.</span></span> <span data-ttu-id="14b45-109">若要直接调用聚合函数，必须将 <xref:System.Data.Objects.ObjectQuery%601> 传递到此函数。</span><span class="sxs-lookup"><span data-stu-id="14b45-109">To call an aggregate function directly, you must pass an <xref:System.Data.Objects.ObjectQuery%601> to the function.</span></span> <span data-ttu-id="14b45-110">有关更多信息，请参见下面的第二个示例。</span><span class="sxs-lookup"><span data-stu-id="14b45-110">For more information, see the second example below.</span></span>  
  
 <span data-ttu-id="14b45-111">可以在 LINQ to Entities 查询中使用公共语言运行时 (CLR) 方法调用某些规范函数。</span><span class="sxs-lookup"><span data-stu-id="14b45-111">You can call some canonical functions by using common language runtime (CLR) methods in LINQ to Entities queries.</span></span> <span data-ttu-id="14b45-112">有关映射到规范函数的 CLR 方法的列表，请参阅 [Clr 方法到规范函数的映射](clr-method-to-canonical-function-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="14b45-112">For a list of CLR methods that map to canonical functions, see [CLR Method to Canonical Function Mapping](clr-method-to-canonical-function-mapping.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="14b45-113">示例</span><span class="sxs-lookup"><span data-stu-id="14b45-113">Example</span></span>  

 <span data-ttu-id="14b45-114">下面的示例使用 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)。</span><span class="sxs-lookup"><span data-stu-id="14b45-114">The following example uses the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks).</span></span> <span data-ttu-id="14b45-115">此示例执行一个 LINQ to Entities 查询，该查询使用 <xref:System.Data.Objects.EntityFunctions.DiffDays%2A> 方法返回 `SellEndDate` 与 `SellStartDate` 之间相差小于 365 天的所有产品：</span><span class="sxs-lookup"><span data-stu-id="14b45-115">The example executes a LINQ to Entities query that uses the <xref:System.Data.Objects.EntityFunctions.DiffDays%2A> method to return all products for which the difference between `SellEndDate` and `SellStartDate` is less than 365 days:</span></span>  
  
 [!code-csharp[DP L2E CanonicalAndStoreFunctions#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp l2e canonicalandstorefunctions/cs/program.cs#1)]
 [!code-vb[DP L2E CanonicalAndStoreFunctions#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp l2e canonicalandstorefunctions/vb/module1.vb#1)]  
  
## <a name="example"></a><span data-ttu-id="14b45-116">示例</span><span class="sxs-lookup"><span data-stu-id="14b45-116">Example</span></span>  

 <span data-ttu-id="14b45-117">下面的示例使用 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)。</span><span class="sxs-lookup"><span data-stu-id="14b45-117">The following example uses the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks).</span></span> <span data-ttu-id="14b45-118">此示例直接调用聚合 <xref:System.Data.Objects.EntityFunctions.StandardDeviation%2A> 方法，以返回 `SalesOrderHeader` 小计的标准偏差。</span><span class="sxs-lookup"><span data-stu-id="14b45-118">The example calls the aggregate <xref:System.Data.Objects.EntityFunctions.StandardDeviation%2A> method directly to return the standard deviation of `SalesOrderHeader` subtotals.</span></span> <span data-ttu-id="14b45-119">请注意，应将 <xref:System.Data.Objects.ObjectQuery%601> 传递给此函数，这样，就可以调用它而不需要使它成为 LINQ to Entities 查询的一部分。</span><span class="sxs-lookup"><span data-stu-id="14b45-119">Note that an <xref:System.Data.Objects.ObjectQuery%601> is passed to the function, which allows it to be called without being part of a LINQ to Entities query.</span></span>  
  
 [!code-csharp[DP L2E CanonicalAndStoreFunctions#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp l2e canonicalandstorefunctions/cs/program.cs#2)]
 [!code-vb[DP L2E CanonicalAndStoreFunctions#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp l2e canonicalandstorefunctions/vb/module1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="14b45-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="14b45-120">See also</span></span>

- [<span data-ttu-id="14b45-121">在 LINQ to Entities 查询中调用函数</span><span class="sxs-lookup"><span data-stu-id="14b45-121">Calling Functions in LINQ to Entities Queries</span></span>](calling-functions-in-linq-to-entities-queries.md)
- [<span data-ttu-id="14b45-122">LINQ to Entities 中的查询</span><span class="sxs-lookup"><span data-stu-id="14b45-122">Queries in LINQ to Entities</span></span>](queries-in-linq-to-entities.md)
