---
description: 了解详细信息： IHostTaskManager：： LeaveRuntime 方法
title: IHostTaskManager::LeaveRuntime 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.LeaveRuntime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::LeaveRuntime
helpviewer_keywords:
- IHostTaskManager::LeaveRuntime method [.NET Framework hosting]
- LeaveRuntime method [.NET Framework hosting]
ms.assetid: 43689cc4-e48e-46e5-a22d-bafd768b8759
topic_type:
- apiref
ms.openlocfilehash: 7b18bdc17b9cfd52b68309a07c6714fd1efa66cb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707420"
---
# <a name="ihosttaskmanagerleaveruntime-method"></a><span data-ttu-id="d4bf3-103">IHostTaskManager::LeaveRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="d4bf3-103">IHostTaskManager::LeaveRuntime Method</span></span>

<span data-ttu-id="d4bf3-104">通知宿主当前正在执行的任务即将使公共语言运行时 (CLR) 并输入非托管代码。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-104">Notifies the host that the currently executing task is about to leave the common language runtime (CLR) and enter unmanaged code.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="d4bf3-105">对应的对 [IHostTaskManager：： EnterRuntime](ihosttaskmanager-enterruntime-method.md) 的调用会通知宿主当前正在执行的任务是重新进入托管代码。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-105">A corresponding call to [IHostTaskManager::EnterRuntime](ihosttaskmanager-enterruntime-method.md) notifies the host that the currently executing task is reentering managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d4bf3-106">语法</span><span class="sxs-lookup"><span data-stu-id="d4bf3-106">Syntax</span></span>  
  
```cpp  
HRESULT LeaveRuntime (  
    [in] SIZE_T target  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d4bf3-107">参数</span><span class="sxs-lookup"><span data-stu-id="d4bf3-107">Parameters</span></span>  

 `target`  
 <span data-ttu-id="d4bf3-108">中要调用的非托管函数的映射可移植可执行文件中的地址。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-108">[in] The address within the mapped portable executable file of the unmanaged function to be called.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d4bf3-109">返回值</span><span class="sxs-lookup"><span data-stu-id="d4bf3-109">Return Value</span></span>  
  
|<span data-ttu-id="d4bf3-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d4bf3-110">HRESULT</span></span>|<span data-ttu-id="d4bf3-111">说明</span><span class="sxs-lookup"><span data-stu-id="d4bf3-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d4bf3-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="d4bf3-112">S_OK</span></span>|<span data-ttu-id="d4bf3-113">`LeaveRuntime` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-113">`LeaveRuntime` returned successfully.</span></span>|  
|<span data-ttu-id="d4bf3-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d4bf3-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d4bf3-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d4bf3-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d4bf3-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="d4bf3-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-117">The call timed out.</span></span>|  
|<span data-ttu-id="d4bf3-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="d4bf3-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="d4bf3-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="d4bf3-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="d4bf3-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="d4bf3-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="d4bf3-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d4bf3-122">E_FAIL</span></span>|<span data-ttu-id="d4bf3-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d4bf3-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d4bf3-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="d4bf3-126">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d4bf3-126">E_OUTOFMEMORY</span></span>|<span data-ttu-id="d4bf3-127">没有足够的内存可用来完成请求的分配。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-127">Not enough memory is available to complete the requested allocation.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d4bf3-128">备注</span><span class="sxs-lookup"><span data-stu-id="d4bf3-128">Remarks</span></span>  

 <span data-ttu-id="d4bf3-129">与非托管代码之间的调用序列可以嵌套。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-129">Call sequences to and from unmanaged code can be nested.</span></span> <span data-ttu-id="d4bf3-130">例如，下面的列表描述了一种假设的情况，在这种情况下 `LeaveRuntime` ，对、 [IHostTaskManager：： ReverseEnterRuntime](ihosttaskmanager-reverseenterruntime-method.md)、 [IHostTaskManager：： ReverseLeaveRuntime](ihosttaskmanager-reverseleaveruntime-method.md)的调用序列，并 `IHostTaskManager::EnterRuntime` 允许主机标识嵌套层。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-130">For example, the list below describes a hypothetical situation in which the sequence of calls to `LeaveRuntime`, [IHostTaskManager::ReverseEnterRuntime](ihosttaskmanager-reverseenterruntime-method.md), [IHostTaskManager::ReverseLeaveRuntime](ihosttaskmanager-reverseleaveruntime-method.md), and `IHostTaskManager::EnterRuntime` allows the host to identify the nested layers.</span></span>  
  
|<span data-ttu-id="d4bf3-131">操作</span><span class="sxs-lookup"><span data-stu-id="d4bf3-131">Action</span></span>|<span data-ttu-id="d4bf3-132">对应的方法调用</span><span class="sxs-lookup"><span data-stu-id="d4bf3-132">Corresponding Method Call</span></span>|  
|------------|-------------------------------|  
|<span data-ttu-id="d4bf3-133">托管 Visual Basic 可执行文件使用平台调用来调用以 C 编写的非托管函数。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-133">A managed Visual Basic executable calls an unmanaged function written in C by using platform invoke.</span></span>|`IHostTaskManager::LeaveRuntime`|  
|<span data-ttu-id="d4bf3-134">非托管 C 函数在用 c # 编写的托管 DLL 中调用方法。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-134">The unmanaged C function calls a method in a managed DLL written in C#.</span></span>|`IHostTaskManager::ReverseEnterRuntime`|  
|<span data-ttu-id="d4bf3-135">托管 c # 函数调用另一个用 C 编写的非托管函数，同时也使用平台调用。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-135">The managed C# function calls another unmanaged function written in C, also using platform invoke.</span></span>|`IHostTaskManager::LeaveRuntime`|  
|<span data-ttu-id="d4bf3-136">第二个非托管函数向 c # 函数返回执行。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-136">The second unmanaged function returns execution to the C# function.</span></span>|`IHostTaskManager::EnterRuntime`|  
|<span data-ttu-id="d4bf3-137">C # 函数返回第一个非托管函数的执行。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-137">The C# function returns execution to the first unmanaged function.</span></span>|`IHostTaskManager::ReverseLeaveRuntime`|  
|<span data-ttu-id="d4bf3-138">第一个非托管函数会将执行返回到 Visual Basic 程序。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-138">The first unmanaged function returns execution to the Visual Basic program.</span></span>|`IHostTaskManager::EnterRuntime`|  
  
## <a name="requirements"></a><span data-ttu-id="d4bf3-139">要求</span><span class="sxs-lookup"><span data-stu-id="d4bf3-139">Requirements</span></span>  

 <span data-ttu-id="d4bf3-140">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d4bf3-140">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d4bf3-141">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d4bf3-141">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d4bf3-142">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d4bf3-142">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d4bf3-143">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d4bf3-143">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4bf3-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="d4bf3-144">See also</span></span>

- [<span data-ttu-id="d4bf3-145">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="d4bf3-145">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="d4bf3-146">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="d4bf3-146">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="d4bf3-147">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="d4bf3-147">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="d4bf3-148">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="d4bf3-148">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
