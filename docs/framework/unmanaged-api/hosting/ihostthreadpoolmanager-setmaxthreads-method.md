---
description: 了解详细信息： IHostThreadPoolManager：： SetMaxThreads 方法
title: IHostThreadPoolManager::SetMaxThreads 方法
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.SetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::SetMaxThreads
helpviewer_keywords:
- IHostThreadPoolManager::SetMaxThreads method [.NET Framework hosting]
- SetMaxThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
ms.assetid: 77cfd347-95c2-4425-b807-4ecc2a8d4578
topic_type:
- apiref
ms.openlocfilehash: 83266b05f639c0aa63e492bca525cbbf09a30775
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671238"
---
# <a name="ihostthreadpoolmanagersetmaxthreads-method"></a><span data-ttu-id="a9f5d-103">IHostThreadPoolManager::SetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="a9f5d-103">IHostThreadPoolManager::SetMaxThreads Method</span></span>

<span data-ttu-id="a9f5d-104">设置宿主可在线程池中维护的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-104">Sets the maximum number of threads that the host can maintain in the thread pool.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9f5d-105">语法</span><span class="sxs-lookup"><span data-stu-id="a9f5d-105">Syntax</span></span>  
  
```cpp  
HRESULT SetMaxThreads (  
    [in] DWORD MaxThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a9f5d-106">参数</span><span class="sxs-lookup"><span data-stu-id="a9f5d-106">Parameters</span></span>  

 `MaxThreads`  
 <span data-ttu-id="a9f5d-107">线程池中辅助线程的最大数目。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-107">The maximum number of worker threads in the thread pool.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a9f5d-108">返回值</span><span class="sxs-lookup"><span data-stu-id="a9f5d-108">Return Value</span></span>  
  
|<span data-ttu-id="a9f5d-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a9f5d-109">HRESULT</span></span>|<span data-ttu-id="a9f5d-110">说明</span><span class="sxs-lookup"><span data-stu-id="a9f5d-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a9f5d-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9f5d-111">S_OK</span></span>|<span data-ttu-id="a9f5d-112">`SetMaxThreads` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-112">`SetMaxThreads` returned successfully.</span></span>|  
|<span data-ttu-id="a9f5d-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a9f5d-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a9f5d-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a9f5d-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a9f5d-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a9f5d-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-116">The call timed out.</span></span>|  
|<span data-ttu-id="a9f5d-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a9f5d-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a9f5d-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a9f5d-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a9f5d-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a9f5d-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a9f5d-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a9f5d-121">E_FAIL</span></span>|<span data-ttu-id="a9f5d-122">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-122">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="a9f5d-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a9f5d-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="a9f5d-125">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a9f5d-125">E_NOTIMPL</span></span>|<span data-ttu-id="a9f5d-126">宿主不提供的实现 `SetMaxThreads` 。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-126">The host does not provide an implementation of `SetMaxThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a9f5d-127">备注</span><span class="sxs-lookup"><span data-stu-id="a9f5d-127">Remarks</span></span>  

 <span data-ttu-id="a9f5d-128">宿主无需允许 CLR 配置线程池的大小。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-128">A host is not required to allow the CLR to configure the size of the thread pool.</span></span> <span data-ttu-id="a9f5d-129">出于实现、性能或可伸缩性等原因，某些主机可能需要对线程池进行独占控制。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-129">Some hosts might want exclusive control over the thread pool, for reasons such as implementation, performance, or scalability.</span></span> <span data-ttu-id="a9f5d-130">在这种情况下，主机应返回 E_NOTIMPL 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-130">In this case, a host should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9f5d-131">要求</span><span class="sxs-lookup"><span data-stu-id="a9f5d-131">Requirements</span></span>  

 <span data-ttu-id="a9f5d-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a9f5d-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9f5d-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a9f5d-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a9f5d-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a9f5d-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a9f5d-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9f5d-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9f5d-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="a9f5d-136">See also</span></span>

- <xref:System.Threading.ThreadPool.SetMaxThreads%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="a9f5d-137">GetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="a9f5d-137">GetMaxThreads Method</span></span>](ihostthreadpoolmanager-getmaxthreads-method.md)
- [<span data-ttu-id="a9f5d-138">SetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="a9f5d-138">SetMinThreads Method</span></span>](ihostthreadpoolmanager-setminthreads-method.md)
- [<span data-ttu-id="a9f5d-139">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="a9f5d-139">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
