---
description: 了解详细信息：如何：通过保留数据库值解决冲突
title: 如何：通过保留数据库值解决冲突
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b475cf72-9e64-4f6e-99c1-af7737bc85ef
ms.openlocfilehash: ef47370768ce474ccb6d941bcec0e66807290599
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723486"
---
# <a name="how-to-resolve-conflicts-by-retaining-database-values"></a><span data-ttu-id="0c7f2-103">如何：通过保留数据库值解决冲突</span><span class="sxs-lookup"><span data-stu-id="0c7f2-103">How to: Resolve Conflicts by Retaining Database Values</span></span>

<span data-ttu-id="0c7f2-104">若要先对帐预期数据库值与实际数据库值之间的差异，再尝试重新提交更改，则可以使用 <xref:System.Data.Linq.RefreshMode.OverwriteCurrentValues> 保留在数据库中找到的值。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-104">To reconcile differences between expected and actual database values before you try to resubmit your changes, you can use <xref:System.Data.Linq.RefreshMode.OverwriteCurrentValues> to retain the values found in the database.</span></span> <span data-ttu-id="0c7f2-105">然后会覆盖对象模型中的当前值。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-105">The current values in the object model are then overwritten.</span></span> <span data-ttu-id="0c7f2-106">有关详细信息，请参阅 [乐观 Concurrency：概述](optimistic-concurrency-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-106">For more information, see [Optimistic Concurrency: Overview](optimistic-concurrency-overview.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0c7f2-107">在所有情况下，都会先通过从数据库中检索更新后的数据来刷新客户端上的记录。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-107">In all cases, the record on the client is first refreshed by retrieving the updated data from the database.</span></span> <span data-ttu-id="0c7f2-108">此操作确保了下一次更新尝试将通过相同的并发检查。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-108">This action makes sure that the next update try will not fail on the same concurrency checks.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0c7f2-109">示例</span><span class="sxs-lookup"><span data-stu-id="0c7f2-109">Example</span></span>  

 <span data-ttu-id="0c7f2-110">在本方案中，当 User1 尝试提交更改时将引发 <xref:System.Data.Linq.ChangeConflictException> 异常，原因是 User2 同时已更改了 Assistant 和 Department 列。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-110">In this scenario, a <xref:System.Data.Linq.ChangeConflictException> exception is thrown when User1 tries to submit changes, because User2 has in the meantime changed the Assistant and Department columns.</span></span> <span data-ttu-id="0c7f2-111">下表说明了这种情况。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-111">The following table shows the situation.</span></span>  
  
||<span data-ttu-id="0c7f2-112">Manager</span><span class="sxs-lookup"><span data-stu-id="0c7f2-112">Manager</span></span>|<span data-ttu-id="0c7f2-113">Assistant</span><span class="sxs-lookup"><span data-stu-id="0c7f2-113">Assistant</span></span>|<span data-ttu-id="0c7f2-114">部门</span><span class="sxs-lookup"><span data-stu-id="0c7f2-114">Department</span></span>|  
|------|-------------|---------------|----------------|  
|<span data-ttu-id="0c7f2-115">原始数据库在被 User1 和 User2 查询时的状态。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-115">Original database state when queried by User1 and User2.</span></span>|<span data-ttu-id="0c7f2-116">Alfreds</span><span class="sxs-lookup"><span data-stu-id="0c7f2-116">Alfreds</span></span>|<span data-ttu-id="0c7f2-117">Maria</span><span class="sxs-lookup"><span data-stu-id="0c7f2-117">Maria</span></span>|<span data-ttu-id="0c7f2-118">Sales</span><span class="sxs-lookup"><span data-stu-id="0c7f2-118">Sales</span></span>|  
|<span data-ttu-id="0c7f2-119">User1 准备提交这些更改。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-119">User1 prepares to submit these changes.</span></span>|<span data-ttu-id="0c7f2-120">Alfred</span><span class="sxs-lookup"><span data-stu-id="0c7f2-120">Alfred</span></span>||<span data-ttu-id="0c7f2-121">Marketing</span><span class="sxs-lookup"><span data-stu-id="0c7f2-121">Marketing</span></span>|  
|<span data-ttu-id="0c7f2-122">User2 已经提交了这些更改。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-122">User2 has already submitted these changes.</span></span>||<span data-ttu-id="0c7f2-123">Mary</span><span class="sxs-lookup"><span data-stu-id="0c7f2-123">Mary</span></span>|<span data-ttu-id="0c7f2-124">服务</span><span class="sxs-lookup"><span data-stu-id="0c7f2-124">Service</span></span>|  
  
 <span data-ttu-id="0c7f2-125">User1 决定通过用更新的数据库值覆盖对象模型中的当前值来解决此冲突。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-125">User1 decides to resolve this conflict by having the newer database values overwrite the current values in the object model.</span></span>  
  
 <span data-ttu-id="0c7f2-126">User1 通过使用 <xref:System.Data.Linq.RefreshMode.OverwriteCurrentValues> 解决了此冲突后，数据库中的结果将如下表中所示：</span><span class="sxs-lookup"><span data-stu-id="0c7f2-126">When User1 resolves the conflict by using <xref:System.Data.Linq.RefreshMode.OverwriteCurrentValues>, the result in the database is as follows in the table:</span></span>  
  
||<span data-ttu-id="0c7f2-127">Manager</span><span class="sxs-lookup"><span data-stu-id="0c7f2-127">Manager</span></span>|<span data-ttu-id="0c7f2-128">Assistant</span><span class="sxs-lookup"><span data-stu-id="0c7f2-128">Assistant</span></span>|<span data-ttu-id="0c7f2-129">部门</span><span class="sxs-lookup"><span data-stu-id="0c7f2-129">Department</span></span>|  
|------|-------------|---------------|----------------|  
|<span data-ttu-id="0c7f2-130">解决冲突后的新状态。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-130">New state after conflict resolution.</span></span>|<span data-ttu-id="0c7f2-131">Alfreds</span><span class="sxs-lookup"><span data-stu-id="0c7f2-131">Alfreds</span></span><br /><br /> <span data-ttu-id="0c7f2-132">（原始）</span><span class="sxs-lookup"><span data-stu-id="0c7f2-132">(original)</span></span>|<span data-ttu-id="0c7f2-133">Mary</span><span class="sxs-lookup"><span data-stu-id="0c7f2-133">Mary</span></span><br /><br /> <span data-ttu-id="0c7f2-134">（来自 User2）</span><span class="sxs-lookup"><span data-stu-id="0c7f2-134">(from User2)</span></span>|<span data-ttu-id="0c7f2-135">服务</span><span class="sxs-lookup"><span data-stu-id="0c7f2-135">Service</span></span><br /><br /> <span data-ttu-id="0c7f2-136">（来自 User2）</span><span class="sxs-lookup"><span data-stu-id="0c7f2-136">(from User2)</span></span>|  
  
 <span data-ttu-id="0c7f2-137">下面的示例代码演示了如何用数据库值覆盖对象模型中的当前值。</span><span class="sxs-lookup"><span data-stu-id="0c7f2-137">The following example code shows how to overwrite current values in the object model with the database values.</span></span> <span data-ttu-id="0c7f2-138">（未对各个成员冲突进行检查或自定义处理。）</span><span class="sxs-lookup"><span data-stu-id="0c7f2-138">(No inspection or custom handling of individual member conflicts occurs.)</span></span>  
  
 [!code-csharp[System.Data.Linq.RefreshMode#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.refreshmode/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.RefreshMode#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.refreshmode/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="0c7f2-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="0c7f2-139">See also</span></span>

- [<span data-ttu-id="0c7f2-140">如何：管理更改冲突</span><span class="sxs-lookup"><span data-stu-id="0c7f2-140">How to: Manage Change Conflicts</span></span>](how-to-manage-change-conflicts.md)
