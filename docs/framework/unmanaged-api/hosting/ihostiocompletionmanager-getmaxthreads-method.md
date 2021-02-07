---
description: 了解详细信息： IHostIoCompletionManager：： GetMaxThreads 方法
title: IHostIoCompletionManager::GetMaxThreads 方法
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.GetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::GetMaxThreads
helpviewer_keywords:
- IHostIoCompletionManager::GetMaxThreads method [.NET Framework hosting]
- GetMaxThreads method, IHostIoCompletionManager interface [.NET Framework hosting]
ms.assetid: e7a6cadc-2433-4472-a701-58891abcde45
topic_type:
- apiref
ms.openlocfilehash: 10c36c058f5161330842fa9d71813c4520d4655c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708504"
---
# <a name="ihostiocompletionmanagergetmaxthreads-method"></a><span data-ttu-id="1de53-103">IHostIoCompletionManager::GetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="1de53-103">IHostIoCompletionManager::GetMaxThreads Method</span></span>

<span data-ttu-id="1de53-104">获取主机可为服务 i/o 请求分配的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="1de53-104">Gets the maximum number of threads that the host can allot to service I/O requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1de53-105">语法</span><span class="sxs-lookup"><span data-stu-id="1de53-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMaxThreads (  
    [out] DWORD *pdwMaxIoCompletionThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1de53-106">参数</span><span class="sxs-lookup"><span data-stu-id="1de53-106">Parameters</span></span>  

 `pdwMaxIoCompletionThreads`  
 <span data-ttu-id="1de53-107">弄一个指针，它指向线程池中的最大线程数，主机可以为这些线程分配服务 i/o 请求。</span><span class="sxs-lookup"><span data-stu-id="1de53-107">[out] A pointer to the maximum number of threads in the thread pool that the host can allot to service I/O requests.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1de53-108">返回值</span><span class="sxs-lookup"><span data-stu-id="1de53-108">Return Value</span></span>  
  
|<span data-ttu-id="1de53-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1de53-109">HRESULT</span></span>|<span data-ttu-id="1de53-110">说明</span><span class="sxs-lookup"><span data-stu-id="1de53-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1de53-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="1de53-111">S_OK</span></span>|<span data-ttu-id="1de53-112">`GetMaxThreads` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="1de53-112">`GetMaxThreads` returned successfully.</span></span>|  
|<span data-ttu-id="1de53-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="1de53-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="1de53-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="1de53-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="1de53-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1de53-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="1de53-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="1de53-116">The call timed out.</span></span>|  
|<span data-ttu-id="1de53-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="1de53-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="1de53-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="1de53-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="1de53-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="1de53-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="1de53-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="1de53-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="1de53-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="1de53-121">E_FAIL</span></span>|<span data-ttu-id="1de53-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="1de53-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="1de53-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="1de53-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="1de53-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="1de53-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="1de53-125">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="1de53-125">E_NOTIMPL</span></span>|<span data-ttu-id="1de53-126">宿主不提供的实现 `GetMaxThreads` 。</span><span class="sxs-lookup"><span data-stu-id="1de53-126">The host does not provide an implementation of `GetMaxThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1de53-127">备注</span><span class="sxs-lookup"><span data-stu-id="1de53-127">Remarks</span></span>  

 <span data-ttu-id="1de53-128">出于实现、性能或可伸缩性等原因，主机可能需要对可分配给处理 i/o 请求的线程数进行独占控制。</span><span class="sxs-lookup"><span data-stu-id="1de53-128">A host might want exclusive control over the number of threads that can be allotted to process I/O requests, for reasons such as implementation, performance, or scalability.</span></span> <span data-ttu-id="1de53-129">出于此原因，主机不需要实现 `GetMaxThreads` 。</span><span class="sxs-lookup"><span data-stu-id="1de53-129">For this reason, the host is not required to implement `GetMaxThreads`.</span></span> <span data-ttu-id="1de53-130">在这种情况下，宿主应从此方法返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="1de53-130">In this case, the host should return E_NOTIMPL from this method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1de53-131">要求</span><span class="sxs-lookup"><span data-stu-id="1de53-131">Requirements</span></span>  

 <span data-ttu-id="1de53-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1de53-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1de53-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="1de53-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1de53-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1de53-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1de53-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1de53-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1de53-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="1de53-136">See also</span></span>

- [<span data-ttu-id="1de53-137">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="1de53-137">ICLRIoCompletionManager Interface</span></span>](iclriocompletionmanager-interface.md)
- [<span data-ttu-id="1de53-138">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="1de53-138">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)
