---
description: 了解详细信息： Method-Based 查询语法示例：分区
title: 基于方法的查询语法示例：分区
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b7b64874-c3c8-4bdb-862c-89a168d07827
ms.openlocfilehash: 914dacb5b82b9ce452d4d1d7a97262de5803a9fa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696680"
---
# <a name="method-based-query-syntax-examples-partitioning"></a><span data-ttu-id="b9fcc-103">基于方法的查询语法示例：分区</span><span class="sxs-lookup"><span data-stu-id="b9fcc-103">Method-Based Query Syntax Examples: Partitioning</span></span>

<span data-ttu-id="b9fcc-104">本主题中的示例演示如何使用 <xref:System.Linq.Enumerable.Skip%2A> 和 <xref:System.Linq.Enumerable.Take%2A> 方法通过使用查询表达式语法来查询 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) 。</span><span class="sxs-lookup"><span data-stu-id="b9fcc-104">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.Skip%2A>, and <xref:System.Linq.Enumerable.Take%2A> methods to query the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) using query expression syntax.</span></span> <span data-ttu-id="b9fcc-105">这些示例中使用的 AdventureWorks 销售模型从 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 等表生成。</span><span class="sxs-lookup"><span data-stu-id="b9fcc-105">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="b9fcc-106">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="b9fcc-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="skip"></a><span data-ttu-id="b9fcc-107">跳过</span><span class="sxs-lookup"><span data-stu-id="b9fcc-107">Skip</span></span>  
  
### <a name="example"></a><span data-ttu-id="b9fcc-108">示例</span><span class="sxs-lookup"><span data-stu-id="b9fcc-108">Example</span></span>  

 <span data-ttu-id="b9fcc-109">以下示例使用 <xref:System.Linq.Enumerable.Skip%2A> 方法以获取 Contact 表中除前五个联系人之外的所有联系人。</span><span class="sxs-lookup"><span data-stu-id="b9fcc-109">The following example uses the <xref:System.Linq.Enumerable.Skip%2A> method to get all but the first five contacts of the Contact table.</span></span>  
  
 [!code-csharp[DP L2E Examples#SkipSimple](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#skipsimple)]
 [!code-vb[DP L2E Examples#SkipSimple](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#skipsimple)]  
  
### <a name="example"></a><span data-ttu-id="b9fcc-110">示例</span><span class="sxs-lookup"><span data-stu-id="b9fcc-110">Example</span></span>  

 <span data-ttu-id="b9fcc-111">以下示例使用 <xref:System.Linq.Enumerable.Skip%2A> 方法以获取 Seattle 的前两个地址之外的所有地址。</span><span class="sxs-lookup"><span data-stu-id="b9fcc-111">The following example uses the <xref:System.Linq.Enumerable.Skip%2A> method to get all but the first two addresses in Seattle.</span></span>  
  
 [!code-csharp[DP L2E Examples#SkipNested](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#skipnested)]
 [!code-vb[DP L2E Examples#SkipNested](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#skipnested)]  
  
## <a name="take"></a><span data-ttu-id="b9fcc-112">Take</span><span class="sxs-lookup"><span data-stu-id="b9fcc-112">Take</span></span>  
  
### <a name="example"></a><span data-ttu-id="b9fcc-113">示例</span><span class="sxs-lookup"><span data-stu-id="b9fcc-113">Example</span></span>  

 <span data-ttu-id="b9fcc-114">以下示例使用 <xref:System.Linq.Enumerable.Take%2A> 方法以只从 Contact 表中获取前五个联系人。</span><span class="sxs-lookup"><span data-stu-id="b9fcc-114">The following example uses the <xref:System.Linq.Enumerable.Take%2A> method to get only the first five contacts from the Contact table.</span></span>  
  
 [!code-csharp[DP L2E Examples#TakeSimple](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#takesimple)]
 [!code-vb[DP L2E Examples#TakeSimple](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#takesimple)]  
  
### <a name="example"></a><span data-ttu-id="b9fcc-115">示例</span><span class="sxs-lookup"><span data-stu-id="b9fcc-115">Example</span></span>  

 <span data-ttu-id="b9fcc-116">以下示例使用 <xref:System.Linq.Enumerable.Take%2A> 方法以获取 Seattle 的前三个地址。</span><span class="sxs-lookup"><span data-stu-id="b9fcc-116">The following example uses the <xref:System.Linq.Enumerable.Take%2A> method to get the first three addresses in Seattle.</span></span>  
  
 [!code-csharp[DP L2E Examples#TakeNested](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#takenested)]
 [!code-vb[DP L2E Examples#TakeNested](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#takenested)]  
  
## <a name="see-also"></a><span data-ttu-id="b9fcc-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="b9fcc-117">See also</span></span>

- [<span data-ttu-id="b9fcc-118">LINQ to Entities 中的查询</span><span class="sxs-lookup"><span data-stu-id="b9fcc-118">Queries in LINQ to Entities</span></span>](queries-in-linq-to-entities.md)
