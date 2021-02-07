---
description: 了解详细信息： IHostThreadPoolManager：： SetMinThreads 方法
title: IHostThreadPoolManager::SetMinThreads 方法
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.SetMinThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::SetMinThreads
helpviewer_keywords:
- SetMinThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
- IHostThreadPoolManager::SetMinThreads method [.NET Framework hosting]
ms.assetid: 10409db9-9fd2-4e4d-b8cd-cf6fec0afaa2
topic_type:
- apiref
ms.openlocfilehash: 00d6bd8212ee95318bbe546da80ca34bff7d1324
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753752"
---
# <a name="ihostthreadpoolmanagersetminthreads-method"></a><span data-ttu-id="6e81e-103">IHostThreadPoolManager::SetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="6e81e-103">IHostThreadPoolManager::SetMinThreads Method</span></span>

<span data-ttu-id="6e81e-104">设置主机在预期请求中必须保持的空闲线程的最小数目。</span><span class="sxs-lookup"><span data-stu-id="6e81e-104">Sets the minimum number of idle threads that the host must maintain in anticipation of requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e81e-105">语法</span><span class="sxs-lookup"><span data-stu-id="6e81e-105">Syntax</span></span>  
  
```cpp  
HRESULT SetMinThreads (  
    [in] DWORD MinThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6e81e-106">参数</span><span class="sxs-lookup"><span data-stu-id="6e81e-106">Parameters</span></span>  

 `MinThreads`  
 <span data-ttu-id="6e81e-107">中宿主必须维持的新最小线程数。</span><span class="sxs-lookup"><span data-stu-id="6e81e-107">[in] The new minimum number of threads that the host must maintain.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6e81e-108">返回值</span><span class="sxs-lookup"><span data-stu-id="6e81e-108">Return Value</span></span>  
  
|<span data-ttu-id="6e81e-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6e81e-109">HRESULT</span></span>|<span data-ttu-id="6e81e-110">说明</span><span class="sxs-lookup"><span data-stu-id="6e81e-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6e81e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e81e-111">S_OK</span></span>|<span data-ttu-id="6e81e-112">`SetMinThreads` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="6e81e-112">`SetMinThreads` returned successfully.</span></span>|  
|<span data-ttu-id="6e81e-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="6e81e-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="6e81e-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="6e81e-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="6e81e-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6e81e-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="6e81e-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="6e81e-116">The call timed out.</span></span>|  
|<span data-ttu-id="6e81e-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="6e81e-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="6e81e-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="6e81e-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="6e81e-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="6e81e-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="6e81e-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="6e81e-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="6e81e-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="6e81e-121">E_FAIL</span></span>|<span data-ttu-id="6e81e-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="6e81e-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="6e81e-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="6e81e-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="6e81e-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="6e81e-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="6e81e-125">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="6e81e-125">E_NOTIMPL</span></span>|<span data-ttu-id="6e81e-126">宿主不提供的实现 `SetMinThreads` 。</span><span class="sxs-lookup"><span data-stu-id="6e81e-126">The host does not provide an implementation of `SetMinThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6e81e-127">备注</span><span class="sxs-lookup"><span data-stu-id="6e81e-127">Remarks</span></span>  

 <span data-ttu-id="6e81e-128">不要求主机提供的实现 `SetMinThreads` 。</span><span class="sxs-lookup"><span data-stu-id="6e81e-128">A host is not required to provide an implementation of `SetMinThreads`.</span></span> <span data-ttu-id="6e81e-129">在这种情况下，它应返回 E_NOTIMPL 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="6e81e-129">In this case, it should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6e81e-130">要求</span><span class="sxs-lookup"><span data-stu-id="6e81e-130">Requirements</span></span>  

 <span data-ttu-id="6e81e-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6e81e-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6e81e-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6e81e-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6e81e-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6e81e-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6e81e-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6e81e-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e81e-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="6e81e-135">See also</span></span>

- <xref:System.Threading.ThreadPool.SetMinThreads%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="6e81e-136">GetMinThreads 方法</span><span class="sxs-lookup"><span data-stu-id="6e81e-136">GetMinThreads Method</span></span>](ihostthreadpoolmanager-getminthreads-method.md)
- [<span data-ttu-id="6e81e-137">SetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="6e81e-137">SetMaxThreads Method</span></span>](ihostthreadpoolmanager-setmaxthreads-method.md)
- [<span data-ttu-id="6e81e-138">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="6e81e-138">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
