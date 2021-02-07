---
description: 了解详细信息： IHostThreadPoolManager：： GetMinThreads 方法
title: IHostThreadPoolManager::GetMinThreads 方法
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.GetMinThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::GetMinThreads
helpviewer_keywords:
- IHostThreadPoolManager::GetMinThreads method [.NET Framework hosting]
- GetMinThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
ms.assetid: dc07232b-b2e4-4dab-87e2-3c955974ab48
topic_type:
- apiref
ms.openlocfilehash: 2ebb828f9bc6230b4b0237aa1494f428a1834139
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728381"
---
# <a name="ihostthreadpoolmanagergetminthreads-method"></a><span data-ttu-id="b72fc-103">IHostThreadPoolManager::GetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="b72fc-103">IHostThreadPoolManager::GetMinThreads Method</span></span>

<span data-ttu-id="b72fc-104">获取主机在线程池中维持的请求的最小空闲线程数。</span><span class="sxs-lookup"><span data-stu-id="b72fc-104">Gets the minimum number of idle threads that the host maintains in the thread pool in anticipation of requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b72fc-105">语法</span><span class="sxs-lookup"><span data-stu-id="b72fc-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMinThreads (  
    [out] DWORD *MinThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b72fc-106">参数</span><span class="sxs-lookup"><span data-stu-id="b72fc-106">Parameters</span></span>  

 `MinThreads`  
 <span data-ttu-id="b72fc-107">弄一个指针，它指向主机当前维护的空闲工作线程的最小数目。</span><span class="sxs-lookup"><span data-stu-id="b72fc-107">[out] A pointer to the minimum number of idle worker threads that the host currently maintains.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b72fc-108">返回值</span><span class="sxs-lookup"><span data-stu-id="b72fc-108">Return Value</span></span>  
  
|<span data-ttu-id="b72fc-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b72fc-109">HRESULT</span></span>|<span data-ttu-id="b72fc-110">说明</span><span class="sxs-lookup"><span data-stu-id="b72fc-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b72fc-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b72fc-111">S_OK</span></span>|<span data-ttu-id="b72fc-112">`GetMinThreads` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="b72fc-112">`GetMinThreads` returned successfully.</span></span>|  
|<span data-ttu-id="b72fc-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b72fc-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b72fc-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="b72fc-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b72fc-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b72fc-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b72fc-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="b72fc-116">The call timed out.</span></span>|  
|<span data-ttu-id="b72fc-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b72fc-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b72fc-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="b72fc-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b72fc-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b72fc-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b72fc-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="b72fc-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b72fc-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b72fc-121">E_FAIL</span></span>|<span data-ttu-id="b72fc-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="b72fc-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b72fc-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="b72fc-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b72fc-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="b72fc-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="b72fc-125">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="b72fc-125">E_NOTIMPL</span></span>|<span data-ttu-id="b72fc-126">宿主不提供的实现 `GetMinThreads` 。</span><span class="sxs-lookup"><span data-stu-id="b72fc-126">The host does not provide an implementation of `GetMinThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b72fc-127">备注</span><span class="sxs-lookup"><span data-stu-id="b72fc-127">Remarks</span></span>  

 <span data-ttu-id="b72fc-128">宿主无需提供的实现 `GetMinThreads` 。</span><span class="sxs-lookup"><span data-stu-id="b72fc-128">The host is not required to provide an implementation of `GetMinThreads`.</span></span> <span data-ttu-id="b72fc-129">在这种情况下，它应返回 E_NOTIMPL 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="b72fc-129">In this case, it should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b72fc-130">要求</span><span class="sxs-lookup"><span data-stu-id="b72fc-130">Requirements</span></span>  

 <span data-ttu-id="b72fc-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b72fc-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b72fc-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b72fc-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b72fc-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b72fc-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b72fc-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b72fc-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b72fc-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="b72fc-135">See also</span></span>

- <xref:System.Threading.ThreadPool.GetMinThreads%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="b72fc-136">GetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="b72fc-136">GetMaxThreads Method</span></span>](ihostthreadpoolmanager-getmaxthreads-method.md)
- [<span data-ttu-id="b72fc-137">SetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="b72fc-137">SetMinThreads Method</span></span>](ihostthreadpoolmanager-setminthreads-method.md)
- [<span data-ttu-id="b72fc-138">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="b72fc-138">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
