---
description: 了解详细信息：如何：筛选相关数据
title: 如何：筛选相关数据
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ec8b8f97-5d01-4f31-9b97-d1556df6a4bc
ms.openlocfilehash: d44e0805b82c0c58f9ee19808e078f9f9b337050
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738944"
---
# <a name="how-to-filter-related-data"></a><span data-ttu-id="5cb39-103">如何：筛选相关数据</span><span class="sxs-lookup"><span data-stu-id="5cb39-103">How to: Filter Related Data</span></span>

<span data-ttu-id="5cb39-104">使用 <xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> 方法可指定用来限制检索到的数据量的子查询。</span><span class="sxs-lookup"><span data-stu-id="5cb39-104">Use the <xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> method to specify sub-queries to limit the amount of retrieved data.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5cb39-105">示例</span><span class="sxs-lookup"><span data-stu-id="5cb39-105">Example</span></span>  

 <span data-ttu-id="5cb39-106">在下面的示例中，<xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> 方法将检索到的 `Orders` 限制为今天尚未发货的那些订单。</span><span class="sxs-lookup"><span data-stu-id="5cb39-106">In the following example, the <xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> method limits the `Orders` retrieved to those that have not been shipped today.</span></span> <span data-ttu-id="5cb39-107">如果不使用这种方式，则即使只需要一部分订单，也会检索到所有 `Orders`。</span><span class="sxs-lookup"><span data-stu-id="5cb39-107">Without this approach, all `Orders` would have been retrieved even though only a subset is desired.</span></span>  
  
 [!code-csharp[System.Data.Linq.DataLoadOptions#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.dataloadoptions/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.DataLoadOptions#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.dataloadoptions/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="5cb39-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="5cb39-108">See also</span></span>

- [<span data-ttu-id="5cb39-109">查询数据库</span><span class="sxs-lookup"><span data-stu-id="5cb39-109">Querying the Database</span></span>](querying-the-database.md)
