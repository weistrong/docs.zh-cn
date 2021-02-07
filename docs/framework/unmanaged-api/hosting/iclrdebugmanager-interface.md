---
description: 了解详细信息： ICLRDebugManager 接口
title: ICLRDebugManager 接口
ms.date: 03/30/2017
api_name:
- ICLRDebugManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDebugManager
helpviewer_keywords:
- ICLRDebugManager interface [.NET Framework hosting]
ms.assetid: e835062c-c7d6-4945-8a44-2de7ebf3928e
topic_type:
- apiref
ms.openlocfilehash: 4306e38b7c868561276d5b00e7730b6fcee46fd7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746004"
---
# <a name="iclrdebugmanager-interface"></a><span data-ttu-id="d1419-103">ICLRDebugManager 接口</span><span class="sxs-lookup"><span data-stu-id="d1419-103">ICLRDebugManager Interface</span></span>

<span data-ttu-id="d1419-104">提供允许主机将一组任务与标识符和友好名称关联的方法。</span><span class="sxs-lookup"><span data-stu-id="d1419-104">Provides methods that allow a host to associate a set of tasks with an identifier and a friendly name.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d1419-105">方法</span><span class="sxs-lookup"><span data-stu-id="d1419-105">Methods</span></span>  
  
|<span data-ttu-id="d1419-106">方法</span><span class="sxs-lookup"><span data-stu-id="d1419-106">Method</span></span>|<span data-ttu-id="d1419-107">说明</span><span class="sxs-lookup"><span data-stu-id="d1419-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d1419-108">BeginConnection 方法</span><span class="sxs-lookup"><span data-stu-id="d1419-108">BeginConnection Method</span></span>](iclrdebugmanager-beginconnection-method.md)|<span data-ttu-id="d1419-109">在宿主和调试器之间建立新的连接，以将任务与标识符和友好名称关联起来。</span><span class="sxs-lookup"><span data-stu-id="d1419-109">Establishes a new connection between the host and the debugger to associate tasks with an identifier and a friendly name.</span></span>|  
|[<span data-ttu-id="d1419-110">EndConnection 方法</span><span class="sxs-lookup"><span data-stu-id="d1419-110">EndConnection Method</span></span>](iclrdebugmanager-endconnection-method.md)|<span data-ttu-id="d1419-111">删除任务列表与标识符和友好名称之间的关联。</span><span class="sxs-lookup"><span data-stu-id="d1419-111">Removes the association between a list of tasks and an identifier and a friendly name.</span></span>|  
|[<span data-ttu-id="d1419-112">GetDacl 方法</span><span class="sxs-lookup"><span data-stu-id="d1419-112">GetDacl Method</span></span>](iclrdebugmanager-getdacl-method.md)|<span data-ttu-id="d1419-113">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="d1419-113">This method is not implemented.</span></span>|  
|[<span data-ttu-id="d1419-114">IsDebuggerAttached 方法</span><span class="sxs-lookup"><span data-stu-id="d1419-114">IsDebuggerAttached Method</span></span>](iclrdebugmanager-isdebuggerattached-method.md)|<span data-ttu-id="d1419-115">获取一个值，它指示调试器是否已附加到进程。</span><span class="sxs-lookup"><span data-stu-id="d1419-115">Gets a value that indicates whether a debugger is attached to the process.</span></span>|  
|[<span data-ttu-id="d1419-116">SetConnectionTasks 方法</span><span class="sxs-lookup"><span data-stu-id="d1419-116">SetConnectionTasks Method</span></span>](iclrdebugmanager-setconnectiontasks-method.md)|<span data-ttu-id="d1419-117">将 [ICLRTask](iclrtask-interface.md) 实例列表与标识符和友好名称关联。</span><span class="sxs-lookup"><span data-stu-id="d1419-117">Associates a list of [ICLRTask](iclrtask-interface.md) instances with an identifier and a friendly name.</span></span>|  
|[<span data-ttu-id="d1419-118">SetDacl 方法</span><span class="sxs-lookup"><span data-stu-id="d1419-118">SetDacl Method</span></span>](iclrdebugmanager-setdacl-method.md)|<span data-ttu-id="d1419-119">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="d1419-119">This method is not implemented.</span></span>|  
|[<span data-ttu-id="d1419-120">SetSymbolReadingPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="d1419-120">SetSymbolReadingPolicy Method</span></span>](iclrdebugmanager-setsymbolreadingpolicy-method.md)|<span data-ttu-id="d1419-121">设置用于读取程序数据库 (PDB) 文件的策略。</span><span class="sxs-lookup"><span data-stu-id="d1419-121">Sets the policy for reading program database (PDB) files.</span></span> <span data-ttu-id="d1419-122">策略确定有关行号和文件的信息是否包含在调用堆栈中。</span><span class="sxs-lookup"><span data-stu-id="d1419-122">The policy determines whether information about line numbers and files is included in call stacks.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d1419-123">备注</span><span class="sxs-lookup"><span data-stu-id="d1419-123">Remarks</span></span>  

 <span data-ttu-id="d1419-124">在调试方案中，主机可能需要根据任务自己的编程逻辑对任务进行分组。</span><span class="sxs-lookup"><span data-stu-id="d1419-124">In debugging scenarios, a host might want to group tasks according to its own programming logic.</span></span> <span data-ttu-id="d1419-125">例如，分组允许开发人员仅查看开发人员的 Api 所需的任务，而不是查看在进程中运行的每个任务。</span><span class="sxs-lookup"><span data-stu-id="d1419-125">For example, a grouping would allow a developer to see only the tasks required by the developer's APIs, instead of seeing every task running in the process.</span></span> <span data-ttu-id="d1419-126">`ICLRDebugManager` 允许宿主实现这种分组。</span><span class="sxs-lookup"><span data-stu-id="d1419-126">`ICLRDebugManager` allows the host to implement this kind of grouping.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="d1419-127">三个 `ICLRDebugManager` 方法（和）相互 `BeginConnection` `SetConnectionTasks` `EndConnection` 依赖。</span><span class="sxs-lookup"><span data-stu-id="d1419-127">Three `ICLRDebugManager` methods, `BeginConnection`, `SetConnectionTasks` and `EndConnection`, are dependent upon each other.</span></span> <span data-ttu-id="d1419-128">必须按给定顺序调用它们才能按预期方式工作。</span><span class="sxs-lookup"><span data-stu-id="d1419-128">They must be called in the given order to work as expected.</span></span>  
  
 <span data-ttu-id="d1419-129">分组以及宿主分配给分组的标识符和友好名称对于公共语言运行时 (CLR) 没有任何意义。</span><span class="sxs-lookup"><span data-stu-id="d1419-129">The grouping, and the identifiers and friendly names that the host assigns to the grouping, have no meaning for the common language runtime (CLR).</span></span> <span data-ttu-id="d1419-130">CLR 只会将信息传递到调试器。</span><span class="sxs-lookup"><span data-stu-id="d1419-130">The CLR merely passes the information along to the debugger.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d1419-131">要求</span><span class="sxs-lookup"><span data-stu-id="d1419-131">Requirements</span></span>  

 <span data-ttu-id="d1419-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d1419-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d1419-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d1419-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d1419-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d1419-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d1419-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d1419-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1419-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="d1419-136">See also</span></span>

- [<span data-ttu-id="d1419-137">承载接口</span><span class="sxs-lookup"><span data-stu-id="d1419-137">Hosting Interfaces</span></span>](hosting-interfaces.md)
