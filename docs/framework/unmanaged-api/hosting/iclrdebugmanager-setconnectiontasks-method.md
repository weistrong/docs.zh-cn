---
description: 了解详细信息： ICLRDebugManager：： SetConnectionTasks 方法
title: ICLRDebugManager::SetConnectionTasks 方法
ms.date: 03/30/2017
api_name:
- ICLRDebugManager.SetConnectionTasks
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDebugManager::SetConnectionTasks
helpviewer_keywords:
- SetConnectionTasks method [.NET Framework hosting]
- ICLRDebugManager::SetConnectionTasks method [.NET Framework hosting]
ms.assetid: b38bbc9a-872c-41a9-b8c3-ca011d25456a
topic_type:
- apiref
ms.openlocfilehash: 851b3f54cc5599781596314dfb70296a3d86491a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728712"
---
# <a name="iclrdebugmanagersetconnectiontasks-method"></a><span data-ttu-id="10da4-103">ICLRDebugManager::SetConnectionTasks 方法</span><span class="sxs-lookup"><span data-stu-id="10da4-103">ICLRDebugManager::SetConnectionTasks Method</span></span>

<span data-ttu-id="10da4-104">将 [ICLRTask](iclrtask-interface.md) 实例列表与标识符和友好名称关联。</span><span class="sxs-lookup"><span data-stu-id="10da4-104">Associates a list of [ICLRTask](iclrtask-interface.md) instances with an identifier and a friendly name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="10da4-105">语法</span><span class="sxs-lookup"><span data-stu-id="10da4-105">Syntax</span></span>  
  
```cpp  
HRESULT SetConnectionTasks (  
    [in] CONNID id,  
    [in] DWORD dwCount,  
    [in, size_is(dwCount)] ICLRTask **ppCLRTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="10da4-106">参数</span><span class="sxs-lookup"><span data-stu-id="10da4-106">Parameters</span></span>  

 `id`  
 <span data-ttu-id="10da4-107">中要与数组关联的连接的主机特定标识符 `ppCLRTask` 。</span><span class="sxs-lookup"><span data-stu-id="10da4-107">[in] The host-specific identifier for the connection with which to associate the `ppCLRTask` array.</span></span>  
  
 `dwCount`  
 <span data-ttu-id="10da4-108">中的成员数 `ppCLRTask` 。</span><span class="sxs-lookup"><span data-stu-id="10da4-108">[in] The number of members of `ppCLRTask`.</span></span> <span data-ttu-id="10da4-109">此数字必须大于零。</span><span class="sxs-lookup"><span data-stu-id="10da4-109">This number must be greater than zero.</span></span>  
  
 `ppCLRTask`  
 <span data-ttu-id="10da4-110">中与标识的 `ICLRTask` 连接关联的指针数组 `id` 。</span><span class="sxs-lookup"><span data-stu-id="10da4-110">[in] An array of `ICLRTask` pointers to associate with the connection identified by `id`.</span></span> <span data-ttu-id="10da4-111">此数组必须至少包含一个成员。</span><span class="sxs-lookup"><span data-stu-id="10da4-111">This array must contain at least one member.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="10da4-112">返回值</span><span class="sxs-lookup"><span data-stu-id="10da4-112">Return Value</span></span>  
  
|<span data-ttu-id="10da4-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="10da4-113">HRESULT</span></span>|<span data-ttu-id="10da4-114">说明</span><span class="sxs-lookup"><span data-stu-id="10da4-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="10da4-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="10da4-115">S_OK</span></span>|<span data-ttu-id="10da4-116">`SetConnectionTasks` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="10da4-116">`SetConnectionTasks` returned successfully.</span></span>|  
|<span data-ttu-id="10da4-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="10da4-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="10da4-118"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="10da4-118">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="10da4-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="10da4-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="10da4-120">调用超时。</span><span class="sxs-lookup"><span data-stu-id="10da4-120">The call timed out.</span></span>|  
|<span data-ttu-id="10da4-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="10da4-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="10da4-122">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="10da4-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="10da4-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="10da4-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="10da4-124">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="10da4-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="10da4-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="10da4-125">E_FAIL</span></span>|<span data-ttu-id="10da4-126">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="10da4-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="10da4-127">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="10da4-127">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="10da4-128">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="10da4-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="10da4-129">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="10da4-129">E_INVALIDARG</span></span>|<span data-ttu-id="10da4-130">尚未使用的此值调用[BeginConnection](iclrdebugmanager-beginconnection-method.md) ，或者 `id` `dwCount` 或 `id` 为零，或的一个元素 `ppCLRTask` 为空。</span><span class="sxs-lookup"><span data-stu-id="10da4-130">[BeginConnection](iclrdebugmanager-beginconnection-method.md) has not been called using this value of `id`, or `dwCount` or `id` is zero, or one of the elements of `ppCLRTask` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="10da4-131">备注</span><span class="sxs-lookup"><span data-stu-id="10da4-131">Remarks</span></span>  

 <span data-ttu-id="10da4-132">[ICLRDebugManager](iclrdebugmanager-interface.md) 提供了三种方法： `BeginConnection` 、 `SetConnectionTasks` 和 [EndConnection](iclrdebugmanager-endconnection-method.md)，用于将任务列表与标识符和友好名称关联起来。</span><span class="sxs-lookup"><span data-stu-id="10da4-132">[ICLRDebugManager](iclrdebugmanager-interface.md) provides three methods, `BeginConnection`, `SetConnectionTasks`, and [EndConnection](iclrdebugmanager-endconnection-method.md), for associating task lists with identifiers and friendly names.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="10da4-133">对于每组任务，这三种方法都必须按特定的顺序进行调用。</span><span class="sxs-lookup"><span data-stu-id="10da4-133">These three methods must be called in a specific order for each set of tasks.</span></span> <span data-ttu-id="10da4-134">`BeginConnection` 首先调用以建立新连接。</span><span class="sxs-lookup"><span data-stu-id="10da4-134">`BeginConnection` is called first to establish a new connection.</span></span> <span data-ttu-id="10da4-135">`SetConnectionTasks` 在旁边调用，提供要与该连接相关联的一组任务。</span><span class="sxs-lookup"><span data-stu-id="10da4-135">`SetConnectionTasks` is called next to provide the set of tasks to be associated with that connection.</span></span> <span data-ttu-id="10da4-136">`EndConnection` 最后调用，以删除任务列表与标识符和友好名称之间的关联。但是，可以嵌套不同连接的调用。</span><span class="sxs-lookup"><span data-stu-id="10da4-136">`EndConnection` is called last to remove the association between the task list and the identifier and friendly name.However, calls for different connections can be nested.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="10da4-137">要求</span><span class="sxs-lookup"><span data-stu-id="10da4-137">Requirements</span></span>  

 <span data-ttu-id="10da4-138">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="10da4-138">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="10da4-139">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="10da4-139">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="10da4-140">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="10da4-140">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="10da4-141">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="10da4-141">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="10da4-142">请参阅</span><span class="sxs-lookup"><span data-stu-id="10da4-142">See also</span></span>

- [<span data-ttu-id="10da4-143">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="10da4-143">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="10da4-144">ICLRDebugManager 接口</span><span class="sxs-lookup"><span data-stu-id="10da4-144">ICLRDebugManager Interface</span></span>](iclrdebugmanager-interface.md)
- [<span data-ttu-id="10da4-145">BeginConnection 方法</span><span class="sxs-lookup"><span data-stu-id="10da4-145">BeginConnection Method</span></span>](iclrdebugmanager-beginconnection-method.md)
- [<span data-ttu-id="10da4-146">EndConnection 方法</span><span class="sxs-lookup"><span data-stu-id="10da4-146">EndConnection Method</span></span>](iclrdebugmanager-endconnection-method.md)
- [<span data-ttu-id="10da4-147">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="10da4-147">IHostControl Interface</span></span>](ihostcontrol-interface.md)
