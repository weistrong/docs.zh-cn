---
description: 了解详细信息：将序列转换为泛型列表
title: 将某一序列转换为泛型列表
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7ab76d93-6898-4e75-b76f-290a66ecead8
ms.openlocfilehash: e9832fd366f22b77674fb4c83f6af7ce89a552c5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99663113"
---
# <a name="convert-a-sequence-to-a-generic-list"></a><span data-ttu-id="ecb6a-103">将某一序列转换为泛型列表</span><span class="sxs-lookup"><span data-stu-id="ecb6a-103">Convert a Sequence to a Generic List</span></span>

<span data-ttu-id="ecb6a-104">使用 <xref:System.Linq.Enumerable.ToList%2A> 可从序列创建泛型列表。</span><span class="sxs-lookup"><span data-stu-id="ecb6a-104">Use <xref:System.Linq.Enumerable.ToList%2A> to create a generic List from a sequence.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ecb6a-105">示例</span><span class="sxs-lookup"><span data-stu-id="ecb6a-105">Example</span></span>  

 <span data-ttu-id="ecb6a-106">下面的示例使用 <xref:System.Linq.Enumerable.ToList%2A> 直接将查询的计算结果放入泛型 <xref:System.Collections.Generic.List%601>。</span><span class="sxs-lookup"><span data-stu-id="ecb6a-106">The following sample uses <xref:System.Linq.Enumerable.ToList%2A> to immediately evaluate a query into a generic <xref:System.Collections.Generic.List%601>.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#45](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#45)]
 [!code-vb[DLinqQueryExamples#45](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#45)]  
  
## <a name="see-also"></a><span data-ttu-id="ecb6a-107">请参阅</span><span class="sxs-lookup"><span data-stu-id="ecb6a-107">See also</span></span>

- [<span data-ttu-id="ecb6a-108">查询示例</span><span class="sxs-lookup"><span data-stu-id="ecb6a-108">Query Examples</span></span>](query-examples.md)
