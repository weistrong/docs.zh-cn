---
description: 了解详细信息： Method-Based 查询语法示例：分组
title: 基于方法的查询语法示例：分组
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: cb23c25c-1075-4cc3-a8ff-4db72e536c0d
ms.openlocfilehash: dd605076a425207aa379216a9e8dba60eaeebc29
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99673500"
---
# <a name="method-based-query-syntax-examples-grouping"></a><span data-ttu-id="40dd7-103">基于方法的查询语法示例：分组</span><span class="sxs-lookup"><span data-stu-id="40dd7-103">Method-Based Query Syntax Examples: Grouping</span></span>

<span data-ttu-id="40dd7-104">本主题中的示例说明如何使用 `GroupBy` 方法通过使用基于方法的查询语法来查询 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) 。</span><span class="sxs-lookup"><span data-stu-id="40dd7-104">The examples in this topic show you how to use the `GroupBy` method to query the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) using method-based query syntax.</span></span> <span data-ttu-id="40dd7-105">这些示例中使用的 AdventureWorks 销售模型基于 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 表生成。</span><span class="sxs-lookup"><span data-stu-id="40dd7-105">The AdventureWorks Sales Model that is used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="40dd7-106">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="40dd7-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="example"></a><span data-ttu-id="40dd7-107">示例</span><span class="sxs-lookup"><span data-stu-id="40dd7-107">Example</span></span>  

 <span data-ttu-id="40dd7-108">下面的示例使用 `GroupBy` 方法来返回按邮政编码分组的 `Address` 对象。</span><span class="sxs-lookup"><span data-stu-id="40dd7-108">The following example uses the `GroupBy` method to return `Address` objects that are grouped by postal code.</span></span> <span data-ttu-id="40dd7-109">这些结果将投影到一个匿名类型。</span><span class="sxs-lookup"><span data-stu-id="40dd7-109">The results are projected into an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupBySimple3_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbysimple3_mq)]
 [!code-vb[DP L2E Examples#GroupBySimple3_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbysimple3_mq)]  
  
## <a name="example"></a><span data-ttu-id="40dd7-110">示例</span><span class="sxs-lookup"><span data-stu-id="40dd7-110">Example</span></span>  

 <span data-ttu-id="40dd7-111">下面的示例使用 `GroupBy` 方法来返回按联系人姓氏的首字母分组的 `Contact` 对象。</span><span class="sxs-lookup"><span data-stu-id="40dd7-111">The following example uses the `GroupBy` method to return `Contact` objects that are grouped by the first letter of the contact's last name.</span></span> <span data-ttu-id="40dd7-112">这些结果还按姓氏的首字母进行排序，并投影到一个匿名类型。</span><span class="sxs-lookup"><span data-stu-id="40dd7-112">The results are also sorted by the first letter of the last name and projected into an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupBySimple2_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbysimple2_mq)]
 [!code-vb[DP L2E Examples#GroupBySimple2_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbysimple2_mq)]  
  
## <a name="example"></a><span data-ttu-id="40dd7-113">示例</span><span class="sxs-lookup"><span data-stu-id="40dd7-113">Example</span></span>  

 <span data-ttu-id="40dd7-114">下面的示例使用 `GroupBy` 方法来返回按客户 ID 分组的 `SalesOrderHeader` 对象。</span><span class="sxs-lookup"><span data-stu-id="40dd7-114">The following example uses the `GroupBy` method to return `SalesOrderHeader` objects that are grouped by customer ID.</span></span> <span data-ttu-id="40dd7-115">同时还返回每个客户的销售数量。</span><span class="sxs-lookup"><span data-stu-id="40dd7-115">The number of sales for each customer is also returned.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupByCount_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbycount_mq)]
 [!code-vb[DP L2E Examples#GroupByCount_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbycount_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="40dd7-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="40dd7-116">See also</span></span>

- [<span data-ttu-id="40dd7-117">LINQ to Entities 中的查询</span><span class="sxs-lookup"><span data-stu-id="40dd7-117">Queries in LINQ to Entities</span></span>](queries-in-linq-to-entities.md)
