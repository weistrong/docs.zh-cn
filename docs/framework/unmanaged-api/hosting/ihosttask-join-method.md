---
description: 了解详细信息： IHostTask：： Join 方法
title: IHostTask::Join 方法
ms.date: 03/30/2017
api_name:
- IHostTask.Join
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::Join
helpviewer_keywords:
- IHostTask::Join method [.NET Framework hosting]
- Join method, IHostTask interface [.NET Framework hosting]
ms.assetid: 2cffcc52-19e0-4ced-a440-fc7375078ac9
topic_type:
- apiref
ms.openlocfilehash: 8231401ab01ee040f225b78a52b61eb7d59af1d7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784647"
---
# <a name="ihosttaskjoin-method"></a><span data-ttu-id="f6e09-103">IHostTask::Join 方法</span><span class="sxs-lookup"><span data-stu-id="f6e09-103">IHostTask::Join Method</span></span>

<span data-ttu-id="f6e09-104">阻止调用任务，直到当前 [IHostTask](ihosttask-interface.md) 实例表示的任务完成，指定的时间间隔结束，或调用 [IHostTask：： Alert](ihosttask-alert-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6e09-104">Blocks the calling task until the task represented by the current [IHostTask](ihosttask-interface.md) instance completes, the specified time interval elapses, or [IHostTask::Alert](ihosttask-alert-method.md) is called.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6e09-105">语法</span><span class="sxs-lookup"><span data-stu-id="f6e09-105">Syntax</span></span>  
  
```cpp  
HRESULT Join (  
    [in] DWORD milliseconds,  
    [in] DWORD option  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f6e09-106">参数</span><span class="sxs-lookup"><span data-stu-id="f6e09-106">Parameters</span></span>  

 `milliseconds`  
 <span data-ttu-id="f6e09-107">中等待任务终止的时间间隔（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="f6e09-107">[in] The time interval, in milliseconds, to wait for the task to terminate.</span></span> <span data-ttu-id="f6e09-108">如果此时间间隔在任务终止之前过期，则调用任务会取消阻止。</span><span class="sxs-lookup"><span data-stu-id="f6e09-108">If this interval elapses before the task terminates, the calling task unblocks.</span></span>  
  
 `option`  
 <span data-ttu-id="f6e09-109">中 [WAIT_OPTION](wait-option-enumeration.md) 值之一。</span><span class="sxs-lookup"><span data-stu-id="f6e09-109">[in] One of the [WAIT_OPTION](wait-option-enumeration.md) values.</span></span> <span data-ttu-id="f6e09-110">如果在 `Alert` 过去之前调用，则值 WAIT_ALERTABLE 指示宿主唤醒任务 `milliseconds` 。</span><span class="sxs-lookup"><span data-stu-id="f6e09-110">A value of WAIT_ALERTABLE instructs the host to wake the task if `Alert` is called before `milliseconds` elapses.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f6e09-111">返回值</span><span class="sxs-lookup"><span data-stu-id="f6e09-111">Return Value</span></span>  
  
|<span data-ttu-id="f6e09-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f6e09-112">HRESULT</span></span>|<span data-ttu-id="f6e09-113">说明</span><span class="sxs-lookup"><span data-stu-id="f6e09-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f6e09-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6e09-114">S_OK</span></span>|<span data-ttu-id="f6e09-115">`Join` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f6e09-115">`Join` returned successfully.</span></span>|  
|<span data-ttu-id="f6e09-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f6e09-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f6e09-117"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f6e09-117">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f6e09-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f6e09-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f6e09-119">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f6e09-119">The call timed out.</span></span>|  
|<span data-ttu-id="f6e09-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f6e09-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f6e09-121">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f6e09-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f6e09-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f6e09-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f6e09-123">已阻止的线程或纤程正在等待事件，或当前 `IHostTask` 实例未与任务关联时，已取消该事件。</span><span class="sxs-lookup"><span data-stu-id="f6e09-123">An event was canceled while a blocked thread or fiber was waiting on it, or the current `IHostTask` instance is not associated with a task.</span></span>|  
|<span data-ttu-id="f6e09-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f6e09-124">E_FAIL</span></span>|<span data-ttu-id="f6e09-125">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f6e09-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f6e09-126">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f6e09-126">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f6e09-127">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f6e09-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f6e09-128">要求</span><span class="sxs-lookup"><span data-stu-id="f6e09-128">Requirements</span></span>  

 <span data-ttu-id="f6e09-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f6e09-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6e09-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f6e09-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f6e09-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f6e09-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f6e09-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6e09-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6e09-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="f6e09-133">See also</span></span>

- [<span data-ttu-id="f6e09-134">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="f6e09-134">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="f6e09-135">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="f6e09-135">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="f6e09-136">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="f6e09-136">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="f6e09-137">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="f6e09-137">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="f6e09-138">WAIT_OPTION 枚举</span><span class="sxs-lookup"><span data-stu-id="f6e09-138">WAIT_OPTION Enumeration</span></span>](wait-option-enumeration.md)
