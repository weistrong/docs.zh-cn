---
description: 了解详细信息： IHostTaskManager：： Sleep 方法
title: IHostTaskManager::Sleep 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.Sleep
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::Sleep
helpviewer_keywords:
- IHostTaskManager::Sleep method [.NET Framework hosting]
- Sleep method, IHostTaskManager interface [.NET Framework hosting]
ms.assetid: f67d25f3-9199-4c5f-b1e8-1c819243cfd5
topic_type:
- apiref
ms.openlocfilehash: fedb87c6bd4558a2aa6158299551327cb2271d51
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789367"
---
# <a name="ihosttaskmanagersleep-method"></a><span data-ttu-id="cdc75-103">IHostTaskManager::Sleep 方法</span><span class="sxs-lookup"><span data-stu-id="cdc75-103">IHostTaskManager::Sleep Method</span></span>

<span data-ttu-id="cdc75-104">通知宿主当前任务将要进入睡眠状态。</span><span class="sxs-lookup"><span data-stu-id="cdc75-104">Notifies the host that the current task is going to sleep.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cdc75-105">语法</span><span class="sxs-lookup"><span data-stu-id="cdc75-105">Syntax</span></span>  
  
```cpp  
HRESULT Sleep (  
    [in] DWORD dwMilliseconds,  
    [in] DWORD option  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cdc75-106">参数</span><span class="sxs-lookup"><span data-stu-id="cdc75-106">Parameters</span></span>  

 `dwMilliseconds`  
 <span data-ttu-id="cdc75-107">中线程将进入睡眠状态的时间间隔（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="cdc75-107">[in] The time interval, in milliseconds, that the thread will sleep.</span></span>  
  
 `option`  
 <span data-ttu-id="cdc75-108">中 [WAIT_OPTION](wait-option-enumeration.md) 枚举值之一，指示当此操作阻止时宿主应执行的操作。</span><span class="sxs-lookup"><span data-stu-id="cdc75-108">[in] One of the [WAIT_OPTION](wait-option-enumeration.md) enumeration values, indicating what action the host should take if this action blocks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cdc75-109">返回值</span><span class="sxs-lookup"><span data-stu-id="cdc75-109">Return Value</span></span>  
  
|<span data-ttu-id="cdc75-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="cdc75-110">HRESULT</span></span>|<span data-ttu-id="cdc75-111">说明</span><span class="sxs-lookup"><span data-stu-id="cdc75-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="cdc75-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="cdc75-112">S_OK</span></span>|<span data-ttu-id="cdc75-113">`Sleep` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="cdc75-113">`Sleep` returned successfully.</span></span>|  
|<span data-ttu-id="cdc75-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="cdc75-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="cdc75-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="cdc75-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="cdc75-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="cdc75-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="cdc75-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="cdc75-117">The call timed out.</span></span>|  
|<span data-ttu-id="cdc75-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="cdc75-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="cdc75-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="cdc75-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="cdc75-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="cdc75-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="cdc75-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="cdc75-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="cdc75-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cdc75-122">E_FAIL</span></span>|<span data-ttu-id="cdc75-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="cdc75-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="cdc75-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="cdc75-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="cdc75-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="cdc75-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cdc75-126">备注</span><span class="sxs-lookup"><span data-stu-id="cdc75-126">Remarks</span></span>  

 <span data-ttu-id="cdc75-127">在 `IHostTaskManager::Sleep` <xref:System.Threading.Thread.Sleep%2A?displayProperty=nameWithType> 从用户代码调用时，CLR 通常会调用。</span><span class="sxs-lookup"><span data-stu-id="cdc75-127">The CLR typically calls `IHostTaskManager::Sleep` when <xref:System.Threading.Thread.Sleep%2A?displayProperty=nameWithType> is called from user code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cdc75-128">要求</span><span class="sxs-lookup"><span data-stu-id="cdc75-128">Requirements</span></span>  

 <span data-ttu-id="cdc75-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cdc75-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cdc75-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="cdc75-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cdc75-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cdc75-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cdc75-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cdc75-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cdc75-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="cdc75-133">See also</span></span>

- [<span data-ttu-id="cdc75-134">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="cdc75-134">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="cdc75-135">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="cdc75-135">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="cdc75-136">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="cdc75-136">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="cdc75-137">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="cdc75-137">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
