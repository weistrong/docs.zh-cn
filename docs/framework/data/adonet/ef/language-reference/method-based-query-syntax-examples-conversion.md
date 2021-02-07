---
description: 了解详细信息： Method-Based 查询语法示例：转换
title: 基于方法的查询语法示例：转换
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 19f66872-d5ab-49f8-969f-e53f9632a13d
ms.openlocfilehash: 054ef9291a66216b14e2f03ecebd28fb24c6574d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696745"
---
# <a name="method-based-query-syntax-examples-conversion"></a><span data-ttu-id="f176b-103">基于方法的查询语法示例：转换</span><span class="sxs-lookup"><span data-stu-id="f176b-103">Method-Based Query Syntax Examples: Conversion</span></span>

<span data-ttu-id="f176b-104">本主题中的示例演示如何使用 <xref:System.Linq.Enumerable.ToArray%2A> <xref:System.Linq.Enumerable.ToDictionary%2A> 和 <xref:System.Linq.Enumerable.ToList%2A> 方法，通过基于方法的查询语法来查询 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) 。</span><span class="sxs-lookup"><span data-stu-id="f176b-104">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.ToArray%2A>, <xref:System.Linq.Enumerable.ToDictionary%2A> and <xref:System.Linq.Enumerable.ToList%2A> methods to query the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) using method-based query syntax.</span></span> <span data-ttu-id="f176b-105">这些示例中使用的 AdventureWorks 销售模型从 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 等表生成。</span><span class="sxs-lookup"><span data-stu-id="f176b-105">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="f176b-106">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="f176b-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="toarray"></a><span data-ttu-id="f176b-107">ToArray</span><span class="sxs-lookup"><span data-stu-id="f176b-107">ToArray</span></span>  
  
### <a name="example"></a><span data-ttu-id="f176b-108">示例</span><span class="sxs-lookup"><span data-stu-id="f176b-108">Example</span></span>  

 <span data-ttu-id="f176b-109">以下示例使用 <xref:System.Linq.Enumerable.ToArray%2A> 方法以立即将序列转换为数组。</span><span class="sxs-lookup"><span data-stu-id="f176b-109">The following example uses the <xref:System.Linq.Enumerable.ToArray%2A> method to immediately evaluate a sequence into an array.</span></span>  
  
 [!code-csharp[DP L2E Examples#ToArray](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#toarray)]
 [!code-vb[DP L2E Examples#ToArray](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#toarray)]  
  
## <a name="todictionary"></a><span data-ttu-id="f176b-110">ToDictionary</span><span class="sxs-lookup"><span data-stu-id="f176b-110">ToDictionary</span></span>  
  
### <a name="example"></a><span data-ttu-id="f176b-111">示例</span><span class="sxs-lookup"><span data-stu-id="f176b-111">Example</span></span>  

 <span data-ttu-id="f176b-112">以下示例使用 <xref:System.Linq.Enumerable.ToDictionary%2A> 方法以立即将序列和相关的键表达式转换为字典。</span><span class="sxs-lookup"><span data-stu-id="f176b-112">The following example uses the <xref:System.Linq.Enumerable.ToDictionary%2A> method to immediately evaluate a sequence and a related key expression into a dictionary.</span></span>  
  
 [!code-csharp[DP L2E Examples#ToDictionary](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#todictionary)]
 [!code-vb[DP L2E Examples#ToDictionary](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#todictionary)]  
  
## <a name="tolist"></a><span data-ttu-id="f176b-113">ToList</span><span class="sxs-lookup"><span data-stu-id="f176b-113">ToList</span></span>  
  
### <a name="example"></a><span data-ttu-id="f176b-114">示例</span><span class="sxs-lookup"><span data-stu-id="f176b-114">Example</span></span>  

 <span data-ttu-id="f176b-115">以下示例使用 <xref:System.Linq.Enumerable.ToList%2A> 方法以立即将序列转换为 <xref:System.Collections.Generic.List%601>，其中，`T` 属于类型 <xref:System.Data.DataRow>。</span><span class="sxs-lookup"><span data-stu-id="f176b-115">The following example uses the <xref:System.Linq.Enumerable.ToList%2A> method to immediately evaluate a sequence into a <xref:System.Collections.Generic.List%601>, where `T` is of type <xref:System.Data.DataRow>.</span></span>  
  
 [!code-csharp[DP L2E Examples#ToList](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#tolist)]
 [!code-vb[DP L2E Examples#ToList](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#tolist)]  
  
## <a name="see-also"></a><span data-ttu-id="f176b-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="f176b-116">See also</span></span>

- [<span data-ttu-id="f176b-117">LINQ to Entities 中的查询</span><span class="sxs-lookup"><span data-stu-id="f176b-117">Queries in LINQ to Entities</span></span>](queries-in-linq-to-entities.md)
