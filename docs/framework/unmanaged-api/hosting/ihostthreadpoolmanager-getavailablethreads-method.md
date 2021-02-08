---
description: 了解详细信息： IHostThreadPoolManager：： GetAvailableThreads 方法
title: IHostThreadPoolManager::GetAvailableThreads 方法
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.GetAvailableThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::GetAvailableThreads
helpviewer_keywords:
- GetAvailableThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
- IHostThreadPoolManager::GetAvailableThreads method [.NET Framework hosting]
ms.assetid: 61d26dfd-7f24-4e7d-a63e-b30a463f08e1
topic_type:
- apiref
ms.openlocfilehash: 95ecaa5757442bb384d303c1f8dafa342bd62f5e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789328"
---
# <a name="ihostthreadpoolmanagergetavailablethreads-method"></a><span data-ttu-id="cbb7e-103">IHostThreadPoolManager::GetAvailableThreads 方法</span><span class="sxs-lookup"><span data-stu-id="cbb7e-103">IHostThreadPoolManager::GetAvailableThreads Method</span></span>

<span data-ttu-id="cbb7e-104">获取线程池中当前未处理工作项的线程的数目。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-104">Gets the number of threads in the thread pool that are not currently processing work items.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cbb7e-105">语法</span><span class="sxs-lookup"><span data-stu-id="cbb7e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAvailableThreads (  
    [out] DWORD *pdwAvailableWorkerThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cbb7e-106">参数</span><span class="sxs-lookup"><span data-stu-id="cbb7e-106">Parameters</span></span>  

 `pdwAvailableWorkerThreads`  
 <span data-ttu-id="cbb7e-107">弄一个指针，指向线程池中当前未处理工作项的线程数。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-107">[out] Pointer to the number of threads in the thread pool that are not currently processing work items.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cbb7e-108">返回值</span><span class="sxs-lookup"><span data-stu-id="cbb7e-108">Return Value</span></span>  
  
|<span data-ttu-id="cbb7e-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="cbb7e-109">HRESULT</span></span>|<span data-ttu-id="cbb7e-110">说明</span><span class="sxs-lookup"><span data-stu-id="cbb7e-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="cbb7e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="cbb7e-111">S_OK</span></span>|<span data-ttu-id="cbb7e-112">`GetAvailableThreads` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-112">`GetAvailableThreads` returned successfully.</span></span>|  
|<span data-ttu-id="cbb7e-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="cbb7e-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="cbb7e-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="cbb7e-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="cbb7e-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="cbb7e-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-116">The call timed out.</span></span>|  
|<span data-ttu-id="cbb7e-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="cbb7e-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="cbb7e-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="cbb7e-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="cbb7e-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="cbb7e-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="cbb7e-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cbb7e-121">E_FAIL</span></span>|<span data-ttu-id="cbb7e-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="cbb7e-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="cbb7e-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="cbb7e-125">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="cbb7e-125">E_NOTIMPL</span></span>|<span data-ttu-id="cbb7e-126">宿主不提供的实现 `GetAvailableThreads` 。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-126">The host does not provide an implementation of `GetAvailableThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cbb7e-127">备注</span><span class="sxs-lookup"><span data-stu-id="cbb7e-127">Remarks</span></span>  

 <span data-ttu-id="cbb7e-128">如果主机未提供的实现 `GetAvailableThreads` ，它应返回 E_NOTIMPL 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-128">If the host does not provide an implementation of `GetAvailableThreads`, it should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cbb7e-129">要求</span><span class="sxs-lookup"><span data-stu-id="cbb7e-129">Requirements</span></span>  

 <span data-ttu-id="cbb7e-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cbb7e-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cbb7e-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="cbb7e-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cbb7e-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cbb7e-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cbb7e-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cbb7e-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cbb7e-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="cbb7e-134">See also</span></span>

- <xref:System.Threading.ThreadPool.GetAvailableThreads%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="cbb7e-135">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="cbb7e-135">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)
