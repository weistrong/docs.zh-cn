---
description: 了解详细信息： ICLRTask：： SetTaskIdentifier 方法
title: ICLRTask::SetTaskIdentifier 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.SetTaskIdentifier
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::SetTaskIdentifier
helpviewer_keywords:
- SetTaskIdentifier method [.NET Framework hosting]
- ICLRTask::SetTaskIdentifier method [.NET Framework hosting]
ms.assetid: bdb7f047-1e90-40fc-9e3b-d44a16509073
topic_type:
- apiref
ms.openlocfilehash: e746d8ec96d16f7761dd49ac814ddbed073c2686
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784946"
---
# <a name="iclrtasksettaskidentifier-method"></a><span data-ttu-id="5fb2a-103">ICLRTask::SetTaskIdentifier 方法</span><span class="sxs-lookup"><span data-stu-id="5fb2a-103">ICLRTask::SetTaskIdentifier Method</span></span>

<span data-ttu-id="5fb2a-104">指示公共语言运行时 (CLR) 将指定标识符值与当前 [ICLRTask](iclrtask-interface.md) 实例表示的任务相关联。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-104">Instructs the common language runtime (CLR) to associate the specified identifier value with the task represented by the current [ICLRTask](iclrtask-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5fb2a-105">语法</span><span class="sxs-lookup"><span data-stu-id="5fb2a-105">Syntax</span></span>  
  
```cpp  
HRESULT SetTaskIdentifier (  
    [in] DWORD Asked  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5fb2a-106">参数</span><span class="sxs-lookup"><span data-stu-id="5fb2a-106">Parameters</span></span>  

 `Asked`  
 <span data-ttu-id="5fb2a-107">中与当前实例表示的任务关联的公共语言运行时的唯一标识符 `ICLRTask` 。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-107">[in] The unique identifier for the common language runtime to associate with the task represented by the current `ICLRTask` instance.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5fb2a-108">返回值</span><span class="sxs-lookup"><span data-stu-id="5fb2a-108">Return Value</span></span>  
  
|<span data-ttu-id="5fb2a-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="5fb2a-109">HRESULT</span></span>|<span data-ttu-id="5fb2a-110">说明</span><span class="sxs-lookup"><span data-stu-id="5fb2a-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5fb2a-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="5fb2a-111">S_OK</span></span>|<span data-ttu-id="5fb2a-112">`SetTaskIdentifier` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-112">`SetTaskIdentifier` returned successfully.</span></span>|  
|<span data-ttu-id="5fb2a-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="5fb2a-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="5fb2a-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="5fb2a-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="5fb2a-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="5fb2a-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-116">The call timed out.</span></span>|  
|<span data-ttu-id="5fb2a-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="5fb2a-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="5fb2a-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="5fb2a-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="5fb2a-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="5fb2a-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="5fb2a-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="5fb2a-121">E_FAIL</span></span>|<span data-ttu-id="5fb2a-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="5fb2a-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="5fb2a-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5fb2a-125">备注</span><span class="sxs-lookup"><span data-stu-id="5fb2a-125">Remarks</span></span>  

 <span data-ttu-id="5fb2a-126">宿主可以将标识符与任务相关联，以帮助在调试环境中集成 CLR 和宿主。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-126">The host can associate an identifier with a task to help integrate the CLR and the host in a debugging environment.</span></span> <span data-ttu-id="5fb2a-127">标识符对于 CLR 没有意义。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-127">The identifier has no meaning for the CLR.</span></span> <span data-ttu-id="5fb2a-128">CLR 将其传递到调试器应用程序。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-128">The CLR passes it along to a debugger application.</span></span> <span data-ttu-id="5fb2a-129">调试器可以使用此标识符将 CLR 调用堆栈与宿主调用堆栈相关联，并使其各自的跟踪信息在调试器的用户界面中查看时能够统一。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-129">The debugger can use this identifier to associate a CLR call stack with a host call stack, and enable their respective trace information to be unified when viewed in the debugger's user interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5fb2a-130">要求</span><span class="sxs-lookup"><span data-stu-id="5fb2a-130">Requirements</span></span>  

 <span data-ttu-id="5fb2a-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5fb2a-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5fb2a-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5fb2a-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5fb2a-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5fb2a-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5fb2a-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5fb2a-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5fb2a-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="5fb2a-135">See also</span></span>

- [<span data-ttu-id="5fb2a-136">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="5fb2a-136">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="5fb2a-137">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="5fb2a-137">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="5fb2a-138">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="5fb2a-138">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="5fb2a-139">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="5fb2a-139">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
