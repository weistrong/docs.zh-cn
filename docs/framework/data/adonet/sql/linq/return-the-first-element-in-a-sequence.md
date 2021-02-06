---
description: 了解详细信息：返回序列中的第一个元素
title: 返回序列中的第一个元素
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ccdc3777-b2c2-44e3-a627-abef8d79a555
ms.openlocfilehash: 004e9a1f03677f6ba49916404b1c44408df40dfa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99663009"
---
# <a name="return-the-first-element-in-a-sequence"></a><span data-ttu-id="29ae9-103">返回序列中的第一个元素</span><span class="sxs-lookup"><span data-stu-id="29ae9-103">Return the First Element in a Sequence</span></span>

<span data-ttu-id="29ae9-104">使用 <xref:System.Linq.Enumerable.First%2A> 运算符可返回序列中的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="29ae9-104">Use the <xref:System.Linq.Enumerable.First%2A> operator to return the first element in a sequence.</span></span> <span data-ttu-id="29ae9-105">使用 <xref:System.Linq.Enumerable.First%2A> 的查询是立即执行的。</span><span class="sxs-lookup"><span data-stu-id="29ae9-105">Queries that use <xref:System.Linq.Enumerable.First%2A> are executed immediately.</span></span>  
  
> [!NOTE]
> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="29ae9-106">不支持 <xref:System.Linq.Enumerable.Last%2A> 运算符。</span><span class="sxs-lookup"><span data-stu-id="29ae9-106">does not support the <xref:System.Linq.Enumerable.Last%2A> operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="29ae9-107">示例</span><span class="sxs-lookup"><span data-stu-id="29ae9-107">Example</span></span>  

 <span data-ttu-id="29ae9-108">下面的代码查找表中的第一个 `Shipper`：</span><span class="sxs-lookup"><span data-stu-id="29ae9-108">The following code finds the first `Shipper` in a table:</span></span>  
  
 <span data-ttu-id="29ae9-109">如果您对 Northwind 示例数据库运行此查询，则结果为</span><span class="sxs-lookup"><span data-stu-id="29ae9-109">If you run this query against the Northwind sample database, the results are</span></span>  
  
 <span data-ttu-id="29ae9-110">`ID = 1, Company = Speedy Express`.</span><span class="sxs-lookup"><span data-stu-id="29ae9-110">`ID = 1, Company = Speedy Express`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#14](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#14)]
 [!code-vb[DLinqQueryExamples#14](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#14)]  
  
## <a name="example"></a><span data-ttu-id="29ae9-111">示例</span><span class="sxs-lookup"><span data-stu-id="29ae9-111">Example</span></span>  

 <span data-ttu-id="29ae9-112">下面的代码查找具有 `Customer` BONAP 的单个 `CustomerID`。</span><span class="sxs-lookup"><span data-stu-id="29ae9-112">The following code finds the single `Customer` that has the `CustomerID` BONAP.</span></span>  
  
 <span data-ttu-id="29ae9-113">如果您对 Northwind 示例数据库运行此查询，则结果为 `ID = BONAP, Contact = Laurence Lebihan`。</span><span class="sxs-lookup"><span data-stu-id="29ae9-113">If you run this query against the Northwind sample database, the results are `ID = BONAP, Contact = Laurence Lebihan`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#15](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#15)]
 [!code-vb[DLinqQueryExamples#15](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#15)]  
  
## <a name="see-also"></a><span data-ttu-id="29ae9-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="29ae9-114">See also</span></span>

- [<span data-ttu-id="29ae9-115">查询示例</span><span class="sxs-lookup"><span data-stu-id="29ae9-115">Query Examples</span></span>](query-examples.md)
- [<span data-ttu-id="29ae9-116">下载示例数据库</span><span class="sxs-lookup"><span data-stu-id="29ae9-116">Downloading Sample Databases</span></span>](downloading-sample-databases.md)
