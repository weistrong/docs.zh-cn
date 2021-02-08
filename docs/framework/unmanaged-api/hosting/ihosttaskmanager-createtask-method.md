---
description: 了解详细信息： IHostTaskManager：： CreateTask 方法
title: IHostTaskManager::CreateTask 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.CreateTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::CreateTask
helpviewer_keywords:
- CreateTask method, IHostTaskManager interface [.NET Framework hosting]
- IHostTaskManager::CreateTask method [.NET Framework hosting]
ms.assetid: a6f8ad36-61e1-42b0-9db2-add575646d18
topic_type:
- apiref
ms.openlocfilehash: c14c80ea9067b0a28e7b9186ea66eb695687bf27
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784569"
---
# <a name="ihosttaskmanagercreatetask-method"></a><span data-ttu-id="b1185-103">IHostTaskManager::CreateTask 方法</span><span class="sxs-lookup"><span data-stu-id="b1185-103">IHostTaskManager::CreateTask Method</span></span>

<span data-ttu-id="b1185-104">请求宿主创建新任务。</span><span class="sxs-lookup"><span data-stu-id="b1185-104">Requests that the host create a new task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1185-105">语法</span><span class="sxs-lookup"><span data-stu-id="b1185-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateTask (  
    [in]  DWORD stacksize,
    [in]  LPTHREAD_START_ROUTINE pStartAddress,  
    [in]  PVOID pParameter,  
    [out] IHostTask **ppTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b1185-106">参数</span><span class="sxs-lookup"><span data-stu-id="b1185-106">Parameters</span></span>  

 `stacksize`  
 <span data-ttu-id="b1185-107">中请求的堆栈的请求大小（以字节为单位），或默认大小为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="b1185-107">[in] The requested size, in bytes, of the requested stack, or 0 (zero) for the default size.</span></span>  
  
 `pStartAddress`  
 <span data-ttu-id="b1185-108">中指向任务要执行的函数的指针。</span><span class="sxs-lookup"><span data-stu-id="b1185-108">[in] A pointer to the function the task is to execute.</span></span>  
  
 `pParameter`  
 <span data-ttu-id="b1185-109">中指向要传递到函数的用户数据的指针; 如果函数不采用任何参数，则为 null。</span><span class="sxs-lookup"><span data-stu-id="b1185-109">[in] A pointer to the user data to be passed to the function, or null if the function takes no parameters.</span></span>  
  
 `ppTask`  
 <span data-ttu-id="b1185-110">弄指向主机创建的 [IHostTask](ihosttask-interface.md) 实例的地址的指针; 如果无法创建任务，则为 null。</span><span class="sxs-lookup"><span data-stu-id="b1185-110">[out] A pointer to the address of an [IHostTask](ihosttask-interface.md) instance created by the host, or null if the task cannot be created.</span></span> <span data-ttu-id="b1185-111">在通过调用 [IHostTask：： Start](ihosttask-start-method.md)显式启动任务之前，任务将保持挂起状态。</span><span class="sxs-lookup"><span data-stu-id="b1185-111">The task remains in a suspended state until it is explicitly started by a call to [IHostTask::Start](ihosttask-start-method.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b1185-112">返回值</span><span class="sxs-lookup"><span data-stu-id="b1185-112">Return Value</span></span>  
  
|<span data-ttu-id="b1185-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b1185-113">HRESULT</span></span>|<span data-ttu-id="b1185-114">说明</span><span class="sxs-lookup"><span data-stu-id="b1185-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b1185-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1185-115">S_OK</span></span>|<span data-ttu-id="b1185-116">`CreateTask` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="b1185-116">`CreateTask` returned successfully.</span></span>|  
|<span data-ttu-id="b1185-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b1185-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b1185-118"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="b1185-118">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b1185-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b1185-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b1185-120">调用超时。</span><span class="sxs-lookup"><span data-stu-id="b1185-120">The call timed out.</span></span>|  
|<span data-ttu-id="b1185-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b1185-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b1185-122">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="b1185-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b1185-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b1185-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b1185-124">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="b1185-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b1185-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b1185-125">E_FAIL</span></span>|<span data-ttu-id="b1185-126">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="b1185-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b1185-127">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="b1185-127">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b1185-128">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="b1185-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="b1185-129">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="b1185-129">E_OUTOFMEMORY</span></span>|<span data-ttu-id="b1185-130">没有足够的内存可用于创建请求的任务。</span><span class="sxs-lookup"><span data-stu-id="b1185-130">Not enough memory was available to create the requested task.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b1185-131">备注</span><span class="sxs-lookup"><span data-stu-id="b1185-131">Remarks</span></span>  

 <span data-ttu-id="b1185-132">CLR 调用 `CreateTask` 来请求宿主创建新任务。</span><span class="sxs-lookup"><span data-stu-id="b1185-132">The CLR calls `CreateTask` to request that the host create a new task.</span></span> <span data-ttu-id="b1185-133">主机返回指向实例的接口指针 `IHostTask` 。</span><span class="sxs-lookup"><span data-stu-id="b1185-133">The host returns an interface pointer to an `IHostTask` instance.</span></span> <span data-ttu-id="b1185-134">返回的任务必须保持挂起状态，直到通过调用显式启动它 `IHostTask::Start` 。</span><span class="sxs-lookup"><span data-stu-id="b1185-134">The returned task must remain suspended until it is explicitly started by a call to `IHostTask::Start`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1185-135">要求</span><span class="sxs-lookup"><span data-stu-id="b1185-135">Requirements</span></span>  

 <span data-ttu-id="b1185-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b1185-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1185-137">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b1185-137">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b1185-138">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b1185-138">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b1185-139">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b1185-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1185-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="b1185-140">See also</span></span>

- [<span data-ttu-id="b1185-141">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="b1185-141">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="b1185-142">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="b1185-142">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="b1185-143">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="b1185-143">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="b1185-144">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="b1185-144">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
