---
description: 了解详细信息： ICLRTask：： RudeAbort 方法
title: ICLRTask::RudeAbort 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.RudeAbort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::RudeAbort
helpviewer_keywords:
- RudeAbort method, ICLRTask interface [.NET Framework hosting]
- ICLRTask::RudeAbort method [.NET Framework hosting]
ms.assetid: b5785468-fcd7-4cc3-8a5d-8796337b53fc
topic_type:
- apiref
ms.openlocfilehash: f152f11ce41018b458ed2cb4df255e486ad54da0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636879"
---
# <a name="iclrtaskrudeabort-method"></a><span data-ttu-id="f2952-103">ICLRTask::RudeAbort 方法</span><span class="sxs-lookup"><span data-stu-id="f2952-103">ICLRTask::RudeAbort Method</span></span>

<span data-ttu-id="f2952-104">指示公共语言运行时 (CLR) 立即和无条件中止当前 [ICLRTask 接口](iclrtask-interface.md) 实例表示的任务。</span><span class="sxs-lookup"><span data-stu-id="f2952-104">Instructs the common language runtime (CLR) to abort the task represented by the current [ICLRTask Interface](iclrtask-interface.md) instance immediately and unconditionally.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2952-105">语法</span><span class="sxs-lookup"><span data-stu-id="f2952-105">Syntax</span></span>  
  
```cpp  
HRESULT RudeAbort ();
```  
  
## <a name="return-value"></a><span data-ttu-id="f2952-106">返回值</span><span class="sxs-lookup"><span data-stu-id="f2952-106">Return Value</span></span>  
  
|<span data-ttu-id="f2952-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f2952-107">HRESULT</span></span>|<span data-ttu-id="f2952-108">说明</span><span class="sxs-lookup"><span data-stu-id="f2952-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f2952-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2952-109">S_OK</span></span>|<span data-ttu-id="f2952-110">`RudeAbort` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f2952-110">`RudeAbort` returned successfully.</span></span>|  
|<span data-ttu-id="f2952-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f2952-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f2952-112">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f2952-112">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f2952-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f2952-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f2952-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f2952-114">The call timed out.</span></span>|  
|<span data-ttu-id="f2952-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f2952-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f2952-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f2952-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f2952-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f2952-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f2952-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="f2952-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f2952-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f2952-119">E_FAIL</span></span>|<span data-ttu-id="f2952-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f2952-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f2952-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f2952-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f2952-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f2952-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f2952-123">备注</span><span class="sxs-lookup"><span data-stu-id="f2952-123">Remarks</span></span>  

 <span data-ttu-id="f2952-124">宿主调用 `RudeAbort` 立即中止任务。</span><span class="sxs-lookup"><span data-stu-id="f2952-124">A host calls `RudeAbort` to abort a task immediately.</span></span> <span data-ttu-id="f2952-125">不保证会执行终结器和异常处理例程。</span><span class="sxs-lookup"><span data-stu-id="f2952-125">Finalizers and exception handling routines are not guaranteed to be executed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2952-126">要求</span><span class="sxs-lookup"><span data-stu-id="f2952-126">Requirements</span></span>  

 <span data-ttu-id="f2952-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f2952-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2952-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f2952-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f2952-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f2952-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f2952-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2952-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2952-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="f2952-131">See also</span></span>

- [<span data-ttu-id="f2952-132">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="f2952-132">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="f2952-133">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="f2952-133">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="f2952-134">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="f2952-134">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="f2952-135">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="f2952-135">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
