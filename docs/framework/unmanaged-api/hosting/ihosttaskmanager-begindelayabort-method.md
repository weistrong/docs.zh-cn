---
description: 了解详细信息： IHostTaskManager：： BeginDelayAbort 方法
title: IHostTaskManager::BeginDelayAbort 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.BeginDelayAbort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::BeginDelayAbort
helpviewer_keywords:
- BeginDelayAbort method [.NET Framework hosting]
- IHostTaskManager::BeginDelayAbort method [.NET Framework hosting]
ms.assetid: 75f42a8b-ed68-4718-a030-a179cfba7d72
topic_type:
- apiref
ms.openlocfilehash: f991690af4f7e634c8d845bdbd09f690b4ea3af7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784608"
---
# <a name="ihosttaskmanagerbegindelayabort-method"></a><span data-ttu-id="0d0ac-103">IHostTaskManager::BeginDelayAbort 方法</span><span class="sxs-lookup"><span data-stu-id="0d0ac-103">IHostTaskManager::BeginDelayAbort Method</span></span>

<span data-ttu-id="0d0ac-104">通知宿主托管代码输入的时间段不得中止当前任务。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-104">Notifies the host that managed code is entering a period in which the current task must not be aborted.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0d0ac-105">语法</span><span class="sxs-lookup"><span data-stu-id="0d0ac-105">Syntax</span></span>  
  
```cpp  
HRESULT BeginDelayAbort ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="0d0ac-106">返回值</span><span class="sxs-lookup"><span data-stu-id="0d0ac-106">Return Value</span></span>  
  
|<span data-ttu-id="0d0ac-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0d0ac-107">HRESULT</span></span>|<span data-ttu-id="0d0ac-108">说明</span><span class="sxs-lookup"><span data-stu-id="0d0ac-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0d0ac-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d0ac-109">S_OK</span></span>|<span data-ttu-id="0d0ac-110">`BeginDelayAbort` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-110">`BeginDelayAbort` returned successfully.</span></span>|  
|<span data-ttu-id="0d0ac-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0d0ac-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="0d0ac-112"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-112">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="0d0ac-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0d0ac-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="0d0ac-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-114">The call timed out.</span></span>|  
|<span data-ttu-id="0d0ac-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="0d0ac-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="0d0ac-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="0d0ac-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="0d0ac-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="0d0ac-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="0d0ac-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0d0ac-119">E_FAIL</span></span>|<span data-ttu-id="0d0ac-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="0d0ac-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="0d0ac-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="0d0ac-123">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="0d0ac-123">E_UNEXPECTED</span></span>|<span data-ttu-id="0d0ac-124">`BeginDelayAbort` 已调用，但尚未接收到对 [EndDelayAbort](ihosttaskmanager-enddelayabort-method.md) 的相应调用。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-124">`BeginDelayAbort` has already been called, but the corresponding call to [EndDelayAbort](ihosttaskmanager-enddelayabort-method.md) has not yet been received.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0d0ac-125">备注</span><span class="sxs-lookup"><span data-stu-id="0d0ac-125">Remarks</span></span>  

 <span data-ttu-id="0d0ac-126">在调用之前，主机不得中止当前任务 `EndDelayAbort` 。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-126">The host must not abort the current task until `EndDelayAbort` is called.</span></span> <span data-ttu-id="0d0ac-127">如果在没有干预调用的情况下进行了对的另一次调用 `BeginDelayAbort` `EndDelayAbort` ，主机应从返回 E_UNEXPECTED `BeginDelayAbort` ，而不应采取任何措施。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-127">If another call to `BeginDelayAbort` is made without an intervening call to `EndDelayAbort`, the host should return E_UNEXPECTED from `BeginDelayAbort`, and should take no action.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0d0ac-128">要求</span><span class="sxs-lookup"><span data-stu-id="0d0ac-128">Requirements</span></span>  

 <span data-ttu-id="0d0ac-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0d0ac-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0d0ac-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="0d0ac-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0d0ac-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0d0ac-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0d0ac-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0d0ac-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d0ac-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="0d0ac-133">See also</span></span>

- [<span data-ttu-id="0d0ac-134">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="0d0ac-134">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="0d0ac-135">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="0d0ac-135">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="0d0ac-136">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="0d0ac-136">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
