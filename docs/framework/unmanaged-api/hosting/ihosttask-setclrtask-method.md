---
description: 了解详细信息： IHostTask：： SetCLRTask 方法
title: IHostTask::SetCLRTask 方法
ms.date: 03/30/2017
api_name:
- IHostTask.SetCLRTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::SetCLRTask
helpviewer_keywords:
- SetCLRTask method [.NET Framework hosting]
- IHostTask::SetCLRTask method [.NET Framework hosting]
ms.assetid: e9d39c80-41a1-49e7-bb5e-ea3433bfb5d7
topic_type:
- apiref
ms.openlocfilehash: 381b7827f043b6ef1d4a6698f5eb103233c9af55
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784673"
---
# <a name="ihosttasksetclrtask-method"></a><span data-ttu-id="cb438-103">IHostTask::SetCLRTask 方法</span><span class="sxs-lookup"><span data-stu-id="cb438-103">IHostTask::SetCLRTask Method</span></span>

<span data-ttu-id="cb438-104">将 `ICLRTask` 实例与当前 [IHostTask](ihosttask-interface.md) 实例相关联。</span><span class="sxs-lookup"><span data-stu-id="cb438-104">Associates an `ICLRTask` instance with the current [IHostTask](ihosttask-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cb438-105">语法</span><span class="sxs-lookup"><span data-stu-id="cb438-105">Syntax</span></span>  
  
```cpp  
HRESULT SetCLRTask (  
    [in] ICLRTask *pCLRTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cb438-106">参数</span><span class="sxs-lookup"><span data-stu-id="cb438-106">Parameters</span></span>  

 `pCLRTask`  
 <span data-ttu-id="cb438-107">中指向要 `ICLRTask` 与当前实例关联的实例的接口指针 `IHostTask` 。</span><span class="sxs-lookup"><span data-stu-id="cb438-107">[in] An interface pointer to the `ICLRTask` instance to be associated with the current `IHostTask` instance.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cb438-108">返回值</span><span class="sxs-lookup"><span data-stu-id="cb438-108">Return Value</span></span>  
  
|<span data-ttu-id="cb438-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="cb438-109">HRESULT</span></span>|<span data-ttu-id="cb438-110">说明</span><span class="sxs-lookup"><span data-stu-id="cb438-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="cb438-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="cb438-111">S_OK</span></span>|<span data-ttu-id="cb438-112">`SetCLRTask` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="cb438-112">`SetCLRTask` returned successfully.</span></span>|  
|<span data-ttu-id="cb438-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="cb438-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="cb438-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="cb438-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="cb438-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="cb438-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="cb438-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="cb438-116">The call timed out.</span></span>|  
|<span data-ttu-id="cb438-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="cb438-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="cb438-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="cb438-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="cb438-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="cb438-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="cb438-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="cb438-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="cb438-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cb438-121">E_FAIL</span></span>|<span data-ttu-id="cb438-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="cb438-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="cb438-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="cb438-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="cb438-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="cb438-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cb438-125">备注</span><span class="sxs-lookup"><span data-stu-id="cb438-125">Remarks</span></span>  

 <span data-ttu-id="cb438-126">CLR 调用将 `SetCLRTask` `ICLRTask` 实例与当前实例相关联 `IHostTask` ，该实例是通过调用 [IHostTaskManager：： CreateTask](ihosttaskmanager-createtask-method.md)创建的。</span><span class="sxs-lookup"><span data-stu-id="cb438-126">The CLR calls `SetCLRTask` to associate an `ICLRTask` instance with the current `IHostTask` instance, which was created by a call to [IHostTaskManager::CreateTask](ihosttaskmanager-createtask-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cb438-127">要求</span><span class="sxs-lookup"><span data-stu-id="cb438-127">Requirements</span></span>  

 <span data-ttu-id="cb438-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cb438-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cb438-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="cb438-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cb438-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cb438-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cb438-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cb438-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb438-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="cb438-132">See also</span></span>

- [<span data-ttu-id="cb438-133">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="cb438-133">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="cb438-134">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="cb438-134">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="cb438-135">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="cb438-135">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="cb438-136">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="cb438-136">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
