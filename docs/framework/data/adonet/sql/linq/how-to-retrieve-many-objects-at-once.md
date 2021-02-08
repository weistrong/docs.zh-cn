---
description: 了解有关详细信息，请参阅如何：一次检索多个对象
title: 如何：一次检索多个对象
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 18aff4d8-bde8-461b-9960-ccabb24e9d22
ms.openlocfilehash: 2bc202e09c64f2a1956b8688be30cfd87fb655c0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802003"
---
# <a name="how-to-retrieve-many-objects-at-once"></a><span data-ttu-id="b8047-103">如何：一次检索多个对象</span><span class="sxs-lookup"><span data-stu-id="b8047-103">How to: Retrieve Many Objects At Once</span></span>

<span data-ttu-id="b8047-104">通过使用 <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>，可以在一个查询中检索许多对象。</span><span class="sxs-lookup"><span data-stu-id="b8047-104">You can retrieve many objects in one query by using <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b8047-105">示例</span><span class="sxs-lookup"><span data-stu-id="b8047-105">Example</span></span>  

 <span data-ttu-id="b8047-106">下面的代码使用 <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> 方法来同时检索 `Customer` 和 `Order` 对象。</span><span class="sxs-lookup"><span data-stu-id="b8047-106">The following code uses the <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> method to retrieve both `Customer` and `Order` objects.</span></span>  
  
 [!code-csharp[DLinqQueryConcepts#9](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#9)]
 [!code-vb[DLinqQueryConcepts#9](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#9)]  
  
## <a name="see-also"></a><span data-ttu-id="b8047-107">请参阅</span><span class="sxs-lookup"><span data-stu-id="b8047-107">See also</span></span>

- [<span data-ttu-id="b8047-108">查询概念</span><span class="sxs-lookup"><span data-stu-id="b8047-108">Query Concepts</span></span>](query-concepts.md)
