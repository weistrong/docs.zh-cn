---
description: 了解详细信息： Method-Based 查询语法示例：排序
title: 基于方法的查询语法示例：中间件排序
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 5d21b178-d731-471a-8534-1f8184a2ef06
ms.openlocfilehash: 7b1c67ba66f549e82a57b5b34c645d36d1255a14
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696693"
---
# <a name="method-based-query-syntax-examples-ordering"></a><span data-ttu-id="18fbf-103">基于方法的查询语法示例：中间件排序</span><span class="sxs-lookup"><span data-stu-id="18fbf-103">Method-Based Query Syntax Examples: Ordering</span></span>

<span data-ttu-id="18fbf-104">本主题中的示例演示如何使用 <xref:System.Linq.Enumerable.ThenBy%2A> 方法通过使用基于方法的查询语法来查询 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) 。</span><span class="sxs-lookup"><span data-stu-id="18fbf-104">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.ThenBy%2A> method to query the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) using method-based query syntax.</span></span> <span data-ttu-id="18fbf-105">这些示例中使用的 AdventureWorks 销售模型从 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 等表生成。</span><span class="sxs-lookup"><span data-stu-id="18fbf-105">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="18fbf-106">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="18fbf-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="thenby"></a><span data-ttu-id="18fbf-107">ThenBy</span><span class="sxs-lookup"><span data-stu-id="18fbf-107">ThenBy</span></span>  
  
### <a name="example"></a><span data-ttu-id="18fbf-108">示例</span><span class="sxs-lookup"><span data-stu-id="18fbf-108">Example</span></span>  

 <span data-ttu-id="18fbf-109">采用基于方法的查询语法的以下示例使用 <xref:System.Linq.Queryable.OrderBy%2A> 和 <xref:System.Linq.Queryable.ThenBy%2A> 以返回先按姓氏后按名字排序的联系人列表。</span><span class="sxs-lookup"><span data-stu-id="18fbf-109">The following example in method-based query syntax uses <xref:System.Linq.Queryable.OrderBy%2A> and <xref:System.Linq.Queryable.ThenBy%2A> to return a list of contacts ordered by last name and then by first name.</span></span>  
  
 [!code-csharp[DP L2E Examples#OrderByThenBy_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#orderbythenby_mq)]
 [!code-vb[DP L2E Examples#OrderByThenBy_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#orderbythenby_mq)]  
  
## <a name="thenbydescending"></a><span data-ttu-id="18fbf-110">ThenByDescending</span><span class="sxs-lookup"><span data-stu-id="18fbf-110">ThenByDescending</span></span>  
  
### <a name="example"></a><span data-ttu-id="18fbf-111">示例</span><span class="sxs-lookup"><span data-stu-id="18fbf-111">Example</span></span>  

 <span data-ttu-id="18fbf-112">以下示例使用 <xref:System.Linq.Queryable.OrderBy%2A> 和 <xref:System.Linq.Queryable.ThenByDescending%2A> 方法以首先按标价排序，然后执行产品名称的降序排序。</span><span class="sxs-lookup"><span data-stu-id="18fbf-112">The following example uses the <xref:System.Linq.Queryable.OrderBy%2A> and <xref:System.Linq.Queryable.ThenByDescending%2A> methods to first sort by list price, and then perform a descending sort of the product names.</span></span>  
  
 [!code-csharp[DP L2E Examples#ThenByDescending_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#thenbydescending_mq)]
 [!code-vb[DP L2E Examples#ThenByDescending_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#thenbydescending_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="18fbf-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="18fbf-113">See also</span></span>

- [<span data-ttu-id="18fbf-114">LINQ to Entities 中的查询</span><span class="sxs-lookup"><span data-stu-id="18fbf-114">Queries in LINQ to Entities</span></span>](queries-in-linq-to-entities.md)
