---
description: 了解详细信息： IHostCrst：： TryEnter 方法
title: IHostCrst::TryEnter 方法
ms.date: 03/30/2017
api_name:
- IHostCrst.TryEnter
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostCrst::TryEnter
helpviewer_keywords:
- IHostCrst::TryEnter method [.NET Framework hosting]
- TryEnter method [.NET Framework hosting]
ms.assetid: a922fa98-beab-4f09-a342-cc94fc65687f
topic_type:
- apiref
ms.openlocfilehash: 59c632b7c9edd422e2ceee1e0526a7bb077759a4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708718"
---
# <a name="ihostcrsttryenter-method"></a><span data-ttu-id="7470c-103">IHostCrst::TryEnter 方法</span><span class="sxs-lookup"><span data-stu-id="7470c-103">IHostCrst::TryEnter Method</span></span>

<span data-ttu-id="7470c-104">尝试输入当前 [IHostCrst](ihostcrst-interface.md) 实例所表示的临界区。</span><span class="sxs-lookup"><span data-stu-id="7470c-104">Attempts to enter the critical section represented by the current [IHostCrst](ihostcrst-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7470c-105">语法</span><span class="sxs-lookup"><span data-stu-id="7470c-105">Syntax</span></span>  
  
```cpp  
HRESULT TryEnter (  
    [in]  DWORD  option,  
    [out] BOOL   *pbSucceeded  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7470c-106">参数</span><span class="sxs-lookup"><span data-stu-id="7470c-106">Parameters</span></span>  

 `option`  
 <span data-ttu-id="7470c-107">中 [WAIT_OPTION](wait-option-enumeration.md) 值之一，指示在操作阻止时主机应执行的操作。</span><span class="sxs-lookup"><span data-stu-id="7470c-107">[in] One of the [WAIT_OPTION](wait-option-enumeration.md) values, indicating what action the host should take if the operation blocks.</span></span>  
  
 `pbSucceeded`  
 <span data-ttu-id="7470c-108">[out] `true` 如果可以输入临界区，则为; 否则为。否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="7470c-108">[out] `true` if the critical section can be entered; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7470c-109">返回值</span><span class="sxs-lookup"><span data-stu-id="7470c-109">Return Value</span></span>  
  
|<span data-ttu-id="7470c-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7470c-110">HRESULT</span></span>|<span data-ttu-id="7470c-111">说明</span><span class="sxs-lookup"><span data-stu-id="7470c-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7470c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7470c-112">S_OK</span></span>|<span data-ttu-id="7470c-113">`TryEnter` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="7470c-113">`TryEnter` returned successfully.</span></span>|  
|<span data-ttu-id="7470c-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="7470c-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="7470c-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="7470c-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="7470c-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="7470c-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="7470c-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="7470c-117">The call timed out.</span></span>|  
|<span data-ttu-id="7470c-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="7470c-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="7470c-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="7470c-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="7470c-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="7470c-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="7470c-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="7470c-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="7470c-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="7470c-122">E_FAIL</span></span>|<span data-ttu-id="7470c-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="7470c-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="7470c-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="7470c-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="7470c-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="7470c-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7470c-126">备注</span><span class="sxs-lookup"><span data-stu-id="7470c-126">Remarks</span></span>  

 <span data-ttu-id="7470c-127">`TryEnter` 立即返回并指示调用线程是否进入了临界区。</span><span class="sxs-lookup"><span data-stu-id="7470c-127">`TryEnter` returns immediately and indicates whether the calling thread entered the critical section.</span></span> <span data-ttu-id="7470c-128">此方法对 Wind32 函数进行镜像 `TryEnterCriticalSection` 。</span><span class="sxs-lookup"><span data-stu-id="7470c-128">This method mirrors the Wind32 `TryEnterCriticalSection` function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7470c-129">要求</span><span class="sxs-lookup"><span data-stu-id="7470c-129">Requirements</span></span>  

 <span data-ttu-id="7470c-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7470c-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7470c-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="7470c-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7470c-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7470c-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7470c-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7470c-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7470c-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="7470c-134">See also</span></span>

- [<span data-ttu-id="7470c-135">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="7470c-135">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="7470c-136">IHostCrst 接口</span><span class="sxs-lookup"><span data-stu-id="7470c-136">IHostCrst Interface</span></span>](ihostcrst-interface.md)
- [<span data-ttu-id="7470c-137">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="7470c-137">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
