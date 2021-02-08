---
description: 了解详细信息： IHostTaskManager：： BeginThreadAffinity 方法
title: IHostTaskManager::BeginThreadAffinity 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.BeginThreadAffinity
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::BeginThreadAffinity
helpviewer_keywords:
- IHostTaskManager::BeginThreadAffinity method [.NET Framework hosting]
- BeginThreadAffinity method [.NET Framework hosting]
ms.assetid: fea3ab88-ce41-4c5a-847b-bb78cd748da6
topic_type:
- apiref
ms.openlocfilehash: 15ee917f5c81ee605c0cb4df3180041797c18daf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784595"
---
# <a name="ihosttaskmanagerbeginthreadaffinity-method"></a><span data-ttu-id="1738f-103">IHostTaskManager::BeginThreadAffinity 方法</span><span class="sxs-lookup"><span data-stu-id="1738f-103">IHostTaskManager::BeginThreadAffinity Method</span></span>

<span data-ttu-id="1738f-104">通知宿主托管代码正在输入一个时间段，在此期间，不能将当前任务移动到另一个操作系统线程。</span><span class="sxs-lookup"><span data-stu-id="1738f-104">Notifies the host that managed code is entering a period in which the current task must not be moved to another operating system thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1738f-105">语法</span><span class="sxs-lookup"><span data-stu-id="1738f-105">Syntax</span></span>  
  
```cpp  
HRESULT BeginThreadAffinity ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="1738f-106">返回值</span><span class="sxs-lookup"><span data-stu-id="1738f-106">Return Value</span></span>  
  
|<span data-ttu-id="1738f-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1738f-107">HRESULT</span></span>|<span data-ttu-id="1738f-108">说明</span><span class="sxs-lookup"><span data-stu-id="1738f-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1738f-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="1738f-109">S_OK</span></span>|<span data-ttu-id="1738f-110">`BeginThreadAffinity` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="1738f-110">`BeginThreadAffinity` returned successfully.</span></span>|  
|<span data-ttu-id="1738f-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="1738f-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="1738f-112"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="1738f-112">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="1738f-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1738f-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="1738f-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="1738f-114">The call timed out.</span></span>|  
|<span data-ttu-id="1738f-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="1738f-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="1738f-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="1738f-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="1738f-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="1738f-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="1738f-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="1738f-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="1738f-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="1738f-119">E_FAIL</span></span>|<span data-ttu-id="1738f-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="1738f-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="1738f-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="1738f-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="1738f-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="1738f-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1738f-123">备注</span><span class="sxs-lookup"><span data-stu-id="1738f-123">Remarks</span></span>  

 <span data-ttu-id="1738f-124">CLR 通常在对的 `IHostTaskManager::BeginThreadAffinity` 调用的上下文中调用 <xref:System.Threading.Thread.BeginThreadAffinity%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="1738f-124">The CLR typically calls `IHostTaskManager::BeginThreadAffinity` in the context of a call to <xref:System.Threading.Thread.BeginThreadAffinity%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="1738f-125">在对 [IHostTaskManager：： EndThreadAffinity](ihosttaskmanager-endthreadaffinity-method.md)进行相应的调用之前，不能重新计划当前任务。</span><span class="sxs-lookup"><span data-stu-id="1738f-125">The current task must not be rescheduled until a corresponding call is made to [IHostTaskManager::EndThreadAffinity](ihosttaskmanager-endthreadaffinity-method.md).</span></span> <span data-ttu-id="1738f-126">可以切换出任务，但当它们切换回时，必须将它们分配到从中进行切换的相同操作系统线程。对的嵌套调用 `BeginThreadAffinity` 不起作用，因为调用指的是当前任务。</span><span class="sxs-lookup"><span data-stu-id="1738f-126">Tasks can be switched out, but when they are switched back in, they must be assigned to the same operating system thread from which they were switched out. Nested calls to `BeginThreadAffinity` have no effect, because the call refers to the current task.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1738f-127">要求</span><span class="sxs-lookup"><span data-stu-id="1738f-127">Requirements</span></span>  

 <span data-ttu-id="1738f-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1738f-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1738f-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="1738f-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1738f-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1738f-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1738f-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1738f-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1738f-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="1738f-132">See also</span></span>

- [<span data-ttu-id="1738f-133">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="1738f-133">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="1738f-134">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="1738f-134">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="1738f-135">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="1738f-135">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="1738f-136">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="1738f-136">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
