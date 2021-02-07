---
description: 了解详细信息： IHostIoCompletionManager：： SetMaxThreads 方法
title: IHostIoCompletionManager::SetMaxThreads 方法
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.SetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::SetMaxThreads
helpviewer_keywords:
- IHostIoCompletionManager::SetMaxThreads method [.NET Framework hosting]
- SetMaxThreads method, IHostIoCompletionManager interface [.NET Framework hosting]
ms.assetid: ebad4f40-d9f1-4dc6-9b27-a89c9eb3926f
topic_type:
- apiref
ms.openlocfilehash: 6b36523b0b0d6cefba383d324eb23debefd7c41b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708250"
---
# <a name="ihostiocompletionmanagersetmaxthreads-method"></a><span data-ttu-id="60121-103">IHostIoCompletionManager::SetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="60121-103">IHostIoCompletionManager::SetMaxThreads Method</span></span>

<span data-ttu-id="60121-104">设置主机 allots i/o 请求的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="60121-104">Sets the maximum number of threads that the host allots to service I/O requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="60121-105">语法</span><span class="sxs-lookup"><span data-stu-id="60121-105">Syntax</span></span>  
  
```cpp  
HRESULT SetMaxThreads (  
    [in] DWORD dwMaxIoCompletionThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="60121-106">参数</span><span class="sxs-lookup"><span data-stu-id="60121-106">Parameters</span></span>  

 `dwMaxIoCompletionThreads`  
 <span data-ttu-id="60121-107">中为 i/o 请求分配的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="60121-107">[in] The maximum number of threads to allot for I/O requests.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="60121-108">返回值</span><span class="sxs-lookup"><span data-stu-id="60121-108">Return Value</span></span>  
  
|<span data-ttu-id="60121-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="60121-109">HRESULT</span></span>|<span data-ttu-id="60121-110">说明</span><span class="sxs-lookup"><span data-stu-id="60121-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="60121-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="60121-111">S_OK</span></span>|<span data-ttu-id="60121-112">`SetMaxThreads` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="60121-112">`SetMaxThreads` returned successfully.</span></span>|  
|<span data-ttu-id="60121-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="60121-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="60121-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="60121-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="60121-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="60121-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="60121-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="60121-116">The call timed out.</span></span>|  
|<span data-ttu-id="60121-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="60121-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="60121-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="60121-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="60121-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="60121-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="60121-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="60121-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="60121-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60121-121">E_FAIL</span></span>|<span data-ttu-id="60121-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="60121-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="60121-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="60121-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="60121-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="60121-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="60121-125">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="60121-125">E_NOTIMPL</span></span>|<span data-ttu-id="60121-126">宿主不提供的实现 `SetMaxThreads` 。</span><span class="sxs-lookup"><span data-stu-id="60121-126">The host does not provide an implementation of `SetMaxThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="60121-127">备注</span><span class="sxs-lookup"><span data-stu-id="60121-127">Remarks</span></span>  

 <span data-ttu-id="60121-128">`SetMaxThreads` 向 CLR 提供一个机会，用于设置对 i/o 端口上的服务请求可用的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="60121-128">`SetMaxThreads` provides the CLR with an opportunity to set the maximum number of threads that are available to service requests on I/O ports.</span></span> <span data-ttu-id="60121-129">出于实现、性能或可伸缩性等原因，主机可能需要独占控制线程池的大小。</span><span class="sxs-lookup"><span data-stu-id="60121-129">A host might need exclusive control over the size of the thread pool, for reasons such as implementation, performance, or scalability.</span></span> <span data-ttu-id="60121-130">出于此原因，主机不需要实现 `SetMaxThreads` 。</span><span class="sxs-lookup"><span data-stu-id="60121-130">For this reason, the host is not required to implement `SetMaxThreads`.</span></span> <span data-ttu-id="60121-131">在这种情况下，主机应从此方法返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="60121-131">In this case, a host should return E_NOTIMPL from this method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="60121-132">要求</span><span class="sxs-lookup"><span data-stu-id="60121-132">Requirements</span></span>  

 <span data-ttu-id="60121-133">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="60121-133">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="60121-134">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="60121-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="60121-135">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="60121-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="60121-136">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="60121-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60121-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="60121-137">See also</span></span>

- [<span data-ttu-id="60121-138">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="60121-138">ICLRIoCompletionManager Interface</span></span>](iclriocompletionmanager-interface.md)
- [<span data-ttu-id="60121-139">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="60121-139">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)
