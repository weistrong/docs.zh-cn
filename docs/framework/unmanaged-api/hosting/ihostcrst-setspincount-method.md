---
description: 了解详细信息： IHostCrst：： SetSpinCount 方法
title: IHostCrst::SetSpinCount 方法
ms.date: 03/30/2017
api_name:
- IHostCrst.SetSpinCount
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostCrst::SetSpinCount
helpviewer_keywords:
- IHostCrst::SetSpinCount method [.NET Framework hosting]
- SetSpinCount method [.NET Framework hosting]
ms.assetid: 863fc8ce-9b8a-477e-8dd8-75c8544bb43a
topic_type:
- apiref
ms.openlocfilehash: f04281d2649f210e64fc4c0585eb7d52be3e8ec5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721224"
---
# <a name="ihostcrstsetspincount-method"></a><span data-ttu-id="3349e-103">IHostCrst::SetSpinCount 方法</span><span class="sxs-lookup"><span data-stu-id="3349e-103">IHostCrst::SetSpinCount Method</span></span>

<span data-ttu-id="3349e-104">为当前的 [IHostCrst](ihostcrst-interface.md) 实例设置自旋计数。</span><span class="sxs-lookup"><span data-stu-id="3349e-104">Sets the spin count for the current [IHostCrst](ihostcrst-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3349e-105">语法</span><span class="sxs-lookup"><span data-stu-id="3349e-105">Syntax</span></span>  
  
```cpp  
HRESULT SetSpinCount (  
    [in] DWORD dwSpinCount  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3349e-106">参数</span><span class="sxs-lookup"><span data-stu-id="3349e-106">Parameters</span></span>  

 `dwSpinCount`  
 <span data-ttu-id="3349e-107">中当前实例的新自旋计数 `IHostCrst` 。</span><span class="sxs-lookup"><span data-stu-id="3349e-107">[in] The new spin count for the current `IHostCrst` instance.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3349e-108">返回值</span><span class="sxs-lookup"><span data-stu-id="3349e-108">Return Value</span></span>  
  
|<span data-ttu-id="3349e-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3349e-109">HRESULT</span></span>|<span data-ttu-id="3349e-110">说明</span><span class="sxs-lookup"><span data-stu-id="3349e-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3349e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="3349e-111">S_OK</span></span>|<span data-ttu-id="3349e-112">`SetSpinCount` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="3349e-112">`SetSpinCount` returned successfully.</span></span>|  
|<span data-ttu-id="3349e-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3349e-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="3349e-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="3349e-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="3349e-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3349e-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="3349e-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="3349e-116">The call timed out.</span></span>|  
|<span data-ttu-id="3349e-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="3349e-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="3349e-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="3349e-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="3349e-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="3349e-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="3349e-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="3349e-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="3349e-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="3349e-121">E_FAIL</span></span>|<span data-ttu-id="3349e-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="3349e-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="3349e-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="3349e-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="3349e-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="3349e-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3349e-125">备注</span><span class="sxs-lookup"><span data-stu-id="3349e-125">Remarks</span></span>  

 <span data-ttu-id="3349e-126">在多处理器系统上，如果当前实例所表示的临界区 `IHostCrst` 不可用，则调用线程将在 `dwSpinCount` 调用 [IHostSemaphore：： Wait](ihostsemaphore-wait-method.md) 与临界区关联的信号量之前，旋转时间。</span><span class="sxs-lookup"><span data-stu-id="3349e-126">On multi-processor systems, if the critical section represented by the current `IHostCrst` instance is unavailable, a calling thread spins `dwSpinCount` times before calling [IHostSemaphore::Wait](ihostsemaphore-wait-method.md) on a semaphore associated with the critical section.</span></span> <span data-ttu-id="3349e-127">如果在自旋操作期间关键部分变为免费，则调用线程将避免等待操作。</span><span class="sxs-lookup"><span data-stu-id="3349e-127">If the critical section becomes free during the spin operation, the calling thread avoids the wait operation.</span></span>  
  
 <span data-ttu-id="3349e-128">的用法与 `dwSpinCount` Win32 函数中具有相同名称的参数的用法相同 `InitializeCriticalSectionAndSpinCount` 。</span><span class="sxs-lookup"><span data-stu-id="3349e-128">The usage of `dwSpinCount` is identical to the usage of the parameter of the same name in the Win32 `InitializeCriticalSectionAndSpinCount` function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3349e-129">要求</span><span class="sxs-lookup"><span data-stu-id="3349e-129">Requirements</span></span>  

 <span data-ttu-id="3349e-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3349e-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3349e-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="3349e-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3349e-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3349e-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3349e-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3349e-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3349e-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="3349e-134">See also</span></span>

- [<span data-ttu-id="3349e-135">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="3349e-135">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="3349e-136">IHostCrst 接口</span><span class="sxs-lookup"><span data-stu-id="3349e-136">IHostCrst Interface</span></span>](ihostcrst-interface.md)
- [<span data-ttu-id="3349e-137">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="3349e-137">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
