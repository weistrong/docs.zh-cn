---
description: 了解详细信息：如何：检索成员冲突信息
title: 如何：检索成员冲突信息
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7dd6829e-79a5-4480-9023-9e588cb0bf2e
ms.openlocfilehash: 2a33aba1a113bdfd66bdc341bfc9ae59406f2c40
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723395"
---
# <a name="how-to-retrieve-member-conflict-information"></a><span data-ttu-id="40e3f-103">如何：检索成员冲突信息</span><span class="sxs-lookup"><span data-stu-id="40e3f-103">How to: Retrieve Member Conflict Information</span></span>

<span data-ttu-id="40e3f-104">您可以使用 <xref:System.Data.Linq.MemberChangeConflict> 类检索有关发生冲突的各成员的信息。</span><span class="sxs-lookup"><span data-stu-id="40e3f-104">You can use the <xref:System.Data.Linq.MemberChangeConflict> class to retrieve information about individual members in conflict.</span></span> <span data-ttu-id="40e3f-105">在此上下文中，您可以提供任何成员的冲突的自定义处理方法。</span><span class="sxs-lookup"><span data-stu-id="40e3f-105">In this same context you can provide for custom handling of the conflict for any member.</span></span> <span data-ttu-id="40e3f-106">有关详细信息，请参阅 [乐观 Concurrency：概述](optimistic-concurrency-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="40e3f-106">For more information, see [Optimistic Concurrency: Overview](optimistic-concurrency-overview.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="40e3f-107">示例</span><span class="sxs-lookup"><span data-stu-id="40e3f-107">Example</span></span>  

 <span data-ttu-id="40e3f-108">下面的代码循环访问 <xref:System.Data.Linq.ObjectChangeConflict> 对象。</span><span class="sxs-lookup"><span data-stu-id="40e3f-108">The following code iterates through the <xref:System.Data.Linq.ObjectChangeConflict> objects.</span></span> <span data-ttu-id="40e3f-109">对于每个对象，它会接着循环访问 <xref:System.Data.Linq.MemberChangeConflict> 对象。</span><span class="sxs-lookup"><span data-stu-id="40e3f-109">For each object, it then iterates through the <xref:System.Data.Linq.MemberChangeConflict> objects.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="40e3f-110">请将 <xref:System.Reflection> 包含在内以提供 <xref:System.Data.Linq.MemberChangeConflict.Member%2A> 信息。</span><span class="sxs-lookup"><span data-stu-id="40e3f-110">Include <xref:System.Reflection> in order to provide <xref:System.Data.Linq.MemberChangeConflict.Member%2A> information.</span></span>  
  
 [!code-csharp[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.memberchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.memberchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="40e3f-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="40e3f-111">See also</span></span>

- [<span data-ttu-id="40e3f-112">如何：管理更改冲突</span><span class="sxs-lookup"><span data-stu-id="40e3f-112">How to: Manage Change Conflicts</span></span>](how-to-manage-change-conflicts.md)
