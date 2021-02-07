---
description: 了解详细信息： IHostTaskManager：： GetCurrentTask 方法
title: IHostTaskManager::GetCurrentTask 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.GetCurrentTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::GetCurrentTask
helpviewer_keywords:
- GetCurrentTask method, IHostTaskManager interface [.NET Framework hosting]
- IHostTaskManager::GetCurrentTask method [.NET Framework hosting]
ms.assetid: f17bca49-90bd-4dee-a5e1-b9a57ea46f85
topic_type:
- apiref
ms.openlocfilehash: 7e7e516fe4a706fce8b0302f318cfbb164a86eea
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753804"
---
# <a name="ihosttaskmanagergetcurrenttask-method"></a><span data-ttu-id="77c58-103">IHostTaskManager::GetCurrentTask 方法</span><span class="sxs-lookup"><span data-stu-id="77c58-103">IHostTaskManager::GetCurrentTask Method</span></span>

<span data-ttu-id="77c58-104">获取一个接口指针，该指针指向正在进行此调用的操作系统线程上当前正在执行的任务。</span><span class="sxs-lookup"><span data-stu-id="77c58-104">Gets an interface pointer to the task that is currently executing on the operating system thread from which this call is made.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77c58-105">语法</span><span class="sxs-lookup"><span data-stu-id="77c58-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentTask (  
    [out] IHostTask **pTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="77c58-106">参数</span><span class="sxs-lookup"><span data-stu-id="77c58-106">Parameters</span></span>  

 `pTask`  
 <span data-ttu-id="77c58-107">弄指向表示当前正在执行的任务的 [IHostTask](ihosttask-interface.md) 实例的地址的指针; 如果当前没有执行任何任务，则为 null。</span><span class="sxs-lookup"><span data-stu-id="77c58-107">[out] A pointer to the address of an [IHostTask](ihosttask-interface.md) instance that represents the currently executing task, or null, if no task is currently executing.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="77c58-108">返回值</span><span class="sxs-lookup"><span data-stu-id="77c58-108">Return Value</span></span>  
  
|<span data-ttu-id="77c58-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="77c58-109">HRESULT</span></span>|<span data-ttu-id="77c58-110">说明</span><span class="sxs-lookup"><span data-stu-id="77c58-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="77c58-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="77c58-111">S_OK</span></span>|<span data-ttu-id="77c58-112">`GetCurrentTask` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="77c58-112">`GetCurrentTask` returned successfully.</span></span>|  
|<span data-ttu-id="77c58-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="77c58-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="77c58-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="77c58-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="77c58-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="77c58-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="77c58-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="77c58-116">The call timed out.</span></span>|  
|<span data-ttu-id="77c58-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="77c58-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="77c58-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="77c58-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="77c58-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="77c58-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="77c58-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="77c58-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="77c58-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="77c58-121">E_FAIL</span></span>|<span data-ttu-id="77c58-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="77c58-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="77c58-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="77c58-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="77c58-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="77c58-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="77c58-125">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="77c58-125">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="77c58-126">`GetCurrentTask` 在宿主控件之外的操作系统线程上调用了。</span><span class="sxs-lookup"><span data-stu-id="77c58-126">`GetCurrentTask` was called on an operating system thread outside the control of the host.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="77c58-127">备注</span><span class="sxs-lookup"><span data-stu-id="77c58-127">Remarks</span></span>  

 <span data-ttu-id="77c58-128">宿主还可以将参数设置 `pTask` 为 null，以防止它在进入 CLR 时未启动的任务。</span><span class="sxs-lookup"><span data-stu-id="77c58-128">The host can also set the `pTask` parameter to null to prevent a task that it did not initiate from entering the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77c58-129">要求</span><span class="sxs-lookup"><span data-stu-id="77c58-129">Requirements</span></span>  

 <span data-ttu-id="77c58-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="77c58-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77c58-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="77c58-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="77c58-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="77c58-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="77c58-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="77c58-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77c58-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="77c58-134">See also</span></span>

- [<span data-ttu-id="77c58-135">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="77c58-135">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="77c58-136">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="77c58-136">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="77c58-137">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="77c58-137">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="77c58-138">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="77c58-138">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
