---
description: 了解详细信息：乐观并发：概述
title: 乐观并发：概述
ms.date: 03/30/2017
ms.assetid: c2e38512-d0c8-4807-b30a-cb7e30338694
ms.openlocfilehash: fbf6714851dbb31982a110749c55e5fad7aa2206
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695419"
---
# <a name="optimistic-concurrency-overview"></a><span data-ttu-id="0aeb7-103">乐观并发：概述</span><span class="sxs-lookup"><span data-stu-id="0aeb7-103">Optimistic Concurrency: Overview</span></span>

[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="0aeb7-104">支持开放式并发控制。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-104">supports optimistic concurrency control.</span></span> <span data-ttu-id="0aeb7-105">下表描述了适用于文档中的开放式并发的术语 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] ：</span><span class="sxs-lookup"><span data-stu-id="0aeb7-105">The following table describes terms that apply to optimistic concurrency in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation:</span></span>  
  
|<span data-ttu-id="0aeb7-106">术语</span><span class="sxs-lookup"><span data-stu-id="0aeb7-106">Terms</span></span>|<span data-ttu-id="0aeb7-107">说明</span><span class="sxs-lookup"><span data-stu-id="0aeb7-107">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="0aeb7-108">concurrency</span><span class="sxs-lookup"><span data-stu-id="0aeb7-108">concurrency</span></span>|<span data-ttu-id="0aeb7-109">两个或更多用户同时尝试更新同一数据库行的情形。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-109">The situation in which two or more users at the same time try to update the same database row.</span></span>|  
|<span data-ttu-id="0aeb7-110">并发冲突 (concurrency conflict)</span><span class="sxs-lookup"><span data-stu-id="0aeb7-110">concurrency conflict</span></span>|<span data-ttu-id="0aeb7-111">两个或更多用户同时尝试向一行的一列或多列提交冲突值的情形。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-111">The situation in which two or more users at the same time try to submit conflicting values to one or more columns of a row.</span></span>|  
|<span data-ttu-id="0aeb7-112">并发控制</span><span class="sxs-lookup"><span data-stu-id="0aeb7-112">concurrency control</span></span>|<span data-ttu-id="0aeb7-113">用于解决并发冲突的技术。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-113">The technique used to resolve concurrency conflicts.</span></span>|  
|<span data-ttu-id="0aeb7-114">开放式并发控制</span><span class="sxs-lookup"><span data-stu-id="0aeb7-114">optimistic concurrency control</span></span>|<span data-ttu-id="0aeb7-115">先调查其他事务是否已更改了行中的值，再允许提交更改的技术。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-115">The technique that first investigates whether other transactions have changed values in a row before permitting changes to be submitted.</span></span><br /><br /> <span data-ttu-id="0aeb7-116">与 *悲观并发控制* 相反，它会锁定记录以避免并发冲突。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-116">Contrast with *pessimistic concurrency control*, which locks the record to avoid concurrency conflicts.</span></span><br /><br /> <span data-ttu-id="0aeb7-117">所谓 *乐观* 控制，因为它会将一个事务干扰另一个事务的几率视为不太可能。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-117">*Optimistic* control is so termed because it considers the chances of one transaction interfering with another to be unlikely.</span></span>|  
|<span data-ttu-id="0aeb7-118">冲突解决</span><span class="sxs-lookup"><span data-stu-id="0aeb7-118">conflict resolution</span></span>|<span data-ttu-id="0aeb7-119">通过重新查询数据库刷新出现冲突的项，然后协调差异的过程。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-119">The process of refreshing a conflicting item by querying the database again and then reconciling differences.</span></span><br /><br /> <span data-ttu-id="0aeb7-120">刷新对象时，[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 更改跟踪器会保留以下数据：</span><span class="sxs-lookup"><span data-stu-id="0aeb7-120">When an object is refreshed, the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] change tracker holds the following data:</span></span><br /><br /> <span data-ttu-id="0aeb7-121">-最初从数据库获取并用于更新检查的值。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-121">-   The values originally taken from the database and used for the update check.</span></span><br /><span data-ttu-id="0aeb7-122">-来自后续查询的新数据库值。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-122">-   The new database values from the subsequent query.</span></span><br /><br /> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="0aeb7-123">随后会确定相应对象是否发生冲突（即它的一个或多个成员值是否已发生更改）。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-123">then determines whether the object is in conflict (that is, whether one or more of its member values has changed).</span></span> <span data-ttu-id="0aeb7-124">如果此对象发生冲突，[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 下一步会确定它的哪些成员发生冲突。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-124">If the object is in conflict, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] next determines which of its members are in conflict.</span></span><br /><br /> <span data-ttu-id="0aeb7-125">[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 发现的任何成员冲突都会添加到冲突列表中。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-125">Any member conflict that [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] discovers is added to a conflict list.</span></span>|  
  
 <span data-ttu-id="0aeb7-126">在 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 对象模型中，当以下两个条件均为 true 时，将发生 *开放式并发冲突* ：</span><span class="sxs-lookup"><span data-stu-id="0aeb7-126">In the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] object model, an *optimistic concurrency conflict* occurs when both of the following conditions are true:</span></span>  
  
- <span data-ttu-id="0aeb7-127">客户端尝试向数据库提交更改。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-127">The client tries to submit changes to the database.</span></span>  
  
- <span data-ttu-id="0aeb7-128">数据库中的一个或多个更新检查值自客户端上次读取它们以来已得到更新。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-128">One or more update-check values have been updated in the database since the client last read them.</span></span>  
  
 <span data-ttu-id="0aeb7-129">此冲突的解决过程包括查明对象的哪些成员发生冲突，然后决定您希望如何进行处理。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-129">Resolution of this conflict includes discovering which members of the object are in conflict, and then deciding what you want to do about it.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0aeb7-130">只有映射为 <xref:System.Data.Linq.Mapping.UpdateCheck.Always> 或 <xref:System.Data.Linq.Mapping.UpdateCheck.WhenChanged> 的成员才会参与开放式并发检查。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-130">Only members mapped as <xref:System.Data.Linq.Mapping.UpdateCheck.Always> or <xref:System.Data.Linq.Mapping.UpdateCheck.WhenChanged> participate in optimistic concurrency checks.</span></span> <span data-ttu-id="0aeb7-131">对于标记为 <xref:System.Data.Linq.Mapping.UpdateCheck.Never> 的成员，不执行检查。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-131">No check is performed for members marked <xref:System.Data.Linq.Mapping.UpdateCheck.Never>.</span></span> <span data-ttu-id="0aeb7-132">有关详细信息，请参阅 <xref:System.Data.Linq.Mapping.UpdateCheck>。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-132">For more information, see <xref:System.Data.Linq.Mapping.UpdateCheck>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0aeb7-133">示例</span><span class="sxs-lookup"><span data-stu-id="0aeb7-133">Example</span></span>  

 <span data-ttu-id="0aeb7-134">例如，在下面的情况中，User1 通过查询数据库中的某一行开始准备更新。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-134">For example, in the following scenario, User1 starts to prepare an update by querying the database for a row.</span></span> <span data-ttu-id="0aeb7-135">User1 收到包含 Alfreds、Maria 和 Sales 值的一行。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-135">User1 receives a row with values of Alfreds, Maria, and Sales.</span></span>  
  
 <span data-ttu-id="0aeb7-136">User1 希望将 Manager 列的值更改为 Alfred，将 Department 列的值更改为 Marketing。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-136">User1 wants to change the value of the Manager column to Alfred and the value of the Department column to Marketing.</span></span> <span data-ttu-id="0aeb7-137">在 User2 将更改提交到数据库后，User1 才能提交这些更改。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-137">Before User1 can submit those changes, User2 has submitted changes to the database.</span></span> <span data-ttu-id="0aeb7-138">所以，现在 Assistant 列的值已更改为 Mary，Department 列的值已更改为 Service。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-138">So now the value of the Assistant column has been changed to Mary and the value of the Department column to Service.</span></span>  
  
 <span data-ttu-id="0aeb7-139">当 User1 现在尝试提交更改时，提交失败并且引发 <xref:System.Data.Linq.ChangeConflictException> 异常。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-139">When User1 now tries to submit changes, the submission fails and a <xref:System.Data.Linq.ChangeConflictException> exception is thrown.</span></span> <span data-ttu-id="0aeb7-140">出现这种结果是因为 Assistant 列和 Department 列的数据库值并不是他们所预期的那些值。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-140">This result occurs because the database values for the Assistant column and the Department column are not those that were expected.</span></span> <span data-ttu-id="0aeb7-141">表示 Assistant 和 Department 列的成员发生了冲突。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-141">Members representing the Assistant and Department columns are in conflict.</span></span> <span data-ttu-id="0aeb7-142">下表对这种情形作了总结。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-142">The following table summarizes the situation.</span></span>  
  
||<span data-ttu-id="0aeb7-143">Manager</span><span class="sxs-lookup"><span data-stu-id="0aeb7-143">Manager</span></span>|<span data-ttu-id="0aeb7-144">Assistant</span><span class="sxs-lookup"><span data-stu-id="0aeb7-144">Assistant</span></span>|<span data-ttu-id="0aeb7-145">部门</span><span class="sxs-lookup"><span data-stu-id="0aeb7-145">Department</span></span>|  
|------|-------------|---------------|----------------|  
|<span data-ttu-id="0aeb7-146">原始状态</span><span class="sxs-lookup"><span data-stu-id="0aeb7-146">Original state</span></span>|<span data-ttu-id="0aeb7-147">Alfreds</span><span class="sxs-lookup"><span data-stu-id="0aeb7-147">Alfreds</span></span>|<span data-ttu-id="0aeb7-148">Maria</span><span class="sxs-lookup"><span data-stu-id="0aeb7-148">Maria</span></span>|<span data-ttu-id="0aeb7-149">Sales</span><span class="sxs-lookup"><span data-stu-id="0aeb7-149">Sales</span></span>|  
|<span data-ttu-id="0aeb7-150">User1</span><span class="sxs-lookup"><span data-stu-id="0aeb7-150">User1</span></span>|<span data-ttu-id="0aeb7-151">Alfred</span><span class="sxs-lookup"><span data-stu-id="0aeb7-151">Alfred</span></span>||<span data-ttu-id="0aeb7-152">Marketing</span><span class="sxs-lookup"><span data-stu-id="0aeb7-152">Marketing</span></span>|  
|<span data-ttu-id="0aeb7-153">User2</span><span class="sxs-lookup"><span data-stu-id="0aeb7-153">User2</span></span>||<span data-ttu-id="0aeb7-154">Mary</span><span class="sxs-lookup"><span data-stu-id="0aeb7-154">Mary</span></span>|<span data-ttu-id="0aeb7-155">服务</span><span class="sxs-lookup"><span data-stu-id="0aeb7-155">Service</span></span>|  
  
 <span data-ttu-id="0aeb7-156">您可以用多种不同的方式来解决此类冲突。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-156">You can resolve conflicts such as this in different ways.</span></span> <span data-ttu-id="0aeb7-157">有关详细信息，请参阅 [如何：管理更改冲突](how-to-manage-change-conflicts.md)。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-157">For more information, see [How to: Manage Change Conflicts](how-to-manage-change-conflicts.md).</span></span>  
  
## <a name="conflict-detection-and-resolution-checklist"></a><span data-ttu-id="0aeb7-158">冲突检测和解决检查表</span><span class="sxs-lookup"><span data-stu-id="0aeb7-158">Conflict Detection and Resolution Checklist</span></span>  

 <span data-ttu-id="0aeb7-159">您可以检测和解决任意详细等级的冲突。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-159">You can detect and resolve conflicts at any level of detail.</span></span> <span data-ttu-id="0aeb7-160">一种极端情况是，您可以用三种方式之一（请参见 <xref:System.Data.Linq.RefreshMode>）来解决所有冲突，而不再作其他方面的考虑。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-160">At one extreme, you can resolve all conflicts in one of three ways (see <xref:System.Data.Linq.RefreshMode>) without additional consideration.</span></span> <span data-ttu-id="0aeb7-161">另一种极端情况是，您可以为发生冲突的每个成员上的每种冲突指定特定操作。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-161">At the other extreme, you can designate a specific action for each type of conflict on every member in conflict.</span></span>  
  
- <span data-ttu-id="0aeb7-162">在您的对象模型中指定或修改 <xref:System.Data.Linq.Mapping.UpdateCheck> 选项。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-162">Specify or revise <xref:System.Data.Linq.Mapping.UpdateCheck> options in your object model.</span></span>  
  
     <span data-ttu-id="0aeb7-163">有关详细信息，请参阅 [如何：指定针对并发冲突对哪些成员进行测试](how-to-specify-which-members-are-tested-for-concurrency-conflicts.md)。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-163">For more information, see [How to: Specify Which Members are Tested for Concurrency Conflicts](how-to-specify-which-members-are-tested-for-concurrency-conflicts.md).</span></span>  
  
- <span data-ttu-id="0aeb7-164">在对 <xref:System.Data.Linq.DataContext.SubmitChanges%2A> 的调用的 try/catch 块中，指定您希望在哪个点引发异常。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-164">In the try/catch block of your call to <xref:System.Data.Linq.DataContext.SubmitChanges%2A>, specify at what point you want exceptions to be thrown.</span></span>  
  
     <span data-ttu-id="0aeb7-165">有关详细信息，请参阅 [如何：指定何时引发并发异常](how-to-specify-when-concurrency-exceptions-are-thrown.md)。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-165">For more information, see [How to: Specify When Concurrency Exceptions are Thrown](how-to-specify-when-concurrency-exceptions-are-thrown.md).</span></span>  
  
- <span data-ttu-id="0aeb7-166">决定你希望检索的冲突详细信息量，并在 try/catch 块中包括相应的代码。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-166">Determine how much conflict detail you want to retrieve, and include code in your try/catch block accordingly.</span></span>  
  
     <span data-ttu-id="0aeb7-167">有关详细信息，请参阅 [如何：检索实体冲突信息](how-to-retrieve-entity-conflict-information.md) 和 [如何：检索成员冲突信息](how-to-retrieve-member-conflict-information.md)。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-167">For more information, see [How to: Retrieve Entity Conflict Information](how-to-retrieve-entity-conflict-information.md) and [How to: Retrieve Member Conflict Information](how-to-retrieve-member-conflict-information.md).</span></span>  
  
- <span data-ttu-id="0aeb7-168">在代码中包含 `try` / `catch` 要如何解决你发现的各种冲突。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-168">Include in your `try`/`catch` code how you want to resolve the various conflicts you discover.</span></span>  
  
     <span data-ttu-id="0aeb7-169">有关详细信息，请参阅 [如何：通过保留数据库值解决冲突](how-to-resolve-conflicts-by-retaining-database-values.md)、 [如何：通过覆盖数据库值解决冲突](how-to-resolve-conflicts-by-overwriting-database-values.md)和 [如何：通过与数据库值合并解决冲突](how-to-resolve-conflicts-by-merging-with-database-values.md)。</span><span class="sxs-lookup"><span data-stu-id="0aeb7-169">For more information, see [How to: Resolve Conflicts by Retaining Database Values](how-to-resolve-conflicts-by-retaining-database-values.md), [How to: Resolve Conflicts by Overwriting Database Values](how-to-resolve-conflicts-by-overwriting-database-values.md), and [How to: Resolve Conflicts by Merging with Database Values](how-to-resolve-conflicts-by-merging-with-database-values.md).</span></span>  
  
## <a name="linq-to-sql-types-that-support-conflict-discovery-and-resolution"></a><span data-ttu-id="0aeb7-170">支持冲突发现和解决的 LINQ to SQL 类型</span><span class="sxs-lookup"><span data-stu-id="0aeb7-170">LINQ to SQL Types That Support Conflict Discovery and Resolution</span></span>  

 <span data-ttu-id="0aeb7-171">[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中支持解决开放式并发冲突的类和功能包括：</span><span class="sxs-lookup"><span data-stu-id="0aeb7-171">Classes and features to support the resolution of conflicts in optimistic concurrency in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] include the following:</span></span>  
  
- <xref:System.Data.Linq.ObjectChangeConflict?displayProperty=nameWithType>  
  
- <xref:System.Data.Linq.MemberChangeConflict?displayProperty=nameWithType>  
  
- <xref:System.Data.Linq.ChangeConflictCollection?displayProperty=nameWithType>  
  
- <xref:System.Data.Linq.ChangeConflictException?displayProperty=nameWithType>  
  
- <xref:System.Data.Linq.DataContext.ChangeConflicts%2A?displayProperty=nameWithType>  
  
- <xref:System.Data.Linq.DataContext.SubmitChanges%2A?displayProperty=nameWithType>  
  
- <xref:System.Data.Linq.DataContext.Refresh%2A?displayProperty=nameWithType>  
  
- <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A?displayProperty=nameWithType>  
  
- <xref:System.Data.Linq.Mapping.UpdateCheck?displayProperty=nameWithType>  
  
- <xref:System.Data.Linq.RefreshMode?displayProperty=nameWithType>  
  
## <a name="see-also"></a><span data-ttu-id="0aeb7-172">请参阅</span><span class="sxs-lookup"><span data-stu-id="0aeb7-172">See also</span></span>

- [<span data-ttu-id="0aeb7-173">如何：管理更改冲突</span><span class="sxs-lookup"><span data-stu-id="0aeb7-173">How to: Manage Change Conflicts</span></span>](how-to-manage-change-conflicts.md)
