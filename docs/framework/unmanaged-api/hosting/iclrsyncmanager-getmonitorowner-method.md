---
description: 了解详细信息： ICLRSyncManager：： GetMonitorOwner 方法
title: ICLRSyncManager::GetMonitorOwner 方法
ms.date: 03/30/2017
api_name:
- ICLRSyncManager.GetMonitorOwner
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager::GetMonitorOwner
helpviewer_keywords:
- ICLRSyncManager::GetMonitorOwner method [.NET Framework hosting]
- GetMonitorOwner method [.NET Framework hosting]
ms.assetid: 840983a4-396d-47b4-86a0-d35f9b437cdb
topic_type:
- apiref
ms.openlocfilehash: 67fb966c415009236cabef5e6b4d27cbb90d50ac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785024"
---
# <a name="iclrsyncmanagergetmonitorowner-method"></a><span data-ttu-id="047f9-103">ICLRSyncManager::GetMonitorOwner 方法</span><span class="sxs-lookup"><span data-stu-id="047f9-103">ICLRSyncManager::GetMonitorOwner Method</span></span>

<span data-ttu-id="047f9-104">获取拥有由指定 cookie 标识的监视器的 [IHostTask](ihosttask-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="047f9-104">Gets the [IHostTask](ihosttask-interface.md) instance that owns the monitor identified by the specified cookie.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="047f9-105">语法</span><span class="sxs-lookup"><span data-stu-id="047f9-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMonitorOwner (  
    [in]  SIZE_T     cookie,  
    [out] IHostTask *ppOwnerHostTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="047f9-106">参数</span><span class="sxs-lookup"><span data-stu-id="047f9-106">Parameters</span></span>  

 `cookie`  
 <span data-ttu-id="047f9-107">中与监视器关联的 cookie。</span><span class="sxs-lookup"><span data-stu-id="047f9-107">[in] The cookie associated with the monitor.</span></span>  
  
 `ppOwnerHostTask`  
 <span data-ttu-id="047f9-108">弄指向 `IHostTask` 当前拥有监视器的的指针; 如果没有任务具有所有权，则为 null。</span><span class="sxs-lookup"><span data-stu-id="047f9-108">[out] A pointer to the `IHostTask` that currently owns the monitor, or null if no task has ownership.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="047f9-109">返回值</span><span class="sxs-lookup"><span data-stu-id="047f9-109">Return Value</span></span>  
  
|<span data-ttu-id="047f9-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="047f9-110">HRESULT</span></span>|<span data-ttu-id="047f9-111">说明</span><span class="sxs-lookup"><span data-stu-id="047f9-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="047f9-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="047f9-112">S_OK</span></span>|<span data-ttu-id="047f9-113">`GetMonitorOwner` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="047f9-113">`GetMonitorOwner` returned successfully.</span></span>|  
|<span data-ttu-id="047f9-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="047f9-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="047f9-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="047f9-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="047f9-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="047f9-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="047f9-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="047f9-117">The call timed out.</span></span>|  
|<span data-ttu-id="047f9-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="047f9-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="047f9-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="047f9-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="047f9-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="047f9-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="047f9-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="047f9-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="047f9-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="047f9-122">E_FAIL</span></span>|<span data-ttu-id="047f9-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="047f9-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="047f9-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="047f9-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="047f9-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="047f9-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="047f9-126">备注</span><span class="sxs-lookup"><span data-stu-id="047f9-126">Remarks</span></span>  

 <span data-ttu-id="047f9-127">宿主通常 `GetMonitorOwner` 作为死锁检测机制的一部分来调用。</span><span class="sxs-lookup"><span data-stu-id="047f9-127">The host typically calls `GetMonitorOwner` as part of a deadlock-detection mechanism.</span></span> <span data-ttu-id="047f9-128">当使用 [IHostSyncManager：： CreateMonitorEvent](ihostsyncmanager-createmonitorevent-method.md)调用创建该 cookie 时，该 cookie 与监视器相关联。</span><span class="sxs-lookup"><span data-stu-id="047f9-128">The cookie is associated with a monitor when it is created by using a call to [IHostSyncManager::CreateMonitorEvent](ihostsyncmanager-createmonitorevent-method.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="047f9-129">如果调用此方法的调用当前对与该监视器关联的 cookie 有效，则调用会阻止该调用，但不会死锁。</span><span class="sxs-lookup"><span data-stu-id="047f9-129">A call to release the event underlying the monitor might block—but will not deadlock—if a call to this method is currently in effect on the cookie associated with that monitor.</span></span> <span data-ttu-id="047f9-130">其他任务也可能会在尝试获取此监视器时阻止。</span><span class="sxs-lookup"><span data-stu-id="047f9-130">Other tasks might also block if they attempt to acquire this monitor.</span></span>  
  
 <span data-ttu-id="047f9-131">`GetMonitorOwner` 始终立即返回，并且可以在调用后随时调用 `CreateMonitorEvent` 。</span><span class="sxs-lookup"><span data-stu-id="047f9-131">`GetMonitorOwner` always returns immediately and can be called any time after a call to `CreateMonitorEvent`.</span></span> <span data-ttu-id="047f9-132">宿主无需等待，直到任务等待事件。</span><span class="sxs-lookup"><span data-stu-id="047f9-132">The host does not need to wait until a task is waiting on the event.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="047f9-133">要求</span><span class="sxs-lookup"><span data-stu-id="047f9-133">Requirements</span></span>  

 <span data-ttu-id="047f9-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="047f9-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="047f9-135">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="047f9-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="047f9-136">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="047f9-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="047f9-137">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="047f9-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="047f9-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="047f9-138">See also</span></span>

- [<span data-ttu-id="047f9-139">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="047f9-139">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="047f9-140">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="047f9-140">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
