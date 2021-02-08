---
description: 了解详细信息： IHostSyncManager：： CreateManualEvent 方法
title: IHostSyncManager::CreateManualEvent 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateManualEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateManualEvent
helpviewer_keywords:
- CreateManualEvent method [.NET Framework hosting]
- IHostSyncManager::CreateManualEvent method [.NET Framework hosting]
ms.assetid: 68661fbd-09cf-46dc-890b-e694f8a3880a
topic_type:
- apiref
ms.openlocfilehash: 300d6cbf9555eb331a470767cdfb2745da300bb6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784790"
---
# <a name="ihostsyncmanagercreatemanualevent-method"></a><span data-ttu-id="5f3b6-103">IHostSyncManager::CreateManualEvent 方法</span><span class="sxs-lookup"><span data-stu-id="5f3b6-103">IHostSyncManager::CreateManualEvent Method</span></span>

<span data-ttu-id="5f3b6-104">创建手动重置的事件对象。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-104">Creates a manual-reset event object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f3b6-105">语法</span><span class="sxs-lookup"><span data-stu-id="5f3b6-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateManualEvent (  
    [in]  BOOL bInitialState,  
    [out] IHostManualEvent **ppEvent  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5f3b6-106">参数</span><span class="sxs-lookup"><span data-stu-id="5f3b6-106">Parameters</span></span>  

 `bInitialState`  
 <span data-ttu-id="5f3b6-107">[in] `true` ，如果对象已终止，则为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-107">[in] `true`, if the object is signaled; otherwise, `false`.</span></span>  
  
 `ppEvent`  
 <span data-ttu-id="5f3b6-108">弄指向 [IHostManualEvent](ihostmanualevent-interface.md) 实例的地址的指针; 如果未能创建该事件，则为 null。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-108">[out] A pointer to the address of an [IHostManualEvent](ihostmanualevent-interface.md) instance, or null if the event could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5f3b6-109">返回值</span><span class="sxs-lookup"><span data-stu-id="5f3b6-109">Return Value</span></span>  
  
|<span data-ttu-id="5f3b6-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="5f3b6-110">HRESULT</span></span>|<span data-ttu-id="5f3b6-111">说明</span><span class="sxs-lookup"><span data-stu-id="5f3b6-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5f3b6-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f3b6-112">S_OK</span></span>|<span data-ttu-id="5f3b6-113">`CreateManualEvent` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-113">`CreateManualEvent` returned successfully.</span></span>|  
|<span data-ttu-id="5f3b6-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="5f3b6-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="5f3b6-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="5f3b6-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="5f3b6-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="5f3b6-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-117">The call timed out.</span></span>|  
|<span data-ttu-id="5f3b6-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="5f3b6-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="5f3b6-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="5f3b6-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="5f3b6-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="5f3b6-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="5f3b6-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="5f3b6-122">E_FAIL</span></span>|<span data-ttu-id="5f3b6-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="5f3b6-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="5f3b6-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="5f3b6-126">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="5f3b6-126">E_OUTOFMEMORY</span></span>|<span data-ttu-id="5f3b6-127">没有足够的内存可用于创建请求的事件对象。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-127">Not enough memory was available to create the requested event object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5f3b6-128">备注</span><span class="sxs-lookup"><span data-stu-id="5f3b6-128">Remarks</span></span>  

 <span data-ttu-id="5f3b6-129">`CreateManualEvent` 创建一个 `IHostManualEvent` 手动重置事件对象，该对象需要调用 [IHostManualEvent：： reset](ihostmanualevent-reset-method.md) 方法，以将其设置为非终止状态。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-129">`CreateManualEvent` creates an `IHostManualEvent`, a manual-reset event object that requires a call to the [IHostManualEvent::Reset](ihostmanualevent-reset-method.md) method to set it to a non-signaled state.</span></span> <span data-ttu-id="5f3b6-130">`CreateManualEvent``CreateEvent`使用 `true` 为参数指定的值镜像 Win32 函数 `bManualReset` 。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-130">`CreateManualEvent` mirrors the Win32 `CreateEvent` function with a value of `true` specified for the `bManualReset` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f3b6-131">要求</span><span class="sxs-lookup"><span data-stu-id="5f3b6-131">Requirements</span></span>  

 <span data-ttu-id="5f3b6-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f3b6-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f3b6-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5f3b6-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5f3b6-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5f3b6-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5f3b6-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f3b6-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f3b6-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f3b6-136">See also</span></span>

- [<span data-ttu-id="5f3b6-137">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="5f3b6-137">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="5f3b6-138">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="5f3b6-138">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="5f3b6-139">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="5f3b6-139">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
