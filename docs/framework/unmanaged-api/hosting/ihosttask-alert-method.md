---
description: 了解详细信息： IHostTask：： Alert 方法
title: IHostTask::Alert 方法
ms.date: 03/30/2017
api_name:
- IHostTask.Alert
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::Alert
helpviewer_keywords:
- IHostTask::Alert method [.NET Framework hosting]
- Alert method, IHostTask interface [.NET Framework hosting]
ms.assetid: 5245d4b5-b6c3-48df-9cb9-8caf059f43fb
topic_type:
- apiref
ms.openlocfilehash: 378552db882aada0b6d0f531a871f2deb02132d0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784699"
---
# <a name="ihosttaskalert-method"></a><span data-ttu-id="b7f28-103">IHostTask::Alert 方法</span><span class="sxs-lookup"><span data-stu-id="b7f28-103">IHostTask::Alert Method</span></span>

<span data-ttu-id="b7f28-104">请求宿主唤醒当前 [IHostTask](ihosttask-interface.md) 实例表示的任务，以便可以中止该任务。</span><span class="sxs-lookup"><span data-stu-id="b7f28-104">Requests that the host wake the task represented by the current [IHostTask](ihosttask-interface.md) instance, so the task can be aborted.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7f28-105">语法</span><span class="sxs-lookup"><span data-stu-id="b7f28-105">Syntax</span></span>  
  
```cpp  
HRESULT Alert ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="b7f28-106">返回值</span><span class="sxs-lookup"><span data-stu-id="b7f28-106">Return Value</span></span>  
  
|<span data-ttu-id="b7f28-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b7f28-107">HRESULT</span></span>|<span data-ttu-id="b7f28-108">说明</span><span class="sxs-lookup"><span data-stu-id="b7f28-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b7f28-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7f28-109">S_OK</span></span>|<span data-ttu-id="b7f28-110">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="b7f28-110">The method returned successfully.</span></span>|  
|<span data-ttu-id="b7f28-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b7f28-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b7f28-112"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="b7f28-112">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b7f28-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b7f28-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b7f28-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="b7f28-114">The call timed out.</span></span>|  
|<span data-ttu-id="b7f28-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b7f28-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b7f28-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="b7f28-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b7f28-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b7f28-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b7f28-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="b7f28-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b7f28-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b7f28-119">E_FAIL</span></span>|<span data-ttu-id="b7f28-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="b7f28-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b7f28-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="b7f28-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b7f28-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="b7f28-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b7f28-123">备注</span><span class="sxs-lookup"><span data-stu-id="b7f28-123">Remarks</span></span>  

 <span data-ttu-id="b7f28-124">`Alert`当 <xref:System.Threading.Thread.Abort%2A?displayProperty=nameWithType> 从用户代码调用时，或当 <xref:System.AppDomain> 与当前的关联关闭时，CLR 将调用方法 <xref:System.Threading.Thread> 。</span><span class="sxs-lookup"><span data-stu-id="b7f28-124">The CLR calls the `Alert` method when <xref:System.Threading.Thread.Abort%2A?displayProperty=nameWithType> is called from user code, or when the <xref:System.AppDomain> associated with the current <xref:System.Threading.Thread> shuts down.</span></span> <span data-ttu-id="b7f28-125">由于调用是异步进行的，因此主机必须立即返回。</span><span class="sxs-lookup"><span data-stu-id="b7f28-125">The host must return immediately, because the call is made asynchronously.</span></span> <span data-ttu-id="b7f28-126">如果主机无法立即对任务发出警报，则必须在下一次进入状态时唤醒该任务。</span><span class="sxs-lookup"><span data-stu-id="b7f28-126">If the host cannot alert the task immediately, it must wake up the next time it enters a state in which it can be alerted.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b7f28-127">`Alert` 仅影响运行时将 WAIT_ALERTABLE [WAIT_OPTION](wait-option-enumeration.md) 值传递到 [联接](ihosttask-join-method.md)等方法的任务。</span><span class="sxs-lookup"><span data-stu-id="b7f28-127">`Alert` affects only those tasks to which the runtime has passed a [WAIT_OPTION](wait-option-enumeration.md) value of WAIT_ALERTABLE to methods such as [Join](ihosttask-join-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7f28-128">要求</span><span class="sxs-lookup"><span data-stu-id="b7f28-128">Requirements</span></span>  

 <span data-ttu-id="b7f28-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b7f28-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7f28-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b7f28-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b7f28-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b7f28-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b7f28-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7f28-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7f28-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="b7f28-133">See also</span></span>

- [<span data-ttu-id="b7f28-134">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="b7f28-134">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="b7f28-135">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="b7f28-135">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="b7f28-136">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="b7f28-136">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="b7f28-137">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="b7f28-137">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
