---
description: 了解详细信息： ICLRTask：： SwitchIn 方法
title: ICLRTask::SwitchIn 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.SwitchIn
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::SwitchIn
helpviewer_keywords:
- ICLRTask::SwitchIn method [.NET Framework hosting]
- SwitchIn method [.NET Framework hosting]
ms.assetid: 3d37ce20-aa65-4043-8f13-7c728b5d8a52
topic_type:
- apiref
ms.openlocfilehash: 0bbcd2b9594a8ce465a1dcd7b5ae3f8a0799826d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636814"
---
# <a name="iclrtaskswitchin-method"></a><span data-ttu-id="fa37e-103">ICLRTask::SwitchIn 方法</span><span class="sxs-lookup"><span data-stu-id="fa37e-103">ICLRTask::SwitchIn Method</span></span>

<span data-ttu-id="fa37e-104">通知公共语言运行时 (CLR) 当前 [ICLRTask](iclrtask-interface.md) 实例表示的任务现在处于可运行状态。</span><span class="sxs-lookup"><span data-stu-id="fa37e-104">Notifies the common language runtime (CLR) that the task that the current [ICLRTask](iclrtask-interface.md) instance represents is now in an operable state.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa37e-105">语法</span><span class="sxs-lookup"><span data-stu-id="fa37e-105">Syntax</span></span>  
  
```cpp  
HRESULT SwitchIn (  
    [in] HANDLE threadHandle  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fa37e-106">参数</span><span class="sxs-lookup"><span data-stu-id="fa37e-106">Parameters</span></span>  

 `threadHandle`  
 <span data-ttu-id="fa37e-107">中当前实例所表示的任务正在执行的物理线程的句柄 `ICLRTask` 。</span><span class="sxs-lookup"><span data-stu-id="fa37e-107">[in] A handle to the physical thread on which the task represented by the current `ICLRTask` instance is executing.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fa37e-108">返回值</span><span class="sxs-lookup"><span data-stu-id="fa37e-108">Return Value</span></span>  
  
|<span data-ttu-id="fa37e-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fa37e-109">HRESULT</span></span>|<span data-ttu-id="fa37e-110">说明</span><span class="sxs-lookup"><span data-stu-id="fa37e-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fa37e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa37e-111">S_OK</span></span>|<span data-ttu-id="fa37e-112">`SwitchIn` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="fa37e-112">`SwitchIn` returned successfully.</span></span>|  
|<span data-ttu-id="fa37e-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="fa37e-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="fa37e-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="fa37e-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="fa37e-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="fa37e-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="fa37e-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="fa37e-116">The call timed out.</span></span>|  
|<span data-ttu-id="fa37e-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="fa37e-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="fa37e-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="fa37e-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="fa37e-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="fa37e-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="fa37e-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="fa37e-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="fa37e-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="fa37e-121">E_FAIL</span></span>|<span data-ttu-id="fa37e-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="fa37e-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="fa37e-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="fa37e-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="fa37e-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="fa37e-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="fa37e-125">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="fa37e-125">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="fa37e-126">`SwitchIn` 调用 [SwitchOut 方法](iclrtask-switchout-method.md)之前调用了。</span><span class="sxs-lookup"><span data-stu-id="fa37e-126">`SwitchIn` was called without an earlier call to [SwitchOut Method](iclrtask-switchout-method.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fa37e-127">备注</span><span class="sxs-lookup"><span data-stu-id="fa37e-127">Remarks</span></span>  

 <span data-ttu-id="fa37e-128">`threadHandle`参数表示操作系统线程的句柄，该句柄由当前实例表示的任务已 `ICLRTask` 计划。</span><span class="sxs-lookup"><span data-stu-id="fa37e-128">The `threadHandle` parameter represents a handle to the operating system thread on which the task represented by the current `ICLRTask` instance has been scheduled.</span></span> <span data-ttu-id="fa37e-129">如果此线程上发生模拟，则必须先调用 [IHostSecurityManager：： RevertToSelf](ihostsecuritymanager-reverttoself-method.md) ，然后才能在该任务中切换。</span><span class="sxs-lookup"><span data-stu-id="fa37e-129">If impersonation has occurred on this thread, you must call [IHostSecurityManager::RevertToSelf](ihostsecuritymanager-reverttoself-method.md) before switching in the task.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="fa37e-130">对不使用之前调用的的调用将 `SwitchIn` `SwitchOut` 失败，HRESULT 值为 HOST_E_INVALIDOPERATION。</span><span class="sxs-lookup"><span data-stu-id="fa37e-130">A call to `SwitchIn` without an earlier call to `SwitchOut` fails with an HRESULT value of HOST_E_INVALIDOPERATION.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fa37e-131">要求</span><span class="sxs-lookup"><span data-stu-id="fa37e-131">Requirements</span></span>  

 <span data-ttu-id="fa37e-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fa37e-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa37e-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="fa37e-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fa37e-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fa37e-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fa37e-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa37e-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa37e-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="fa37e-136">See also</span></span>

- [<span data-ttu-id="fa37e-137">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="fa37e-137">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="fa37e-138">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="fa37e-138">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="fa37e-139">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="fa37e-139">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="fa37e-140">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="fa37e-140">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
