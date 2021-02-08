---
description: 了解详细信息：如何：关闭延迟加载
title: 如何：禁用推迟加载
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1b84b852-3cad-41a7-8077-149a70d50c8b
ms.openlocfilehash: 739c9b0b65eda73d6c504409395eb805b0c02873
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785830"
---
# <a name="how-to-turn-off-deferred-loading"></a><span data-ttu-id="62a02-103">如何：禁用推迟加载</span><span class="sxs-lookup"><span data-stu-id="62a02-103">How to: Turn Off Deferred Loading</span></span>

<span data-ttu-id="62a02-104">可以通过将 <xref:System.Data.Linq.DataContext.DeferredLoadingEnabled%2A> 设置为 `false` 来关闭延迟加载。</span><span class="sxs-lookup"><span data-stu-id="62a02-104">You can turn off deferred loading by setting <xref:System.Data.Linq.DataContext.DeferredLoadingEnabled%2A> to `false`.</span></span> <span data-ttu-id="62a02-105">有关详细信息，请参阅 [延迟与立即加载](deferred-versus-immediate-loading.md)。</span><span class="sxs-lookup"><span data-stu-id="62a02-105">For more information, see [Deferred versus Immediate Loading](deferred-versus-immediate-loading.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="62a02-106">关闭对象跟踪时，也隐式地关闭了延迟加载。</span><span class="sxs-lookup"><span data-stu-id="62a02-106">Deferred loading is turned off by implication when object tracking is turned off.</span></span> <span data-ttu-id="62a02-107">有关详细信息，请参阅 [如何：将信息检索为只读](how-to-retrieve-information-as-read-only.md)。</span><span class="sxs-lookup"><span data-stu-id="62a02-107">For more information, see [How to: Retrieve Information As Read-Only](how-to-retrieve-information-as-read-only.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="62a02-108">示例</span><span class="sxs-lookup"><span data-stu-id="62a02-108">Example</span></span>  

 <span data-ttu-id="62a02-109">下面的示例演示如何通过将 <xref:System.Data.Linq.DataContext.DeferredLoadingEnabled%2A> 设置为 `false` 来关闭延迟加载。</span><span class="sxs-lookup"><span data-stu-id="62a02-109">The following example shows how to turn off deferred loading by setting <xref:System.Data.Linq.DataContext.DeferredLoadingEnabled%2A> to `false`.</span></span>  
  
 [!code-csharp[DLinqQuerying#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQuerying/cs/Program.cs#3)]
 [!code-vb[DLinqQuerying#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQuerying/vb/Module1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="62a02-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="62a02-110">See also</span></span>

- [<span data-ttu-id="62a02-111">查询概念</span><span class="sxs-lookup"><span data-stu-id="62a02-111">Query Concepts</span></span>](query-concepts.md)
- [<span data-ttu-id="62a02-112">查询数据库</span><span class="sxs-lookup"><span data-stu-id="62a02-112">Querying the Database</span></span>](querying-the-database.md)
