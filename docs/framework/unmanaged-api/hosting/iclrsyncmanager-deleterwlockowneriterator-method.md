---
description: 了解详细信息： ICLRSyncManager：:D eleteRWLockOwnerIterator 方法
title: ICLRSyncManager::DeleteRWLockOwnerIterator 方法
ms.date: 03/30/2017
api_name:
- ICLRSyncManager.DeleteRWLockOwnerIterator
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager::DeleteRWLockOwnerIterator
helpviewer_keywords:
- ICLRSyncManager::DeleteRWLockOwnerIterator method [.NET Framework hosting]
- DeleteRWLockOwnerIterator method [.NET Framework hosting]
ms.assetid: fcfd340a-b7d6-44e4-8167-2c05b789d483
topic_type:
- apiref
ms.openlocfilehash: 7968f326f1ad92fe6e3a0f91749fb7e462e81c04
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789770"
---
# <a name="iclrsyncmanagerdeleterwlockowneriterator-method"></a><span data-ttu-id="62f07-103">ICLRSyncManager::DeleteRWLockOwnerIterator 方法</span><span class="sxs-lookup"><span data-stu-id="62f07-103">ICLRSyncManager::DeleteRWLockOwnerIterator Method</span></span>

<span data-ttu-id="62f07-104">请求公共语言运行时 (CLR) 销毁通过调用 [ICLRSyncManager：： CreateRWLockOwnerIterator](iclrsyncmanager-createrwlockowneriterator-method.md)创建的迭代器。</span><span class="sxs-lookup"><span data-stu-id="62f07-104">Requests that the common language runtime (CLR) destroy an iterator that was created by a call to [ICLRSyncManager::CreateRWLockOwnerIterator](iclrsyncmanager-createrwlockowneriterator-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62f07-105">语法</span><span class="sxs-lookup"><span data-stu-id="62f07-105">Syntax</span></span>  
  
```cpp  
HRESULT DeleteRWLockOwnerIterator (  
    [in] SIZE_T  Iterator  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="62f07-106">参数</span><span class="sxs-lookup"><span data-stu-id="62f07-106">Parameters</span></span>  

 `Iterator`  
 <span data-ttu-id="62f07-107">中使用对的调用创建的迭代器 `CreateRWLockOwnerIterator` 。</span><span class="sxs-lookup"><span data-stu-id="62f07-107">[in] The iterator that was created by using a call to `CreateRWLockOwnerIterator`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="62f07-108">返回值</span><span class="sxs-lookup"><span data-stu-id="62f07-108">Return Value</span></span>  
  
|<span data-ttu-id="62f07-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="62f07-109">HRESULT</span></span>|<span data-ttu-id="62f07-110">说明</span><span class="sxs-lookup"><span data-stu-id="62f07-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="62f07-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="62f07-111">S_OK</span></span>|<span data-ttu-id="62f07-112">`DeleteRWLockOwnerIterator` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="62f07-112">`DeleteRWLockOwnerIterator` returned successfully.</span></span>|  
|<span data-ttu-id="62f07-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="62f07-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="62f07-114">CLR 尚未加载到进程中，或处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="62f07-114">The CLR has not been loaded into a process, or is in a state in which it cannot run managed code or successfully process the call.</span></span>|  
|<span data-ttu-id="62f07-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="62f07-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="62f07-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="62f07-116">The call timed out.</span></span>|  
|<span data-ttu-id="62f07-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="62f07-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="62f07-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="62f07-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="62f07-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="62f07-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="62f07-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="62f07-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="62f07-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="62f07-121">E_FAIL</span></span>|<span data-ttu-id="62f07-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="62f07-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="62f07-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="62f07-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="62f07-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="62f07-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="62f07-125">备注</span><span class="sxs-lookup"><span data-stu-id="62f07-125">Remarks</span></span>  

 <span data-ttu-id="62f07-126">宿主可以调用此方法并 `CreateRWLockOwnerIterator` 确保它的线程实现保持同步。</span><span class="sxs-lookup"><span data-stu-id="62f07-126">The host can call this method and `CreateRWLockOwnerIterator` to ensure that its threading implementation remains synchronized.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="62f07-127">要求</span><span class="sxs-lookup"><span data-stu-id="62f07-127">Requirements</span></span>  

 <span data-ttu-id="62f07-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="62f07-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="62f07-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="62f07-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="62f07-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="62f07-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="62f07-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="62f07-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62f07-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="62f07-132">See also</span></span>

- [<span data-ttu-id="62f07-133">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="62f07-133">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="62f07-134">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="62f07-134">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
