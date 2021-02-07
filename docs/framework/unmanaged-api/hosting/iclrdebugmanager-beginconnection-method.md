---
description: 了解详细信息： ICLRDebugManager：： BeginConnection 方法
title: ICLRDebugManager::BeginConnection 方法
ms.date: 03/30/2017
api_name:
- ICLRDebugManager.BeginConnection
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDebugManager::BeginConnection
helpviewer_keywords:
- ICLRDebugManager::BeginConnection method [.NET Framework hosting]
- BeginConnection method [.NET Framework hosting]
ms.assetid: bdd98146-ff4d-4150-a264-a4c1a32d31f3
topic_type:
- apiref
ms.openlocfilehash: 9b4ee64ad96bddfd5d7d650b657c6691b27d8c69
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746121"
---
# <a name="iclrdebugmanagerbeginconnection-method"></a><span data-ttu-id="f7929-103">ICLRDebugManager::BeginConnection 方法</span><span class="sxs-lookup"><span data-stu-id="f7929-103">ICLRDebugManager::BeginConnection Method</span></span>

<span data-ttu-id="f7929-104">在宿主和调试器之间建立新的连接，以将任务列表与标识符和友好名称关联起来。</span><span class="sxs-lookup"><span data-stu-id="f7929-104">Establishes a new connection between the host and the debugger to associate a list of tasks with an identifier and a friendly name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f7929-105">语法</span><span class="sxs-lookup"><span data-stu-id="f7929-105">Syntax</span></span>  
  
```cpp  
HRESULT BeginConnection (  
    [in] CONNID dwConnectionId,  
    [in, string] wchar_t* szConnectionName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f7929-106">参数</span><span class="sxs-lookup"><span data-stu-id="f7929-106">Parameters</span></span>  

 `dwConnectionId`  
 <span data-ttu-id="f7929-107">中与公共语言运行时的列表关联的标识符 (CLR) 任务。</span><span class="sxs-lookup"><span data-stu-id="f7929-107">[in] An identifier to associate with the list of common language runtime (CLR) tasks.</span></span>  
  
 `szConnectionName`  
 <span data-ttu-id="f7929-108">中与 CLR 任务列表关联的友好名称。</span><span class="sxs-lookup"><span data-stu-id="f7929-108">[in] A friendly name to associate with the list of CLR tasks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f7929-109">返回值</span><span class="sxs-lookup"><span data-stu-id="f7929-109">Return Value</span></span>  
  
|<span data-ttu-id="f7929-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f7929-110">HRESULT</span></span>|<span data-ttu-id="f7929-111">说明</span><span class="sxs-lookup"><span data-stu-id="f7929-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f7929-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7929-112">S_OK</span></span>|<span data-ttu-id="f7929-113">`BeginConnection` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f7929-113">`BeginConnection` returned successfully.</span></span>|  
|<span data-ttu-id="f7929-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f7929-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f7929-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f7929-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f7929-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f7929-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f7929-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f7929-117">The call timed out.</span></span>|  
|<span data-ttu-id="f7929-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f7929-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f7929-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f7929-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f7929-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f7929-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f7929-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="f7929-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f7929-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f7929-122">E_FAIL</span></span>|<span data-ttu-id="f7929-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f7929-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f7929-124">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f7929-124">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f7929-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f7929-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="f7929-126">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f7929-126">E_INVALIDARG</span></span>|<span data-ttu-id="f7929-127">`dwConnectionId` 为零，或 `BeginConnection` 已使用此值调用 `dwConnectionId` ，或为 `szConnectionName` null。</span><span class="sxs-lookup"><span data-stu-id="f7929-127">`dwConnectionId` was zero, or `BeginConnection` was already called using this `dwConnectionId` value, or `szConnectionName` was null.</span></span>|  
|<span data-ttu-id="f7929-128">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="f7929-128">E_OUTOFMEMORY</span></span>|<span data-ttu-id="f7929-129">无法分配足够的内存来保存与此连接关联的任务列表。</span><span class="sxs-lookup"><span data-stu-id="f7929-129">Not enough memory could be allocated to hold the list of tasks associated with this connection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f7929-130">备注</span><span class="sxs-lookup"><span data-stu-id="f7929-130">Remarks</span></span>  

 <span data-ttu-id="f7929-131">[ICLRDebugManager](iclrdebugmanager-interface.md) 提供了三种方法： `BeginConnection` 、 [SetConnectionTasks](iclrdebugmanager-setconnectiontasks-method.md)和 [EndConnection](iclrdebugmanager-endconnection-method.md)，用于将任务列表与标识符和友好名称关联起来。</span><span class="sxs-lookup"><span data-stu-id="f7929-131">[ICLRDebugManager](iclrdebugmanager-interface.md) provides three methods, `BeginConnection`, [SetConnectionTasks](iclrdebugmanager-setconnectiontasks-method.md), and [EndConnection](iclrdebugmanager-endconnection-method.md), for associating task lists with identifiers and friendly names.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="f7929-132">对于每组任务，这三种方法都必须按特定的顺序进行调用。</span><span class="sxs-lookup"><span data-stu-id="f7929-132">These three methods must be called in a specific order for each set of tasks.</span></span> <span data-ttu-id="f7929-133">`BeginConnection` 首先调用以建立新连接。</span><span class="sxs-lookup"><span data-stu-id="f7929-133">`BeginConnection` is called first to establish a new connection.</span></span> <span data-ttu-id="f7929-134">`SetConnectionTasks` 在旁边调用，提供要与该连接相关联的一组任务。</span><span class="sxs-lookup"><span data-stu-id="f7929-134">`SetConnectionTasks` is called next to provide the set of tasks to be associated with that connection.</span></span> <span data-ttu-id="f7929-135">`EndConnection` 最后调用，以删除任务列表与标识符和友好名称之间的关联。但是，可以嵌套不同连接的调用。</span><span class="sxs-lookup"><span data-stu-id="f7929-135">`EndConnection` is called last to remove the association between the task list and the identifier and friendly name.However, calls for different connections can be nested.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f7929-136">要求</span><span class="sxs-lookup"><span data-stu-id="f7929-136">Requirements</span></span>  

 <span data-ttu-id="f7929-137">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f7929-137">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f7929-138">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f7929-138">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f7929-139">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f7929-139">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f7929-140">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f7929-140">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f7929-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="f7929-141">See also</span></span>

- [<span data-ttu-id="f7929-142">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="f7929-142">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="f7929-143">ICLRDebugManager 接口</span><span class="sxs-lookup"><span data-stu-id="f7929-143">ICLRDebugManager Interface</span></span>](iclrdebugmanager-interface.md)
- [<span data-ttu-id="f7929-144">EndConnection 方法</span><span class="sxs-lookup"><span data-stu-id="f7929-144">EndConnection Method</span></span>](iclrdebugmanager-endconnection-method.md)
- [<span data-ttu-id="f7929-145">SetConnectionTasks 方法</span><span class="sxs-lookup"><span data-stu-id="f7929-145">SetConnectionTasks Method</span></span>](iclrdebugmanager-setconnectiontasks-method.md)
- [<span data-ttu-id="f7929-146">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="f7929-146">IHostControl Interface</span></span>](ihostcontrol-interface.md)
