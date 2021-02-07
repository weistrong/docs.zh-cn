---
description: 了解详细信息： ICLRTask2 接口
title: ICLRTask2 接口
ms.date: 03/30/2017
api_name:
- ICLRTask2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask2
helpviewer_keywords:
- ICLRTask2 interface [.NET Framework hosting]
ms.assetid: b5a22ebc-0582-49de-91f9-97a3d9789290
topic_type:
- apiref
ms.openlocfilehash: 835b01e1c808c071e9393c5117d5e38415ec8eba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728623"
---
# <a name="iclrtask2-interface"></a><span data-ttu-id="47d9a-103">ICLRTask2 接口</span><span class="sxs-lookup"><span data-stu-id="47d9a-103">ICLRTask2 Interface</span></span>

<span data-ttu-id="47d9a-104">提供 [ICLRTask](iclrtask-interface.md) 接口的所有功能;此外，还提供了允许线程中止在当前线程上延迟的方法。</span><span class="sxs-lookup"><span data-stu-id="47d9a-104">Provides all the functionality of the [ICLRTask](iclrtask-interface.md) interface; in addition, provides methods that allow thread aborts to be delayed on the current thread.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="47d9a-105">方法</span><span class="sxs-lookup"><span data-stu-id="47d9a-105">Methods</span></span>  
  
|<span data-ttu-id="47d9a-106">方法</span><span class="sxs-lookup"><span data-stu-id="47d9a-106">Method</span></span>|<span data-ttu-id="47d9a-107">说明</span><span class="sxs-lookup"><span data-stu-id="47d9a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="47d9a-108">BeginPreventAsyncAbort 方法</span><span class="sxs-lookup"><span data-stu-id="47d9a-108">BeginPreventAsyncAbort Method</span></span>](iclrtask2-beginpreventasyncabort-method.md)|<span data-ttu-id="47d9a-109">延迟当前线程上的新线程中止请求。</span><span class="sxs-lookup"><span data-stu-id="47d9a-109">Delays new thread abort requests on the current thread.</span></span>|  
|[<span data-ttu-id="47d9a-110">EndPreventAsyncAbort 方法</span><span class="sxs-lookup"><span data-stu-id="47d9a-110">EndPreventAsyncAbort Method</span></span>](iclrtask2-endpreventasyncabort-method.md)|<span data-ttu-id="47d9a-111">允许新的或挂起的线程中止请求导致在当前线程上中止线程。</span><span class="sxs-lookup"><span data-stu-id="47d9a-111">Allows new or pending thread abort requests to result in thread aborts on the current thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="47d9a-112">备注</span><span class="sxs-lookup"><span data-stu-id="47d9a-112">Remarks</span></span>  

 <span data-ttu-id="47d9a-113">`ICLRTask2`接口继承 `ICLRTask` 接口并添加允许主机延迟线程中止的方法，以保护不能失败的代码区域。</span><span class="sxs-lookup"><span data-stu-id="47d9a-113">The `ICLRTask2` interface inherits the `ICLRTask` interface and adds methods that allow the host to delay thread aborts, to protect a region of code that must not fail.</span></span> <span data-ttu-id="47d9a-114">调用 `BeginPreventAsyncAbort` 会递增当前线程的延迟线程中止计数器，并调用 `EndPreventAsyncAbort` 减量。</span><span class="sxs-lookup"><span data-stu-id="47d9a-114">Calling `BeginPreventAsyncAbort` increments the delay-thread-abort counter for the current thread, and calling `EndPreventAsyncAbort` decrements it.</span></span> <span data-ttu-id="47d9a-115">对和的调用 `BeginPreventAsyncAbort` `EndPreventAsyncAbort` 可以嵌套。</span><span class="sxs-lookup"><span data-stu-id="47d9a-115">Calls to `BeginPreventAsyncAbort` and `EndPreventAsyncAbort` can be nested.</span></span> <span data-ttu-id="47d9a-116">只要计数器大于零，就会延迟当前线程的线程中止。</span><span class="sxs-lookup"><span data-stu-id="47d9a-116">As long as the counter is greater than zero, thread aborts for the current thread are delayed.</span></span>  
  
 <span data-ttu-id="47d9a-117">如果对 `BeginPreventAsyncAbort` 和 `EndPreventAsyncAbort` 的调用不成对，则可能会达到无法将线程中止传递到当前线程的状态。</span><span class="sxs-lookup"><span data-stu-id="47d9a-117">If calls to `BeginPreventAsyncAbort` and `EndPreventAsyncAbort` are not paired, it is possible to reach a state in which thread aborts cannot be delivered to the current thread.</span></span>  
  
 <span data-ttu-id="47d9a-118">此延迟不适用于自行中止的线程。</span><span class="sxs-lookup"><span data-stu-id="47d9a-118">The delay is not honored for a thread that aborts itself.</span></span>  
  
 <span data-ttu-id="47d9a-119">此功能公开的功能由虚拟机在内部使用 (VM) 。</span><span class="sxs-lookup"><span data-stu-id="47d9a-119">The functionality that is exposed by this feature is used internally by the virtual machine (VM).</span></span> <span data-ttu-id="47d9a-120">滥用这些方法可能会导致 VM 中未指定的行为。</span><span class="sxs-lookup"><span data-stu-id="47d9a-120">Misuse of these methods may cause unspecified behavior in the VM.</span></span> <span data-ttu-id="47d9a-121">例如， `EndPreventAsyncAbort` 如果未通过第一次调用调用，则在 `BeginPreventAsyncAbort` VM 之前将计数器设置为零。</span><span class="sxs-lookup"><span data-stu-id="47d9a-121">For example, calling `EndPreventAsyncAbort` without first calling `BeginPreventAsyncAbort` could set the counter to zero when the VM has previously incremented it.</span></span> <span data-ttu-id="47d9a-122">同样，不检查内部计数器是否溢出。</span><span class="sxs-lookup"><span data-stu-id="47d9a-122">Similarly, the internal counter is not checked for overflow.</span></span> <span data-ttu-id="47d9a-123">如果它超过其整数限制，原因是主机和 VM 均递增，则未指定产生的行为。</span><span class="sxs-lookup"><span data-stu-id="47d9a-123">If it exceeds its integral limit because it is incremented by both the host and the VM, the resulting behavior is unspecified.</span></span>  
  
 <span data-ttu-id="47d9a-124">有关从和继承此接口的其他用法的成员的信息 `ICLRTask` ，请参阅 [ICLRTask](iclrtask-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="47d9a-124">For information about members inherited from `ICLRTask` and about the other uses of this interface, see the [ICLRTask](iclrtask-interface.md) interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="47d9a-125">要求</span><span class="sxs-lookup"><span data-stu-id="47d9a-125">Requirements</span></span>  

 <span data-ttu-id="47d9a-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="47d9a-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="47d9a-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="47d9a-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="47d9a-128">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="47d9a-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="47d9a-129">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="47d9a-129">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47d9a-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="47d9a-130">See also</span></span>

- [<span data-ttu-id="47d9a-131">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="47d9a-131">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="47d9a-132">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="47d9a-132">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="47d9a-133">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="47d9a-133">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="47d9a-134">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="47d9a-134">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="47d9a-135">承载接口</span><span class="sxs-lookup"><span data-stu-id="47d9a-135">Hosting Interfaces</span></span>](hosting-interfaces.md)
