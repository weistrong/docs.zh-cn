---
description: 了解详细信息： IHostSyncManager：： CreateSemaphore 方法
title: IHostSyncManager::CreateSemaphore 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateSemaphore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateSemaphore
helpviewer_keywords:
- CreateSemaphore method [.NET Framework hosting]
- IHostSyncManager::CreateSemaphore method [.NET Framework hosting]
ms.assetid: 37679e94-5ff9-4173-8fa5-457febeb89bf
topic_type:
- apiref
ms.openlocfilehash: 5a03ef7532e2ac8357ec015b40cc54942f5420e5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784738"
---
# <a name="ihostsyncmanagercreatesemaphore-method"></a><span data-ttu-id="f1c7b-103">IHostSyncManager::CreateSemaphore 方法</span><span class="sxs-lookup"><span data-stu-id="f1c7b-103">IHostSyncManager::CreateSemaphore Method</span></span>

<span data-ttu-id="f1c7b-104">为公共语言运行时 (CLR) 创建一个 [IHostSemaphore](ihostsemaphore-interface.md) 对象，该对象用作等待事件的信号量。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-104">Creates an [IHostSemaphore](ihostsemaphore-interface.md) object for the common language runtime (CLR) to use as a semaphore for wait events.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1c7b-105">语法</span><span class="sxs-lookup"><span data-stu-id="f1c7b-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateSemaphore (  
    [in]  DWORD dwInitial,  
    [in]  DWORD dwMax,  
    [out] IHostSemaphore **ppSemaphore  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f1c7b-106">参数</span><span class="sxs-lookup"><span data-stu-id="f1c7b-106">Parameters</span></span>  

 `dwInitial`  
 <span data-ttu-id="f1c7b-107">中的初始计数 `ppSemaphore` 。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-107">[in] The initial count for `ppSemaphore`.</span></span>  
  
 `dwMax`  
 <span data-ttu-id="f1c7b-108">中的最大计数 `ppSemaphore` 。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-108">[in] The maximum count for `ppSemaphore`.</span></span>  
  
 `ppSemaphore`  
 <span data-ttu-id="f1c7b-109">弄指向实例的地址的指针 `IHostSemaphore` ; 如果无法创建信号量，则为 null。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-109">[out] A pointer to the address of an `IHostSemaphore` instance, or null if the semaphore could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f1c7b-110">返回值</span><span class="sxs-lookup"><span data-stu-id="f1c7b-110">Return Value</span></span>  
  
|<span data-ttu-id="f1c7b-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f1c7b-111">HRESULT</span></span>|<span data-ttu-id="f1c7b-112">说明</span><span class="sxs-lookup"><span data-stu-id="f1c7b-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f1c7b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1c7b-113">S_OK</span></span>|<span data-ttu-id="f1c7b-114">`CreateSemaphore` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-114">`CreateSemaphore` returned successfully.</span></span>|  
|<span data-ttu-id="f1c7b-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f1c7b-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f1c7b-116">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-116">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f1c7b-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f1c7b-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f1c7b-118">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-118">The call timed out.</span></span>|  
|<span data-ttu-id="f1c7b-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f1c7b-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f1c7b-120">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f1c7b-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f1c7b-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f1c7b-122">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-122">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f1c7b-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f1c7b-123">E_FAIL</span></span>|<span data-ttu-id="f1c7b-124">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f1c7b-125">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-125">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f1c7b-126">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="f1c7b-127">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="f1c7b-127">E_OUTOFMEMORY</span></span>|<span data-ttu-id="f1c7b-128">没有足够的内存可用于创建请求的事件对象。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-128">Not enough memory was available to create the requested event object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f1c7b-129">备注</span><span class="sxs-lookup"><span data-stu-id="f1c7b-129">Remarks</span></span>  

 <span data-ttu-id="f1c7b-130">`CreateSemaphore` 镜像同名的 Win32 函数。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-130">`CreateSemaphore` mirrors the Win32 function that has the same name.</span></span> <span data-ttu-id="f1c7b-131">`dwInitial`和 `dwMax` 参数分别对信号量和参数使用相同的语义 `lInitialCount` `lMaximumCount` 。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-131">The `dwInitial` and `dwMax` parameters use the same semantics for the semaphore count as the Win32 `lInitialCount` and `lMaximumCount` parameters, respectively.</span></span> <span data-ttu-id="f1c7b-132">`dwInitial` 必须介于零和 `dwMax` （含）之间。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-132">`dwInitial` must be between zero and `dwMax`, inclusive.</span></span> <span data-ttu-id="f1c7b-133">`dwMax` 必须大于零。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-133">`dwMax` must be greater than zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f1c7b-134">要求</span><span class="sxs-lookup"><span data-stu-id="f1c7b-134">Requirements</span></span>  

 <span data-ttu-id="f1c7b-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f1c7b-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f1c7b-136">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f1c7b-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f1c7b-137">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f1c7b-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f1c7b-138">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f1c7b-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1c7b-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="f1c7b-139">See also</span></span>

- [<span data-ttu-id="f1c7b-140">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="f1c7b-140">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="f1c7b-141">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="f1c7b-141">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="f1c7b-142">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="f1c7b-142">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
