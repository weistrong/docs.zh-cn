---
description: 了解详细信息： ICLRSyncManager：： CreateRWLockOwnerIterator 方法
title: ICLRSyncManager::CreateRWLockOwnerIterator 方法
ms.date: 03/30/2017
api_name:
- ICLRSyncManager.CreateRWLockOwnerIterator
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager::CreateRWLockOwnerIterator
helpviewer_keywords:
- ICLRSyncManager::CreateRWLockOwnerIterator method [.NET Framework hosting]
- CreateRWLockOwnerIterator method [.NET Framework hosting]
ms.assetid: b5535b87-9439-424e-b9b3-7d6fafb9819e
topic_type:
- apiref
ms.openlocfilehash: c6997b7720586f422cba3c96ca06a93f747d05bc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781774"
---
# <a name="iclrsyncmanagercreaterwlockowneriterator-method"></a><span data-ttu-id="f5a98-103">ICLRSyncManager::CreateRWLockOwnerIterator 方法</span><span class="sxs-lookup"><span data-stu-id="f5a98-103">ICLRSyncManager::CreateRWLockOwnerIterator Method</span></span>

<span data-ttu-id="f5a98-104">请求公共语言运行时 (CLR) 为主机创建迭代器，以用于确定等待读取器-编写器锁的任务集。</span><span class="sxs-lookup"><span data-stu-id="f5a98-104">Requests that the common language runtime (CLR) create an iterator for the host to use to determine the set of tasks waiting on a reader-writer lock.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5a98-105">语法</span><span class="sxs-lookup"><span data-stu-id="f5a98-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateRWLockOwnerIterator (  
    [in]  SIZE_T    cookie,  
    [out] SIZE_T   *pIterator  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f5a98-106">参数</span><span class="sxs-lookup"><span data-stu-id="f5a98-106">Parameters</span></span>  

 `cookie`  
 <span data-ttu-id="f5a98-107">中与所需的读取器锁关联的 cookie。</span><span class="sxs-lookup"><span data-stu-id="f5a98-107">[in] The cookie associated with the desired reader-writer lock.</span></span>  
  
 `pIterator`  
 <span data-ttu-id="f5a98-108">弄指向可传递给 [GetRWLockOwnerNext](iclrsyncmanager-getrwlockownernext-method.md) 和 [DeleteRWLockOwnerIterator](iclrsyncmanager-deleterwlockowneriterator-method.md) 方法的迭代器的指针。</span><span class="sxs-lookup"><span data-stu-id="f5a98-108">[out] A pointer to an iterator that can be passed to the [GetRWLockOwnerNext](iclrsyncmanager-getrwlockownernext-method.md) and [DeleteRWLockOwnerIterator](iclrsyncmanager-deleterwlockowneriterator-method.md) methods.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f5a98-109">返回值</span><span class="sxs-lookup"><span data-stu-id="f5a98-109">Return Value</span></span>  
  
|<span data-ttu-id="f5a98-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f5a98-110">HRESULT</span></span>|<span data-ttu-id="f5a98-111">说明</span><span class="sxs-lookup"><span data-stu-id="f5a98-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f5a98-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5a98-112">S_OK</span></span>|<span data-ttu-id="f5a98-113">`CreateRWLockOwnerIterator` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f5a98-113">`CreateRWLockOwnerIterator` returned successfully.</span></span>|  
|<span data-ttu-id="f5a98-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f5a98-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f5a98-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f5a98-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f5a98-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f5a98-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f5a98-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f5a98-117">The call timed out.</span></span>|  
|<span data-ttu-id="f5a98-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f5a98-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f5a98-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f5a98-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f5a98-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f5a98-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f5a98-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="f5a98-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f5a98-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f5a98-122">E_FAIL</span></span>|<span data-ttu-id="f5a98-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f5a98-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f5a98-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f5a98-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f5a98-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f5a98-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="f5a98-126">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="f5a98-126">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="f5a98-127">`CreateRWLockOwnerIterator` 在当前正在运行托管代码的线程上调用了。</span><span class="sxs-lookup"><span data-stu-id="f5a98-127">`CreateRWLockOwnerIterator` was called on a thread that is currently running managed code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f5a98-128">备注</span><span class="sxs-lookup"><span data-stu-id="f5a98-128">Remarks</span></span>  

 <span data-ttu-id="f5a98-129">`CreateRWLockOwnerIterator` `DeleteRWLockOwnerIterator` 在死锁检测期间，主机通常会调用、和 `GetRWLockOwnerNext` 方法。</span><span class="sxs-lookup"><span data-stu-id="f5a98-129">Hosts typically call the `CreateRWLockOwnerIterator`, `DeleteRWLockOwnerIterator`, and `GetRWLockOwnerNext` methods during deadlock detection.</span></span> <span data-ttu-id="f5a98-130">宿主负责确保读取器-编写器锁仍有效，因为 CLR 不会尝试使读取器-编写器锁保持活动状态。</span><span class="sxs-lookup"><span data-stu-id="f5a98-130">The host is responsible for ensuring that the reader-writer lock is still valid, because the CLR makes no attempt to keep the reader-writer lock alive.</span></span> <span data-ttu-id="f5a98-131">主机可以使用多种策略来确保锁的有效性：</span><span class="sxs-lookup"><span data-stu-id="f5a98-131">Several strategies are available for the host to ensure the validity of the lock:</span></span>  
  
- <span data-ttu-id="f5a98-132">宿主可以在读取器-编写器锁 (（例如 [IHostSemaphore：： ReleaseSemaphore](ihostsemaphore-releasesemaphore-method.md)) ）上阻止释放调用，同时确保此块不会导致死锁。</span><span class="sxs-lookup"><span data-stu-id="f5a98-132">The host can block release calls on the reader-writer lock (for example, [IHostSemaphore::ReleaseSemaphore](ihostsemaphore-releasesemaphore-method.md)) while ensuring that this block does not cause deadlock.</span></span>  
  
- <span data-ttu-id="f5a98-133">宿主可以阻止退出等待与读取器-编写器锁关联的事件对象，并再次确保此块不会导致死锁。</span><span class="sxs-lookup"><span data-stu-id="f5a98-133">The host can block the exit from waiting on the event object associated with the reader-writer lock, again ensuring that this block does not cause deadlock.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f5a98-134">`CreateRWLockOwnerIterator` 只能在当前正在执行非托管代码的线程上调用。</span><span class="sxs-lookup"><span data-stu-id="f5a98-134">`CreateRWLockOwnerIterator` must be called only on threads that are currently executing unmanaged code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f5a98-135">要求</span><span class="sxs-lookup"><span data-stu-id="f5a98-135">Requirements</span></span>  

 <span data-ttu-id="f5a98-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f5a98-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f5a98-137">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f5a98-137">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f5a98-138">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f5a98-138">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f5a98-139">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f5a98-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f5a98-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="f5a98-140">See also</span></span>

- [<span data-ttu-id="f5a98-141">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="f5a98-141">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="f5a98-142">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="f5a98-142">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
