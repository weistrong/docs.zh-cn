---
description: 了解详细信息： IHostSyncManager：： CreateAutoEvent 方法
title: IHostSyncManager::CreateAutoEvent 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateAutoEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateAutoEvent
helpviewer_keywords:
- IHostSyncManager::CreateAutoEvent method [.NET Framework hosting]
- CreateAutoEvent method [.NET Framework hosting]
ms.assetid: 3153643e-cf5c-4b44-8e0e-c2b22cb08208
topic_type:
- apiref
ms.openlocfilehash: 69767f1e01ead93c874eecf01c3167a5dc0e4b82
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784842"
---
# <a name="ihostsyncmanagercreateautoevent-method"></a><span data-ttu-id="38297-103">IHostSyncManager::CreateAutoEvent 方法</span><span class="sxs-lookup"><span data-stu-id="38297-103">IHostSyncManager::CreateAutoEvent Method</span></span>

<span data-ttu-id="38297-104">创建自动重置事件对象。</span><span class="sxs-lookup"><span data-stu-id="38297-104">Creates an auto-reset event object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38297-105">语法</span><span class="sxs-lookup"><span data-stu-id="38297-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateAutoEvent (  
    [out] IHostAutoEvent **ppEvent  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="38297-106">参数</span><span class="sxs-lookup"><span data-stu-id="38297-106">Parameters</span></span>  

 `ppEvent`  
 <span data-ttu-id="38297-107">弄指向由主机实现的 [IHostAutoEvent](ihostautoevent-interface.md) 实例的地址的指针; 如果无法创建事件对象，则为 null。</span><span class="sxs-lookup"><span data-stu-id="38297-107">[out] A pointer to the address of an [IHostAutoEvent](ihostautoevent-interface.md) instance implemented by the host, or null if the event object could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="38297-108">返回值</span><span class="sxs-lookup"><span data-stu-id="38297-108">Return Value</span></span>  
  
|<span data-ttu-id="38297-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="38297-109">HRESULT</span></span>|<span data-ttu-id="38297-110">说明</span><span class="sxs-lookup"><span data-stu-id="38297-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="38297-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="38297-111">S_OK</span></span>|<span data-ttu-id="38297-112">`CreateAutoEvent` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="38297-112">`CreateAutoEvent` returned successfully.</span></span>|  
|<span data-ttu-id="38297-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="38297-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="38297-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="38297-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="38297-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="38297-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="38297-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="38297-116">The call timed out.</span></span>|  
|<span data-ttu-id="38297-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="38297-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="38297-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="38297-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="38297-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="38297-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="38297-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="38297-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="38297-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="38297-121">E_FAIL</span></span>|<span data-ttu-id="38297-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="38297-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="38297-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="38297-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="38297-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="38297-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="38297-125">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="38297-125">E_OUTOFMEMORY</span></span>|<span data-ttu-id="38297-126">没有足够的内存可用于创建请求的事件对象。</span><span class="sxs-lookup"><span data-stu-id="38297-126">Not enough memory was available to create the requested event object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="38297-127">备注</span><span class="sxs-lookup"><span data-stu-id="38297-127">Remarks</span></span>  

 <span data-ttu-id="38297-128">`CreateAutoEvent` 创建自动事件对象，其状态将在释放等待线程后自动更改为非终止状态。</span><span class="sxs-lookup"><span data-stu-id="38297-128">`CreateAutoEvent` creates an auto-event object whose state is automatically changed to non-signaled after the waiting thread has been released.</span></span> <span data-ttu-id="38297-129">此方法 `CreateEvent` 使用 `false` 为参数指定的值镜像 Win32 函数 `bManualReset`</span><span class="sxs-lookup"><span data-stu-id="38297-129">This method mirrors the Win32 `CreateEvent` function with a value of `false` specified for the `bManualReset` parameter</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="38297-130">要求</span><span class="sxs-lookup"><span data-stu-id="38297-130">Requirements</span></span>  

 <span data-ttu-id="38297-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="38297-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="38297-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="38297-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="38297-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="38297-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="38297-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="38297-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38297-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="38297-135">See also</span></span>

- [<span data-ttu-id="38297-136">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="38297-136">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="38297-137">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="38297-137">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="38297-138">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="38297-138">IHostControl Interface</span></span>](ihostcontrol-interface.md)
- [<span data-ttu-id="38297-139">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="38297-139">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
