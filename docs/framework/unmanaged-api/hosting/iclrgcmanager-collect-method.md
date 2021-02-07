---
description: 了解详细信息： ICLRGCManager：： Collect 方法
title: ICLRGCManager::Collect 方法
ms.date: 03/30/2017
api_name:
- ICLRGCManager.Collect
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRGCManager::Collect
helpviewer_keywords:
- ICLRGCManager::Collect method [.NET Framework hosting]
- Collect method, ICLRGCManager interface [.NET Framework hosting]
ms.assetid: 0c6cbbea-c27c-4695-bda3-17c1910d8ddb
topic_type:
- apiref
ms.openlocfilehash: 7c2649f7ce3472c504c1e48a203cf89d4b8508e3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746030"
---
# <a name="iclrgcmanagercollect-method"></a><span data-ttu-id="2b9d4-103">ICLRGCManager::Collect 方法</span><span class="sxs-lookup"><span data-stu-id="2b9d4-103">ICLRGCManager::Collect Method</span></span>

<span data-ttu-id="2b9d4-104">强制执行指定代的垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-104">Forces a garbage collection for the specified generation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b9d4-105">语法</span><span class="sxs-lookup"><span data-stu-id="2b9d4-105">Syntax</span></span>  
  
```cpp  
HRESULT Collect (  
    [in] LONG Generation  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2b9d4-106">参数</span><span class="sxs-lookup"><span data-stu-id="2b9d4-106">Parameters</span></span>  

 `Generation`  
 <span data-ttu-id="2b9d4-107">中要收集的代。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-107">[in] The generation to collect.</span></span> <span data-ttu-id="2b9d4-108">如果值为-1，则强制收集所有代。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-108">A value of -1 forces a collection of all generations.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2b9d4-109">返回值</span><span class="sxs-lookup"><span data-stu-id="2b9d4-109">Return Value</span></span>  
  
|<span data-ttu-id="2b9d4-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2b9d4-110">HRESULT</span></span>|<span data-ttu-id="2b9d4-111">说明</span><span class="sxs-lookup"><span data-stu-id="2b9d4-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2b9d4-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b9d4-112">S_OK</span></span>|<span data-ttu-id="2b9d4-113">`Collect` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-113">`Collect` returned successfully.</span></span>|  
|<span data-ttu-id="2b9d4-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="2b9d4-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="2b9d4-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="2b9d4-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2b9d4-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="2b9d4-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-117">The call timed out.</span></span>|  
|<span data-ttu-id="2b9d4-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="2b9d4-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="2b9d4-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="2b9d4-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="2b9d4-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="2b9d4-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="2b9d4-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="2b9d4-122">E_FAIL</span></span>|<span data-ttu-id="2b9d4-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="2b9d4-124">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-124">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="2b9d4-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2b9d4-126">备注</span><span class="sxs-lookup"><span data-stu-id="2b9d4-126">Remarks</span></span>  

 <span data-ttu-id="2b9d4-127">`Collect`方法强制 CLR 的垃圾回收器执行集合，而不考虑其当前状态。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-127">The `Collect` method forces the CLR's garbage collector to perform a collection regardless of its current state.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2b9d4-128">要求</span><span class="sxs-lookup"><span data-stu-id="2b9d4-128">Requirements</span></span>  

 <span data-ttu-id="2b9d4-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2b9d4-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2b9d4-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="2b9d4-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2b9d4-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2b9d4-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2b9d4-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2b9d4-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b9d4-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="2b9d4-133">See also</span></span>

- [<span data-ttu-id="2b9d4-134">自动内存管理</span><span class="sxs-lookup"><span data-stu-id="2b9d4-134">Automatic Memory Management</span></span>](../../../standard/automatic-memory-management.md)
- [<span data-ttu-id="2b9d4-135">垃圾回收</span><span class="sxs-lookup"><span data-stu-id="2b9d4-135">Garbage Collection</span></span>](../../../standard/garbage-collection/index.md)
- [<span data-ttu-id="2b9d4-136">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="2b9d4-136">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="2b9d4-137">ICLRGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="2b9d4-137">ICLRGCManager Interface</span></span>](iclrgcmanager-interface.md)
- [<span data-ttu-id="2b9d4-138">CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="2b9d4-138">CLR Hosting Interfaces</span></span>](clr-hosting-interfaces.md)
- [<span data-ttu-id="2b9d4-139">承载接口</span><span class="sxs-lookup"><span data-stu-id="2b9d4-139">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="2b9d4-140">承载</span><span class="sxs-lookup"><span data-stu-id="2b9d4-140">Hosting</span></span>](index.md)
