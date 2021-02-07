---
description: 了解详细信息： IHostCrst：： Leave 方法
title: IHostCrst::Leave 方法
ms.date: 03/30/2017
api_name:
- IHostCrst.Leave
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostCrst::Leave
helpviewer_keywords:
- IHostCrst::Leave method [.NET Framework hosting]
- Leave method [.NET Framework hosting]
ms.assetid: dfc51d9e-b36d-4dba-9ea1-4f63fa0601ae
topic_type:
- apiref
ms.openlocfilehash: b00e62c7b2683ab6024a7c9b8de4645ceb59fb02
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708835"
---
# <a name="ihostcrstleave-method"></a><span data-ttu-id="08d62-103">IHostCrst::Leave 方法</span><span class="sxs-lookup"><span data-stu-id="08d62-103">IHostCrst::Leave Method</span></span>

<span data-ttu-id="08d62-104">保留 [IHostCrst](ihostcrst-interface.md)的当前实例所表示的临界区。</span><span class="sxs-lookup"><span data-stu-id="08d62-104">Leaves the critical section that is represented by the current instance of [IHostCrst](ihostcrst-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08d62-105">语法</span><span class="sxs-lookup"><span data-stu-id="08d62-105">Syntax</span></span>  
  
```cpp  
HRESULT Leave ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="08d62-106">返回值</span><span class="sxs-lookup"><span data-stu-id="08d62-106">Return Value</span></span>  
  
|<span data-ttu-id="08d62-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="08d62-107">HRESULT</span></span>|<span data-ttu-id="08d62-108">说明</span><span class="sxs-lookup"><span data-stu-id="08d62-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="08d62-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="08d62-109">S_OK</span></span>|<span data-ttu-id="08d62-110">`Leave` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="08d62-110">`Leave` returned successfully.</span></span>|  
|<span data-ttu-id="08d62-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="08d62-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="08d62-112"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="08d62-112">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="08d62-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="08d62-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="08d62-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="08d62-114">The call timed out.</span></span>|  
|<span data-ttu-id="08d62-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="08d62-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="08d62-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="08d62-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="08d62-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="08d62-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="08d62-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="08d62-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="08d62-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="08d62-119">E_FAIL</span></span>|<span data-ttu-id="08d62-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="08d62-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="08d62-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="08d62-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="08d62-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="08d62-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="08d62-123">备注</span><span class="sxs-lookup"><span data-stu-id="08d62-123">Remarks</span></span>  

 <span data-ttu-id="08d62-124">`Leave` 允许 CLR 与宿主的线程实现直接通信，而不是使用相应的 Win32 `LeaveCriticalSection` 函数。</span><span class="sxs-lookup"><span data-stu-id="08d62-124">`Leave` allows the CLR to communicate directly with the host's threading implementation, rather than using the corresponding Win32 `LeaveCriticalSection` function.</span></span> <span data-ttu-id="08d62-125">获取由当前实例表示的临界区所有权的线程必须在 `IHostCrst` `Leave` 每次进入该临界部分时调用一次。</span><span class="sxs-lookup"><span data-stu-id="08d62-125">A thread that takes ownership of the critical section represented by the current `IHostCrst` instance must call `Leave` once for each time it enters that critical section.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08d62-126">要求</span><span class="sxs-lookup"><span data-stu-id="08d62-126">Requirements</span></span>  

 <span data-ttu-id="08d62-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="08d62-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="08d62-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="08d62-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="08d62-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="08d62-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="08d62-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="08d62-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08d62-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="08d62-131">See also</span></span>

- [<span data-ttu-id="08d62-132">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="08d62-132">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="08d62-133">IHostCrst 接口</span><span class="sxs-lookup"><span data-stu-id="08d62-133">IHostCrst Interface</span></span>](ihostcrst-interface.md)
- [<span data-ttu-id="08d62-134">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="08d62-134">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
