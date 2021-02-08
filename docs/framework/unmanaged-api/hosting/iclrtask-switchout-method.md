---
description: 了解详细信息： ICLRTask：： SwitchOut 方法
title: ICLRTask::SwitchOut 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.SwitchOut
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::SwitchOut
helpviewer_keywords:
- ICLRTask::SwitchOut method [.NET Framework hosting]
- SwitchOut method [.NET Framework hosting]
ms.assetid: b6fb168c-b24b-4ecf-a390-2b5ba3317ae6
topic_type:
- apiref
ms.openlocfilehash: 6c491c4d9005fb850c5adecd025730f1ea71f513
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784933"
---
# <a name="iclrtaskswitchout-method"></a><span data-ttu-id="bd8da-103">ICLRTask::SwitchOut 方法</span><span class="sxs-lookup"><span data-stu-id="bd8da-103">ICLRTask::SwitchOut Method</span></span>

<span data-ttu-id="bd8da-104">通知公共语言运行时 (CLR) 当前 [ICLRTask](iclrtask-interface.md) 实例表示的任务不再处于可运行状态。</span><span class="sxs-lookup"><span data-stu-id="bd8da-104">Notifies the common language runtime (CLR) that the task represented by the current [ICLRTask](iclrtask-interface.md) instance is no longer in an operable state.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd8da-105">语法</span><span class="sxs-lookup"><span data-stu-id="bd8da-105">Syntax</span></span>  
  
```cpp  
HRESULT SwitchOut ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="bd8da-106">返回值</span><span class="sxs-lookup"><span data-stu-id="bd8da-106">Return Value</span></span>  
  
|<span data-ttu-id="bd8da-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bd8da-107">HRESULT</span></span>|<span data-ttu-id="bd8da-108">说明</span><span class="sxs-lookup"><span data-stu-id="bd8da-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bd8da-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd8da-109">S_OK</span></span>|<span data-ttu-id="bd8da-110">`SwitchOut` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="bd8da-110">`SwitchOut` returned successfully.</span></span>|  
|<span data-ttu-id="bd8da-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bd8da-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bd8da-112">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="bd8da-112">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bd8da-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bd8da-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bd8da-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="bd8da-114">The call timed out.</span></span>|  
|<span data-ttu-id="bd8da-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bd8da-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bd8da-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="bd8da-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bd8da-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bd8da-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bd8da-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="bd8da-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="bd8da-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bd8da-119">E_FAIL</span></span>|<span data-ttu-id="bd8da-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="bd8da-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bd8da-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="bd8da-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bd8da-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="bd8da-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bd8da-123">备注</span><span class="sxs-lookup"><span data-stu-id="bd8da-123">Remarks</span></span>  

 <span data-ttu-id="bd8da-124">宿主调用 `SwitchOut` 以通知 CLR 它已暂时停止执行当前实例所表示的任务 `ICLRTask` ，并将重新计划任务。</span><span class="sxs-lookup"><span data-stu-id="bd8da-124">A host calls `SwitchOut` to inform the CLR that it has temporarily stopped executing the task that the current `ICLRTask` instance represents, and will reschedule the task.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bd8da-125">要求</span><span class="sxs-lookup"><span data-stu-id="bd8da-125">Requirements</span></span>  

 <span data-ttu-id="bd8da-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bd8da-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bd8da-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="bd8da-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bd8da-128">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bd8da-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bd8da-129">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bd8da-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd8da-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="bd8da-130">See also</span></span>

- [<span data-ttu-id="bd8da-131">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="bd8da-131">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="bd8da-132">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="bd8da-132">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="bd8da-133">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="bd8da-133">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="bd8da-134">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="bd8da-134">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
