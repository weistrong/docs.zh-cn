---
description: 了解详细信息： IHostThreadPoolManager：： GetMaxThreads 方法
title: IHostThreadPoolManager::GetMaxThreads 方法
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.GetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::GetMaxThreads
helpviewer_keywords:
- IHostThreadPoolManager::GetMaxThreads method [.NET Framework hosting]
- GetMaxThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
ms.assetid: db268876-6178-4a81-aca3-318ee7f96001
topic_type:
- apiref
ms.openlocfilehash: e8cae2aa29a50ef58a5b87deba9e275a441d43ef
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728361"
---
# <a name="ihostthreadpoolmanagergetmaxthreads-method"></a><span data-ttu-id="f3367-103">IHostThreadPoolManager::GetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="f3367-103">IHostThreadPoolManager::GetMaxThreads Method</span></span>

<span data-ttu-id="f3367-104">获取主机在线程池中并发维护的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="f3367-104">Gets the maximum number of threads that the host maintains concurrently in the thread pool.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3367-105">语法</span><span class="sxs-lookup"><span data-stu-id="f3367-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMaxThreads (  
    [out] DWORD *pdwMaxWorkerThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f3367-106">参数</span><span class="sxs-lookup"><span data-stu-id="f3367-106">Parameters</span></span>  

 `pdwMaxWorkerThreads`  
 <span data-ttu-id="f3367-107">弄一个指针，它指向主机在线程池中维护的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="f3367-107">[out] A pointer to the maximum number of threads that the host maintains in the thread pool.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f3367-108">返回值</span><span class="sxs-lookup"><span data-stu-id="f3367-108">Return Value</span></span>  
  
|<span data-ttu-id="f3367-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f3367-109">HRESULT</span></span>|<span data-ttu-id="f3367-110">说明</span><span class="sxs-lookup"><span data-stu-id="f3367-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f3367-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3367-111">S_OK</span></span>|<span data-ttu-id="f3367-112">`GetMaxThreads` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f3367-112">`GetMaxThreads` returned successfully.</span></span>|  
|<span data-ttu-id="f3367-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f3367-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f3367-114"> (CLR ( 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f3367-114">The common language runtime (CLR( has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f3367-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f3367-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f3367-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f3367-116">The call timed out.</span></span>|  
|<span data-ttu-id="f3367-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f3367-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f3367-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f3367-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f3367-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f3367-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f3367-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="f3367-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f3367-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3367-121">E_FAIL</span></span>|<span data-ttu-id="f3367-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f3367-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f3367-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f3367-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f3367-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f3367-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="f3367-125">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="f3367-125">E_NOTIMPL</span></span>|<span data-ttu-id="f3367-126">宿主不提供的实现 `GetMaxThreads` 。</span><span class="sxs-lookup"><span data-stu-id="f3367-126">The host does not provide an implementation of `GetMaxThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f3367-127">备注</span><span class="sxs-lookup"><span data-stu-id="f3367-127">Remarks</span></span>  

 <span data-ttu-id="f3367-128">CLR 调用 `GetMaxThreads` 来确定线程池中线程的总数。</span><span class="sxs-lookup"><span data-stu-id="f3367-128">The CLR calls `GetMaxThreads` to determine the total number of threads in the thread pool.</span></span> <span data-ttu-id="f3367-129">[GetAvailableThreads](ihostthreadpoolmanager-getavailablethreads-method.md)方法获取当前未处理工作项的线程数。</span><span class="sxs-lookup"><span data-stu-id="f3367-129">The [GetAvailableThreads](ihostthreadpoolmanager-getavailablethreads-method.md) method gets the number of threads that are not currently processing work items.</span></span> <span data-ttu-id="f3367-130">所有超出参数返回值的请求将 `pdwMaxWorkerThreads` 保持排队状态，直到线程变为可用。</span><span class="sxs-lookup"><span data-stu-id="f3367-130">All requests above the returned value of the `pdwMaxWorkerThreads` parameter remain queued until threads become available.</span></span>  
  
 <span data-ttu-id="f3367-131">如果主机未提供的实现 `GetMaxThreads` ，它应返回 E_NOTIMPL 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="f3367-131">If the host does not provide an implementation of `GetMaxThreads`, it should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f3367-132">要求</span><span class="sxs-lookup"><span data-stu-id="f3367-132">Requirements</span></span>  

 <span data-ttu-id="f3367-133">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f3367-133">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f3367-134">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f3367-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f3367-135">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f3367-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f3367-136">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f3367-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3367-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="f3367-137">See also</span></span>

- <xref:System.Threading.ThreadPool.GetMaxThreads%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="f3367-138">GetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="f3367-138">GetMinThreads Method</span></span>](ihostthreadpoolmanager-getminthreads-method.md)
- [<span data-ttu-id="f3367-139">SetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="f3367-139">SetMaxThreads Method</span></span>](ihostthreadpoolmanager-setmaxthreads-method.md)
- [<span data-ttu-id="f3367-140">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="f3367-140">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
