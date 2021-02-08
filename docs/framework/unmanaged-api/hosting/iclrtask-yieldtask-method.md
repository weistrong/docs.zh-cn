---
description: 了解详细信息： ICLRTask：： YieldTask 方法
title: ICLRTask::YieldTask 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.YieldTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::YieldTask
helpviewer_keywords:
- ICLRTask::YieldTask method [.NET Framework hosting]
- YieldTask method [.NET Framework hosting]
ms.assetid: b8eb4095-3a8f-4be3-9446-63e9893dce7d
topic_type:
- apiref
ms.openlocfilehash: b72b31b0a1c10a2b0b1e2ad379b140ff33419fa1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784920"
---
# <a name="iclrtaskyieldtask-method"></a><span data-ttu-id="3ed17-103">ICLRTask::YieldTask 方法</span><span class="sxs-lookup"><span data-stu-id="3ed17-103">ICLRTask::YieldTask Method</span></span>

<span data-ttu-id="3ed17-104">请求公共语言运行时 (CLR) 放置当前 [ICLRTask](iclrtask-interface.md) 实例表示的任务，并使处理器时间可供其他任务使用。</span><span class="sxs-lookup"><span data-stu-id="3ed17-104">Requests that the common language runtime (CLR) put aside the task that the current [ICLRTask](iclrtask-interface.md) instance represents, and make the processor time available to other tasks.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3ed17-105">语法</span><span class="sxs-lookup"><span data-stu-id="3ed17-105">Syntax</span></span>  
  
```cpp  
HRESULT YieldTask ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="3ed17-106">返回值</span><span class="sxs-lookup"><span data-stu-id="3ed17-106">Return Value</span></span>  
  
|<span data-ttu-id="3ed17-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3ed17-107">HRESULT</span></span>|<span data-ttu-id="3ed17-108">说明</span><span class="sxs-lookup"><span data-stu-id="3ed17-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3ed17-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ed17-109">S_OK</span></span>|<span data-ttu-id="3ed17-110">`YieldTask` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="3ed17-110">`YieldTask` returned successfully.</span></span>|  
|<span data-ttu-id="3ed17-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3ed17-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="3ed17-112">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="3ed17-112">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="3ed17-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3ed17-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="3ed17-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="3ed17-114">The call timed out.</span></span>|  
|<span data-ttu-id="3ed17-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="3ed17-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="3ed17-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="3ed17-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="3ed17-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="3ed17-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="3ed17-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="3ed17-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="3ed17-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="3ed17-119">E_FAIL</span></span>|<span data-ttu-id="3ed17-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="3ed17-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="3ed17-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="3ed17-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="3ed17-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="3ed17-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3ed17-123">备注</span><span class="sxs-lookup"><span data-stu-id="3ed17-123">Remarks</span></span>  

 <span data-ttu-id="3ed17-124">主机调用 `YieldTask` 来请求其他任务或进程的处理器资源。</span><span class="sxs-lookup"><span data-stu-id="3ed17-124">A host calls `YieldTask` to request processor resources for other tasks or processes.</span></span> <span data-ttu-id="3ed17-125">此方法主要用于允许长时间运行的代码放弃 CPU 时间。</span><span class="sxs-lookup"><span data-stu-id="3ed17-125">This method is primarily intended to allow long-running code to give up CPU time.</span></span> <span data-ttu-id="3ed17-126">运行时尝试将当前实例表示的任务置于 `ICLRTask` 可产生处理时间的状态，但不保证成功。</span><span class="sxs-lookup"><span data-stu-id="3ed17-126">The runtime attempts to put the task that the current `ICLRTask` instance represents in a state where it can yield processing time, but makes no guarantee of success.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3ed17-127">要求</span><span class="sxs-lookup"><span data-stu-id="3ed17-127">Requirements</span></span>  

 <span data-ttu-id="3ed17-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3ed17-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3ed17-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="3ed17-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3ed17-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3ed17-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3ed17-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3ed17-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ed17-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="3ed17-132">See also</span></span>

- [<span data-ttu-id="3ed17-133">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="3ed17-133">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="3ed17-134">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="3ed17-134">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="3ed17-135">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="3ed17-135">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="3ed17-136">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="3ed17-136">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
