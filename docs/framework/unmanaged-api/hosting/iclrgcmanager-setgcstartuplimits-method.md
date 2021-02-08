---
description: 了解详细信息： ICLRGCManager：： SetGCStartupLimits 方法
title: ICLRGCManager::SetGCStartupLimits 方法
ms.date: 03/30/2017
api_name:
- ICLRGCManager.SetGCStartupLimits
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRGCManager::SetGCStartupLimits
helpviewer_keywords:
- SetGCStartupLimits method, ICLRGCManager interface [.NET Framework hosting]
- ICLRGCManager::SetGCStartupLimits method [.NET Framework hosting]
ms.assetid: 1c8d9959-95b5-4131-be4a-556d97774014
topic_type:
- apiref
ms.openlocfilehash: 5614b41cfd7a7938cdb653d879119ddbd9560b9d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789978"
---
# <a name="iclrgcmanagersetgcstartuplimits-method"></a><span data-ttu-id="d2160-103">ICLRGCManager::SetGCStartupLimits 方法</span><span class="sxs-lookup"><span data-stu-id="d2160-103">ICLRGCManager::SetGCStartupLimits Method</span></span>

<span data-ttu-id="d2160-104">设置垃圾回收段的大小以及垃圾回收系统的第0代的最大大小。</span><span class="sxs-lookup"><span data-stu-id="d2160-104">Sets the size of a garbage collection segment and the maximum size of the garbage collection system's generation 0.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="d2160-105">从 .NET Framework 4.5 开始，可以 `DWORD` 使用 [ICLRGCManager2：： SetGCStartupLimitsEx](iclrgcmanager2-setgcstartuplimitsex-method.md) 方法将段大小和最大第0代大小设置为大于的值。</span><span class="sxs-lookup"><span data-stu-id="d2160-105">Starting with the .NET Framework 4.5, you can set segment size and maximum generation 0 size to values greater than `DWORD` by using the [ICLRGCManager2::SetGCStartupLimitsEx](iclrgcmanager2-setgcstartuplimitsex-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d2160-106">语法</span><span class="sxs-lookup"><span data-stu-id="d2160-106">Syntax</span></span>  
  
```cpp  
HRESULT SetGCStartupLimits (  
    [in] DWORD SegmentSize,
    [in] DWORD MaxGen0Size  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d2160-107">参数</span><span class="sxs-lookup"><span data-stu-id="d2160-107">Parameters</span></span>  

 `SegmentSize`  
 <span data-ttu-id="d2160-108">中垃圾收集段的指定大小。</span><span class="sxs-lookup"><span data-stu-id="d2160-108">[in] The specified size of a garbage collection segment.</span></span>  
  
 <span data-ttu-id="d2160-109">最小段大小为 4 MB。</span><span class="sxs-lookup"><span data-stu-id="d2160-109">The minimum segment size is 4 MB.</span></span> <span data-ttu-id="d2160-110">段可以增加 1 MB 或更大的增量。</span><span class="sxs-lookup"><span data-stu-id="d2160-110">Segments can be increased in increments of 1 MB or larger.</span></span>  
  
 `MaxGen0Size`  
 <span data-ttu-id="d2160-111">中第0代的指定最大大小。</span><span class="sxs-lookup"><span data-stu-id="d2160-111">[in] The specified maximum size for generation 0.</span></span>  
  
 <span data-ttu-id="d2160-112">最小第0代大小为 64 KB。</span><span class="sxs-lookup"><span data-stu-id="d2160-112">The minimum generation 0 size is 64 KB.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d2160-113">返回值</span><span class="sxs-lookup"><span data-stu-id="d2160-113">Return Value</span></span>  
  
|<span data-ttu-id="d2160-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d2160-114">HRESULT</span></span>|<span data-ttu-id="d2160-115">说明</span><span class="sxs-lookup"><span data-stu-id="d2160-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d2160-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2160-116">S_OK</span></span>|<span data-ttu-id="d2160-117">`SetGCStartupLimits` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="d2160-117">`SetGCStartupLimits` returned successfully.</span></span>|  
|<span data-ttu-id="d2160-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d2160-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d2160-119"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="d2160-119">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d2160-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d2160-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="d2160-121">调用超时。</span><span class="sxs-lookup"><span data-stu-id="d2160-121">The call timed out.</span></span>|  
|<span data-ttu-id="d2160-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="d2160-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="d2160-123">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="d2160-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="d2160-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="d2160-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="d2160-125">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="d2160-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="d2160-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d2160-126">E_FAIL</span></span>|<span data-ttu-id="d2160-127">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="d2160-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d2160-128">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="d2160-128">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d2160-129">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="d2160-129">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d2160-130">备注</span><span class="sxs-lookup"><span data-stu-id="d2160-130">Remarks</span></span>  

 <span data-ttu-id="d2160-131">设置的值 `SetGCStartupLimits` 只能指定一次。</span><span class="sxs-lookup"><span data-stu-id="d2160-131">The values that `SetGCStartupLimits` sets can be specified only once.</span></span> <span data-ttu-id="d2160-132">`SetGCStartupLimits`将忽略以后对的调用。</span><span class="sxs-lookup"><span data-stu-id="d2160-132">Later calls to `SetGCStartupLimits` are ignored.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d2160-133">要求</span><span class="sxs-lookup"><span data-stu-id="d2160-133">Requirements</span></span>  

 <span data-ttu-id="d2160-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d2160-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d2160-135">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d2160-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d2160-136">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d2160-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d2160-137">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d2160-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2160-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="d2160-138">See also</span></span>

- [<span data-ttu-id="d2160-139">自动内存管理</span><span class="sxs-lookup"><span data-stu-id="d2160-139">Automatic Memory Management</span></span>](../../../standard/automatic-memory-management.md)
- [<span data-ttu-id="d2160-140">垃圾回收</span><span class="sxs-lookup"><span data-stu-id="d2160-140">Garbage Collection</span></span>](../../../standard/garbage-collection/index.md)
- [<span data-ttu-id="d2160-141">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="d2160-141">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="d2160-142">ICLRGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="d2160-142">ICLRGCManager Interface</span></span>](iclrgcmanager-interface.md)
