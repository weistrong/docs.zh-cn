---
description: 了解详细信息： ICLRSyncManager：： GetRWLockOwnerNext 方法
title: ICLRSyncManager::GetRWLockOwnerNext 方法
ms.date: 03/30/2017
api_name:
- ICLRSyncManager.GetRWLockOwnerNext
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager::GetRWLockOwnerNext
helpviewer_keywords:
- ICLRSyncManager::GetRWLockOwnerNext method [.NET Framework hosting]
- GetRWLockOwnerNext method [.NET Framework hosting]
ms.assetid: 0e025b6a-280e-40a2-a2d0-b15f58777b81
topic_type:
- apiref
ms.openlocfilehash: f49bdd5065ac896147967c0a013347ab39ce1eff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784985"
---
# <a name="iclrsyncmanagergetrwlockownernext-method"></a><span data-ttu-id="9ca4b-103">ICLRSyncManager::GetRWLockOwnerNext 方法</span><span class="sxs-lookup"><span data-stu-id="9ca4b-103">ICLRSyncManager::GetRWLockOwnerNext Method</span></span>

<span data-ttu-id="9ca4b-104">获取在当前读取器-编写器锁上被阻止的下一个 [IHostTask](ihosttask-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-104">Gets the next [IHostTask](ihosttask-interface.md) instance that is blocked on the current reader-writer lock.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ca4b-105">语法</span><span class="sxs-lookup"><span data-stu-id="9ca4b-105">Syntax</span></span>  
  
```cpp
HRESULT GetRWLockOwnerNext (  
    [in] SIZE_T       Iterator,  
    [out] IHostTask  *ppOwnerHostTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9ca4b-106">参数</span><span class="sxs-lookup"><span data-stu-id="9ca4b-106">Parameters</span></span>  

 `Iterator`  
 <span data-ttu-id="9ca4b-107">中使用对 [CreateRWLockOwnerIterator](iclrsyncmanager-createrwlockowneriterator-method.md)的调用创建的迭代器。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-107">[in] The iterator that was created by using a call to [CreateRWLockOwnerIterator](iclrsyncmanager-createrwlockowneriterator-method.md).</span></span>  
  
 `ppOwnerHostTask`  
 <span data-ttu-id="9ca4b-108">弄指向下一个正在 `IHostTask` 等待锁定的的指针; 如果没有正在等待的任务，则为 null。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-108">[out] A pointer to the next `IHostTask` that is waiting on the lock, or null if no task is waiting.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9ca4b-109">返回值</span><span class="sxs-lookup"><span data-stu-id="9ca4b-109">Return Value</span></span>  
  
|<span data-ttu-id="9ca4b-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9ca4b-110">HRESULT</span></span>|<span data-ttu-id="9ca4b-111">说明</span><span class="sxs-lookup"><span data-stu-id="9ca4b-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9ca4b-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ca4b-112">S_OK</span></span>|<span data-ttu-id="9ca4b-113">`GetRWLockOwnerNext` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-113">`GetRWLockOwnerNext` returned successfully.</span></span>|  
|<span data-ttu-id="9ca4b-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="9ca4b-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="9ca4b-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="9ca4b-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="9ca4b-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="9ca4b-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-117">The call timed out.</span></span>|  
|<span data-ttu-id="9ca4b-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="9ca4b-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="9ca4b-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="9ca4b-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="9ca4b-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="9ca4b-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="9ca4b-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="9ca4b-122">E_FAIL</span></span>|<span data-ttu-id="9ca4b-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="9ca4b-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="9ca4b-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9ca4b-126">备注</span><span class="sxs-lookup"><span data-stu-id="9ca4b-126">Remarks</span></span>  

 <span data-ttu-id="9ca4b-127">如果 `ppOwnerHostTask` 设置为 null，则迭代已终止，主机应调用 [DeleteRWLockOwnerIterator](iclrsyncmanager-deleterwlockowneriterator-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-127">If `ppOwnerHostTask` is set to null, the iteration has terminated, and the host should call the [DeleteRWLockOwnerIterator](iclrsyncmanager-deleterwlockowneriterator-method.md) method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="9ca4b-128">CLR 对指向的调用，以 `AddRef` `IHostTask` `ppOwnerHostTask` 防止该任务在宿主保存指针时退出。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-128">The CLR calls `AddRef` on the `IHostTask` to which `ppOwnerHostTask` points to prevent this task from exiting while the host holds the pointer.</span></span> <span data-ttu-id="9ca4b-129">宿主必须调用 `Release` ，以在完成后减小引用计数。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-129">The host must call `Release` to decrement the reference count when it is finished.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ca4b-130">要求</span><span class="sxs-lookup"><span data-stu-id="9ca4b-130">Requirements</span></span>  

 <span data-ttu-id="9ca4b-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9ca4b-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ca4b-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9ca4b-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9ca4b-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9ca4b-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9ca4b-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ca4b-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ca4b-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="9ca4b-135">See also</span></span>

- [<span data-ttu-id="9ca4b-136">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="9ca4b-136">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="9ca4b-137">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="9ca4b-137">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
