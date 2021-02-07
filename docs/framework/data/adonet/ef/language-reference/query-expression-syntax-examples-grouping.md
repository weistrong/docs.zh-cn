---
description: 了解详细信息：查询表达式语法示例：分组
title: 查询表达式语法示例：分组
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2d83d7c0-b3be-4c92-a630-25cd1285de31
ms.openlocfilehash: 1d8bd51a783cbd53716daebfa9b547f5e4fffc1f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696212"
---
# <a name="query-expression-syntax-examples-grouping"></a><span data-ttu-id="4eeb0-103">查询表达式语法示例：分组</span><span class="sxs-lookup"><span data-stu-id="4eeb0-103">Query Expression Syntax Examples: Grouping</span></span>

<span data-ttu-id="4eeb0-104">本主题中的示例演示如何使用 `GroupBy` 方法通过使用查询表达式语法来查询 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) 。</span><span class="sxs-lookup"><span data-stu-id="4eeb0-104">The examples in this topic demonstrate how to use the `GroupBy` method to query the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) using query expression syntax.</span></span> <span data-ttu-id="4eeb0-105">这些示例中使用的 AdventureWorks 销售模型从 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 等表生成。</span><span class="sxs-lookup"><span data-stu-id="4eeb0-105">The AdventureWorks Sales model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="4eeb0-106">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="4eeb0-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="example"></a><span data-ttu-id="4eeb0-107">示例</span><span class="sxs-lookup"><span data-stu-id="4eeb0-107">Example</span></span>  

 <span data-ttu-id="4eeb0-108">以下示例返回按邮政编码分组的 `Address` 对象。</span><span class="sxs-lookup"><span data-stu-id="4eeb0-108">The following example returns `Address` objects grouped by postal code.</span></span> <span data-ttu-id="4eeb0-109">这些结果将投影到一个匿名类型。</span><span class="sxs-lookup"><span data-stu-id="4eeb0-109">The results are projected into an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupBySimple3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbysimple3)]
 [!code-vb[DP L2E Examples#GroupBySimple3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbysimple3)]  
  
## <a name="example"></a><span data-ttu-id="4eeb0-110">示例</span><span class="sxs-lookup"><span data-stu-id="4eeb0-110">Example</span></span>  

 <span data-ttu-id="4eeb0-111">以下示例返回按联系人姓氏的第一个字母分组的 `Contact` 对象。</span><span class="sxs-lookup"><span data-stu-id="4eeb0-111">The following example returns `Contact` objects grouped by the first letter of the contact's last name.</span></span> <span data-ttu-id="4eeb0-112">这些结果还可以按姓氏的第一个字母进行排序，并投影到一个匿名类型。</span><span class="sxs-lookup"><span data-stu-id="4eeb0-112">The results are also sorted by the first letter of last name and projected into an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupBySimple2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbysimple2)]
 [!code-vb[DP L2E Examples#GroupBySimple2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbysimple2)]  
  
## <a name="example"></a><span data-ttu-id="4eeb0-113">示例</span><span class="sxs-lookup"><span data-stu-id="4eeb0-113">Example</span></span>  

 <span data-ttu-id="4eeb0-114">下面的示例返回按客户 ID 分组的 `SalesOrderHeader` 对象。</span><span class="sxs-lookup"><span data-stu-id="4eeb0-114">The following example returns `SalesOrderHeader` objects grouped by customer ID.</span></span> <span data-ttu-id="4eeb0-115">同时还返回每个客户的销售数量。</span><span class="sxs-lookup"><span data-stu-id="4eeb0-115">The number of sales for each customer is also returned.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupByCount](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbycount)]
 [!code-vb[DP L2E Examples#GroupByCount](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbycount)]  
  
## <a name="see-also"></a><span data-ttu-id="4eeb0-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="4eeb0-116">See also</span></span>

- [<span data-ttu-id="4eeb0-117">LINQ to Entities 中的查询</span><span class="sxs-lookup"><span data-stu-id="4eeb0-117">Queries in LINQ to Entities</span></span>](queries-in-linq-to-entities.md)
