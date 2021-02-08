---
description: 了解详细信息：如何：检索实体冲突信息
title: 如何：检索实体冲突信息
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 9a02b608-e7bb-4041-a452-a7fed26fd008
ms.openlocfilehash: dde11a431ae977595b9845444e48705a4552fb23
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767747"
---
# <a name="how-to-retrieve-entity-conflict-information"></a><span data-ttu-id="497da-103">如何：检索实体冲突信息</span><span class="sxs-lookup"><span data-stu-id="497da-103">How to: Retrieve Entity Conflict Information</span></span>

<span data-ttu-id="497da-104">您可以使用 <xref:System.Data.Linq.ObjectChangeConflict> 类的对象来提供有关 <xref:System.Data.Linq.ChangeConflictException> 异常指出的冲突的信息。</span><span class="sxs-lookup"><span data-stu-id="497da-104">You can use objects of the <xref:System.Data.Linq.ObjectChangeConflict> class to provide information about conflicts revealed by <xref:System.Data.Linq.ChangeConflictException> exceptions.</span></span> <span data-ttu-id="497da-105">有关详细信息，请参阅 [乐观 Concurrency：概述](optimistic-concurrency-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="497da-105">For more information, see [Optimistic Concurrency: Overview](optimistic-concurrency-overview.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="497da-106">示例</span><span class="sxs-lookup"><span data-stu-id="497da-106">Example</span></span>  

 <span data-ttu-id="497da-107">下面的示例循环访问累积冲突的列表。</span><span class="sxs-lookup"><span data-stu-id="497da-107">The following example iterates through a list of accumulated conflicts.</span></span>  
  
 [!code-csharp[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.objectchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.objectchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="497da-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="497da-108">See also</span></span>

- [<span data-ttu-id="497da-109">如何：管理更改冲突</span><span class="sxs-lookup"><span data-stu-id="497da-109">How to: Manage Change Conflicts</span></span>](how-to-manage-change-conflicts.md)
