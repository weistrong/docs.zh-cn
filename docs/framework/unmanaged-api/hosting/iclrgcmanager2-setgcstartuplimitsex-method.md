---
description: 了解详细信息： ICLRGCManager2：： SetGCStartupLimitsEx 方法
title: ICLRGCManager2::SetGCStartupLimitsEx 方法
ms.date: 03/30/2017
api_name:
- ICLRGCManager2.SetGCStartupLimitsEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRGCManager2::SetCLRGCStartupLimitsEx
helpviewer_keywords:
- ICLRGCManager2::SetGCStartupLimitsEx method [.NET Framework hosting]
- SetGCStartupLimitsEx method, ICLRGCManager2 interface [.NET Framework hosting]
ms.assetid: 6c3a08a9-5d65-48d4-8bbf-2a86ed7d356a
topic_type:
- apiref
ms.openlocfilehash: 2a4801d2f6255f5f84e0a4bae7a1886689ee8dc5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689231"
---
# <a name="iclrgcmanager2setgcstartuplimitsex-method"></a><span data-ttu-id="50bf8-103">ICLRGCManager2::SetGCStartupLimitsEx 方法</span><span class="sxs-lookup"><span data-stu-id="50bf8-103">ICLRGCManager2::SetGCStartupLimitsEx Method</span></span>

<span data-ttu-id="50bf8-104">设置垃圾回收段的大小以及垃圾回收系统的第0代的最大大小。</span><span class="sxs-lookup"><span data-stu-id="50bf8-104">Sets the size of a garbage collection segment and the maximum size of the garbage collection system's generation 0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50bf8-105">语法</span><span class="sxs-lookup"><span data-stu-id="50bf8-105">Syntax</span></span>  
  
```cpp  
HRESULT SetGCStartupLimitsEx (  
    [in] SIZE_T SegmentSize,
    [in] SIZE_T MaxGen0Size  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="50bf8-106">参数</span><span class="sxs-lookup"><span data-stu-id="50bf8-106">Parameters</span></span>  

 `SegmentSize`  
 <span data-ttu-id="50bf8-107">中垃圾收集段的指定大小。</span><span class="sxs-lookup"><span data-stu-id="50bf8-107">[in] The specified size of a garbage collection segment.</span></span>  
  
 <span data-ttu-id="50bf8-108">最小段大小为 4 MB。</span><span class="sxs-lookup"><span data-stu-id="50bf8-108">The minimum segment size is 4 MB.</span></span> <span data-ttu-id="50bf8-109">段可以增加 1 MB 或更大的增量。</span><span class="sxs-lookup"><span data-stu-id="50bf8-109">Segments can be increased in increments of 1 MB or larger.</span></span>  
  
 `MaxGen0Size`  
 <span data-ttu-id="50bf8-110">中第0代的指定最大大小。</span><span class="sxs-lookup"><span data-stu-id="50bf8-110">[in] The specified maximum size for generation 0.</span></span>  
  
 <span data-ttu-id="50bf8-111">最小第0代大小为 64 KB。</span><span class="sxs-lookup"><span data-stu-id="50bf8-111">The minimum generation 0 size is 64 KB.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="50bf8-112">返回值</span><span class="sxs-lookup"><span data-stu-id="50bf8-112">Return Value</span></span>  
  
|<span data-ttu-id="50bf8-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="50bf8-113">HRESULT</span></span>|<span data-ttu-id="50bf8-114">说明</span><span class="sxs-lookup"><span data-stu-id="50bf8-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="50bf8-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="50bf8-115">S_OK</span></span>|<span data-ttu-id="50bf8-116">`SetGCStartupLimitsEx` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="50bf8-116">`SetGCStartupLimitsEx` returned successfully.</span></span>|  
|<span data-ttu-id="50bf8-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="50bf8-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="50bf8-118"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="50bf8-118">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="50bf8-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="50bf8-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="50bf8-120">调用超时。</span><span class="sxs-lookup"><span data-stu-id="50bf8-120">The call timed out.</span></span>|  
|<span data-ttu-id="50bf8-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="50bf8-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="50bf8-122">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="50bf8-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="50bf8-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="50bf8-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="50bf8-124">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="50bf8-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="50bf8-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="50bf8-125">E_FAIL</span></span>|<span data-ttu-id="50bf8-126">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="50bf8-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="50bf8-127">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="50bf8-127">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="50bf8-128">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="50bf8-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="50bf8-129">备注</span><span class="sxs-lookup"><span data-stu-id="50bf8-129">Remarks</span></span>  

 <span data-ttu-id="50bf8-130">`SetGCStartupLimitsEx`只能在启动主机之前指定设置的值。</span><span class="sxs-lookup"><span data-stu-id="50bf8-130">The values that `SetGCStartupLimitsEx` sets can be specified only before the host is started.</span></span> <span data-ttu-id="50bf8-131">`SetGCStartupLimitsEx`将忽略以后对的调用。</span><span class="sxs-lookup"><span data-stu-id="50bf8-131">Later calls to `SetGCStartupLimitsEx` are ignored.</span></span>  
  
 <span data-ttu-id="50bf8-132">若要设置任一参数而不影响其他参数，请为不想更改的参数指定 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="50bf8-132">To set either parameter without affecting the other, specify 0 (zero) for the parameter you don't want to change.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="50bf8-133">要求</span><span class="sxs-lookup"><span data-stu-id="50bf8-133">Requirements</span></span>  

 <span data-ttu-id="50bf8-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="50bf8-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="50bf8-135">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="50bf8-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="50bf8-136">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="50bf8-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="50bf8-137">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="50bf8-137">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50bf8-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="50bf8-138">See also</span></span>

- [<span data-ttu-id="50bf8-139">自动内存管理</span><span class="sxs-lookup"><span data-stu-id="50bf8-139">Automatic Memory Management</span></span>](../../../standard/automatic-memory-management.md)
- [<span data-ttu-id="50bf8-140">垃圾回收</span><span class="sxs-lookup"><span data-stu-id="50bf8-140">Garbage Collection</span></span>](../../../standard/garbage-collection/index.md)
- [<span data-ttu-id="50bf8-141">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="50bf8-141">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="50bf8-142">ICLRGCManager2 接口</span><span class="sxs-lookup"><span data-stu-id="50bf8-142">ICLRGCManager2 Interface</span></span>](iclrgcmanager2-interface.md)
