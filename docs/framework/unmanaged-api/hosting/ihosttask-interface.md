---
description: 了解详细信息： IHostTask 接口
title: IHostTask 接口
ms.date: 03/30/2017
api_name:
- IHostTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask
helpviewer_keywords:
- IHostTask interface [.NET Framework hosting]
ms.assetid: a71dbbd5-64b8-47eb-9f03-8e8c85fbe2bc
topic_type:
- apiref
ms.openlocfilehash: c46bbdd2e881c20d1ffd634bec8ddfa3b70b0f82
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784660"
---
# <a name="ihosttask-interface"></a><span data-ttu-id="5ebb9-103">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="5ebb9-103">IHostTask Interface</span></span>

<span data-ttu-id="5ebb9-104">提供允许公共语言运行时 (CLR) 与宿主通信以管理任务的方法。</span><span class="sxs-lookup"><span data-stu-id="5ebb9-104">Provides methods that allow the common language runtime (CLR) to communicate with the host to manage tasks.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5ebb9-105">方法</span><span class="sxs-lookup"><span data-stu-id="5ebb9-105">Methods</span></span>  
  
|<span data-ttu-id="5ebb9-106">方法</span><span class="sxs-lookup"><span data-stu-id="5ebb9-106">Method</span></span>|<span data-ttu-id="5ebb9-107">说明</span><span class="sxs-lookup"><span data-stu-id="5ebb9-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5ebb9-108">Alert 方法</span><span class="sxs-lookup"><span data-stu-id="5ebb9-108">Alert Method</span></span>](ihosttask-alert-method.md)|<span data-ttu-id="5ebb9-109">请求宿主唤醒当前实例表示的任务 `IHostTask` ，以便可以中止任务。</span><span class="sxs-lookup"><span data-stu-id="5ebb9-109">Requests that the host wake the task represented by the current `IHostTask` instance, so the task can be aborted.</span></span>|  
|[<span data-ttu-id="5ebb9-110">GetPriority 方法</span><span class="sxs-lookup"><span data-stu-id="5ebb9-110">GetPriority Method</span></span>](ihosttask-getpriority-method.md)|<span data-ttu-id="5ebb9-111">获取当前实例表示的任务的线程优先级别 `IHostTask` 。</span><span class="sxs-lookup"><span data-stu-id="5ebb9-111">Gets the thread priority level of the task represented by the current `IHostTask` instance.</span></span>|  
|[<span data-ttu-id="5ebb9-112">Join 方法</span><span class="sxs-lookup"><span data-stu-id="5ebb9-112">Join Method</span></span>](ihosttask-join-method.md)|<span data-ttu-id="5ebb9-113">阻止调用任务，直到当前实例表示的任务 `IHostTask` 完成、指定的时间间隔结束或调用 [IHostTask：： Alert](ihosttask-alert-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="5ebb9-113">Blocks the calling task until the task represented by the current `IHostTask` instance completes, the specified time interval elapses, or [IHostTask::Alert](ihosttask-alert-method.md) is called.</span></span>|  
|[<span data-ttu-id="5ebb9-114">SetCLRTask 方法</span><span class="sxs-lookup"><span data-stu-id="5ebb9-114">SetCLRTask Method</span></span>](ihosttask-setclrtask-method.md)|<span data-ttu-id="5ebb9-115">将 [ICLRTask 接口](iclrtask-interface.md) 实例与当前实例相关联 `IHostTask` 。</span><span class="sxs-lookup"><span data-stu-id="5ebb9-115">Associates an [ICLRTask Interface](iclrtask-interface.md) instance with the current `IHostTask` instance.</span></span>|  
|[<span data-ttu-id="5ebb9-116">SetPriority 方法</span><span class="sxs-lookup"><span data-stu-id="5ebb9-116">SetPriority Method</span></span>](ihosttask-setpriority-method.md)|<span data-ttu-id="5ebb9-117">请求宿主调整当前实例所表示的任务的线程优先级别 `IHostTask` 。</span><span class="sxs-lookup"><span data-stu-id="5ebb9-117">Requests that the host adjust the thread priority level for the task represented by the current `IHostTask` instance.</span></span>|  
|[<span data-ttu-id="5ebb9-118">Start 方法</span><span class="sxs-lookup"><span data-stu-id="5ebb9-118">Start Method</span></span>](ihosttask-start-method.md)|<span data-ttu-id="5ebb9-119">请求宿主将当前实例表示的任务 `IHostTask` 从挂起状态移动到实时状态，在此状态下可以执行代码。</span><span class="sxs-lookup"><span data-stu-id="5ebb9-119">Requests that the host move the task represented by the current `IHostTask` instance from a suspended state to a live state, in which code can be executed.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5ebb9-120">备注</span><span class="sxs-lookup"><span data-stu-id="5ebb9-120">Remarks</span></span>  

 <span data-ttu-id="5ebb9-121">CLR 调用定义的方法 `IHostTask` 来启动任务、设置其线程优先级别，等等。</span><span class="sxs-lookup"><span data-stu-id="5ebb9-121">The CLR calls methods defined by `IHostTask` to start a task, set its thread priority level, and so on.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5ebb9-122">要求</span><span class="sxs-lookup"><span data-stu-id="5ebb9-122">Requirements</span></span>  

 <span data-ttu-id="5ebb9-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5ebb9-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5ebb9-124">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5ebb9-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5ebb9-125">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5ebb9-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5ebb9-126">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5ebb9-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ebb9-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="5ebb9-127">See also</span></span>

- [<span data-ttu-id="5ebb9-128">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="5ebb9-128">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="5ebb9-129">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="5ebb9-129">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="5ebb9-130">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="5ebb9-130">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="5ebb9-131">承载接口</span><span class="sxs-lookup"><span data-stu-id="5ebb9-131">Hosting Interfaces</span></span>](hosting-interfaces.md)
