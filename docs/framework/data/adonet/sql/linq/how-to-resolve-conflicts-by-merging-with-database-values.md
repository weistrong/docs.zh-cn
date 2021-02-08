---
description: 了解有关详细信息，请参阅如何：通过与数据库值合并解决冲突
title: 如何：通过与数据库值合并解决冲突
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1988b79c-3bfc-4c5c-a08a-86cf638bbe17
ms.openlocfilehash: 83cae4c98fdd2e51065c66d36ef04202bdc86c9e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767760"
---
# <a name="how-to-resolve-conflicts-by-merging-with-database-values"></a><span data-ttu-id="f3935-103">如何：通过与数据库值合并解决冲突</span><span class="sxs-lookup"><span data-stu-id="f3935-103">How to: Resolve Conflicts by Merging with Database Values</span></span>

<span data-ttu-id="f3935-104">若要先对帐预期数据库值与实际数据库值之间的差异，再尝试重新提交更改，则可以使用 <xref:System.Data.Linq.RefreshMode.KeepChanges> 将数据库值与当前客户端成员值合并。</span><span class="sxs-lookup"><span data-stu-id="f3935-104">To reconcile differences between expected and actual database values before you try to resubmit your changes, you can use <xref:System.Data.Linq.RefreshMode.KeepChanges> to merge database values with the current client member values.</span></span> <span data-ttu-id="f3935-105">有关详细信息，请参阅 [乐观 Concurrency：概述](optimistic-concurrency-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f3935-105">For more information, see [Optimistic Concurrency: Overview](optimistic-concurrency-overview.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f3935-106">在所有情况下，都会先通过从数据库中检索更新后的数据来刷新客户端上的记录。</span><span class="sxs-lookup"><span data-stu-id="f3935-106">In all cases, the record on the client is first refreshed by retrieving the updated data from the database.</span></span> <span data-ttu-id="f3935-107">此操作确保了下一次更新尝试将通过相同的并发检查。</span><span class="sxs-lookup"><span data-stu-id="f3935-107">This action makes sure that the next update try will not fail on the same concurrency checks.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f3935-108">示例</span><span class="sxs-lookup"><span data-stu-id="f3935-108">Example</span></span>  

 <span data-ttu-id="f3935-109">在本方案中，当 User1 尝试提交更改时将引发 <xref:System.Data.Linq.ChangeConflictException> 异常，原因是 User2 同时已更改了 Assistant 和 Department 列。</span><span class="sxs-lookup"><span data-stu-id="f3935-109">In this scenario, a <xref:System.Data.Linq.ChangeConflictException> exception is thrown when User1 tries to submit changes, because User2 has in the meantime changed the Assistant and Department columns.</span></span> <span data-ttu-id="f3935-110">下表说明了这种情况。</span><span class="sxs-lookup"><span data-stu-id="f3935-110">The following table shows the situation.</span></span>  
  
||<span data-ttu-id="f3935-111">Manager</span><span class="sxs-lookup"><span data-stu-id="f3935-111">Manager</span></span>|<span data-ttu-id="f3935-112">Assistant</span><span class="sxs-lookup"><span data-stu-id="f3935-112">Assistant</span></span>|<span data-ttu-id="f3935-113">部门</span><span class="sxs-lookup"><span data-stu-id="f3935-113">Department</span></span>|  
|------|-------------|---------------|----------------|  
|<span data-ttu-id="f3935-114">原始数据库在被 User1 和 User2 查询时的状态。</span><span class="sxs-lookup"><span data-stu-id="f3935-114">Original database state when queried by User1 and User2.</span></span>|<span data-ttu-id="f3935-115">Alfreds</span><span class="sxs-lookup"><span data-stu-id="f3935-115">Alfreds</span></span>|<span data-ttu-id="f3935-116">Maria</span><span class="sxs-lookup"><span data-stu-id="f3935-116">Maria</span></span>|<span data-ttu-id="f3935-117">Sales</span><span class="sxs-lookup"><span data-stu-id="f3935-117">Sales</span></span>|  
|<span data-ttu-id="f3935-118">User1 准备提交这些更改。</span><span class="sxs-lookup"><span data-stu-id="f3935-118">User1 prepares to submit these changes.</span></span>|<span data-ttu-id="f3935-119">Alfred</span><span class="sxs-lookup"><span data-stu-id="f3935-119">Alfred</span></span>||<span data-ttu-id="f3935-120">Marketing</span><span class="sxs-lookup"><span data-stu-id="f3935-120">Marketing</span></span>|  
|<span data-ttu-id="f3935-121">User2 已经提交了这些更改。</span><span class="sxs-lookup"><span data-stu-id="f3935-121">User2 has already submitted these changes.</span></span>||<span data-ttu-id="f3935-122">Mary</span><span class="sxs-lookup"><span data-stu-id="f3935-122">Mary</span></span>|<span data-ttu-id="f3935-123">服务</span><span class="sxs-lookup"><span data-stu-id="f3935-123">Service</span></span>|  
  
 <span data-ttu-id="f3935-124">User1 决定通过将数据库值与当前客户端成员值合并来解决此冲突。</span><span class="sxs-lookup"><span data-stu-id="f3935-124">User1 decides to resolve this conflict by merging database values with the current client member values.</span></span> <span data-ttu-id="f3935-125">结果将是，数据库值仅在当前变更集也修改了该值时才会被覆盖。</span><span class="sxs-lookup"><span data-stu-id="f3935-125">The result will be that database values are overwritten only when the current changeset has also modified that value.</span></span>  
  
 <span data-ttu-id="f3935-126">User1 通过使用 <xref:System.Data.Linq.RefreshMode.KeepChanges> 解决了此冲突后，数据库中的结果将如下表所示：</span><span class="sxs-lookup"><span data-stu-id="f3935-126">When User1 resolves the conflict by using <xref:System.Data.Linq.RefreshMode.KeepChanges>, the result in the database is as in the following table:</span></span>  
  
||<span data-ttu-id="f3935-127">Manager</span><span class="sxs-lookup"><span data-stu-id="f3935-127">Manager</span></span>|<span data-ttu-id="f3935-128">Assistant</span><span class="sxs-lookup"><span data-stu-id="f3935-128">Assistant</span></span>|<span data-ttu-id="f3935-129">部门</span><span class="sxs-lookup"><span data-stu-id="f3935-129">Department</span></span>|  
|------|-------------|---------------|----------------|  
|<span data-ttu-id="f3935-130">解决冲突后的新状态。</span><span class="sxs-lookup"><span data-stu-id="f3935-130">New state after conflict resolution.</span></span>|<span data-ttu-id="f3935-131">Alfred</span><span class="sxs-lookup"><span data-stu-id="f3935-131">Alfred</span></span><br /><br /> <span data-ttu-id="f3935-132">（来自 User1）</span><span class="sxs-lookup"><span data-stu-id="f3935-132">(from User1)</span></span>|<span data-ttu-id="f3935-133">Mary</span><span class="sxs-lookup"><span data-stu-id="f3935-133">Mary</span></span><br /><br /> <span data-ttu-id="f3935-134">（来自 User2）</span><span class="sxs-lookup"><span data-stu-id="f3935-134">(from User2)</span></span>|<span data-ttu-id="f3935-135">Marketing</span><span class="sxs-lookup"><span data-stu-id="f3935-135">Marketing</span></span><br /><br /> <span data-ttu-id="f3935-136">（来自 User1）</span><span class="sxs-lookup"><span data-stu-id="f3935-136">(from User1)</span></span>|  
  
 <span data-ttu-id="f3935-137">下面的示例演示如何将数据库值与当前客户端成员值合并（除非此客户端也已经更改了该值）。</span><span class="sxs-lookup"><span data-stu-id="f3935-137">The following example shows how to merge database values with the current client member values (unless the client has also changed that value).</span></span> <span data-ttu-id="f3935-138">未对各个成员冲突进行检查或自定义处理。</span><span class="sxs-lookup"><span data-stu-id="f3935-138">No inspection or custom handling of individual member conflicts occurs.</span></span>  
  
 [!code-csharp[System.Data.Linq.RefreshMode#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.refreshmode/cs/program.cs#3)]
 [!code-vb[System.Data.Linq.RefreshMode#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.refreshmode/vb/module1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="f3935-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="f3935-139">See also</span></span>

- [<span data-ttu-id="f3935-140">如何：通过重写数据库值解决冲突</span><span class="sxs-lookup"><span data-stu-id="f3935-140">How to: Resolve Conflicts by Overwriting Database Values</span></span>](how-to-resolve-conflicts-by-overwriting-database-values.md)
- [<span data-ttu-id="f3935-141">如何：通过保留数据库值解决冲突</span><span class="sxs-lookup"><span data-stu-id="f3935-141">How to: Resolve Conflicts by Retaining Database Values</span></span>](how-to-resolve-conflicts-by-retaining-database-values.md)
- [<span data-ttu-id="f3935-142">如何：管理更改冲突</span><span class="sxs-lookup"><span data-stu-id="f3935-142">How to: Manage Change Conflicts</span></span>](how-to-manage-change-conflicts.md)
