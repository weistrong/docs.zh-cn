---
description: 了解详细信息： ICLRTask：： GetMemStats 方法
title: ICLRTask::GetMemStats 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.GetMemStats
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::GetMemStats
helpviewer_keywords:
- ICLRTask::GetMemStats method [.NET Framework hosting]
- GetMemStats method [.NET Framework hosting]
ms.assetid: c9e07657-1682-4c30-a336-f8658ff1a125
topic_type:
- apiref
ms.openlocfilehash: ed81e9ced20a43528247d70012077ffd466f9ed1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784971"
---
# <a name="iclrtaskgetmemstats-method"></a><span data-ttu-id="bb2b0-103">ICLRTask::GetMemStats 方法</span><span class="sxs-lookup"><span data-stu-id="bb2b0-103">ICLRTask::GetMemStats Method</span></span>

<span data-ttu-id="bb2b0-104">获取与当前 [ICLRTask](iclrtask-interface.md) 实例表示的任务相关的统计内存使用情况信息。</span><span class="sxs-lookup"><span data-stu-id="bb2b0-104">Gets statistical memory usage information related to the task that the current [ICLRTask](iclrtask-interface.md) instance represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb2b0-105">语法</span><span class="sxs-lookup"><span data-stu-id="bb2b0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMemStats (  
    [out] COR_GC_THREAD_STATS *pMemUsage  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bb2b0-106">参数</span><span class="sxs-lookup"><span data-stu-id="bb2b0-106">Parameters</span></span>  

 `pMemUsage`  
 <span data-ttu-id="bb2b0-107">弄一个指向 [COR_GC_THREAD_STATS](cor-gc-thread-stats-structure.md) 实例的指针，其中包含有关该任务的内存使用情况的详细信息，包括已分配的字节数。</span><span class="sxs-lookup"><span data-stu-id="bb2b0-107">[out] A pointer to a [COR_GC_THREAD_STATS](cor-gc-thread-stats-structure.md) instance that contains details about the memory usage of the task, including the number of bytes allocated.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bb2b0-108">返回值</span><span class="sxs-lookup"><span data-stu-id="bb2b0-108">Return Value</span></span>  
  
|<span data-ttu-id="bb2b0-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bb2b0-109">HRESULT</span></span>|<span data-ttu-id="bb2b0-110">说明</span><span class="sxs-lookup"><span data-stu-id="bb2b0-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bb2b0-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb2b0-111">S_OK</span></span>|<span data-ttu-id="bb2b0-112">`GetMemStats` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="bb2b0-112">`GetMemStats` returned successfully.</span></span>|  
|<span data-ttu-id="bb2b0-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bb2b0-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bb2b0-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="bb2b0-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bb2b0-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bb2b0-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bb2b0-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="bb2b0-116">The call timed out.</span></span>|  
|<span data-ttu-id="bb2b0-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bb2b0-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bb2b0-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="bb2b0-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bb2b0-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bb2b0-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bb2b0-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="bb2b0-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="bb2b0-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bb2b0-121">E_FAIL</span></span>|<span data-ttu-id="bb2b0-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="bb2b0-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bb2b0-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="bb2b0-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bb2b0-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="bb2b0-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bb2b0-125">要求</span><span class="sxs-lookup"><span data-stu-id="bb2b0-125">Requirements</span></span>  

 <span data-ttu-id="bb2b0-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bb2b0-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb2b0-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="bb2b0-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bb2b0-128">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bb2b0-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bb2b0-129">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bb2b0-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb2b0-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="bb2b0-130">See also</span></span>

- [<span data-ttu-id="bb2b0-131">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="bb2b0-131">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="bb2b0-132">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="bb2b0-132">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="bb2b0-133">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="bb2b0-133">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="bb2b0-134">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="bb2b0-134">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
