---
description: 了解详细信息： ICLRGCManager：： GetStats 方法
title: ICLRGCManager::GetStats 方法
ms.date: 03/30/2017
api_name:
- ICLRGCManager.GetStats
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRGCManager::GetStats
helpviewer_keywords:
- GetStats method, ICLRGCManager interface [.NET Framework hosting]
- ICLRGCManager::GetStats method [.NET Framework hosting]
ms.assetid: ce259d1d-cd81-4490-a7a1-0d0ea0804872
topic_type:
- apiref
ms.openlocfilehash: 94b20fb313f06d73f1e7fafd1f46fefb0da3fe95
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790017"
---
# <a name="iclrgcmanagergetstats-method"></a><span data-ttu-id="03ecf-103">ICLRGCManager::GetStats 方法</span><span class="sxs-lookup"><span data-stu-id="03ecf-103">ICLRGCManager::GetStats Method</span></span>

<span data-ttu-id="03ecf-104">获取有关公共语言运行时的垃圾回收系统的当前统计信息集。</span><span class="sxs-lookup"><span data-stu-id="03ecf-104">Gets a set of current statistics about the common language runtime's garbage collection system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="03ecf-105">语法</span><span class="sxs-lookup"><span data-stu-id="03ecf-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStats (  
    [in, out] COR_GC_STATS *pStats  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="03ecf-106">参数</span><span class="sxs-lookup"><span data-stu-id="03ecf-106">Parameters</span></span>  

 `pStats`  
 <span data-ttu-id="03ecf-107">[in，out]一个 [COR_GC_STATS](cor-gc-stats-structure.md) 实例，其中包含请求的统计信息。</span><span class="sxs-lookup"><span data-stu-id="03ecf-107">[in, out] A [COR_GC_STATS](cor-gc-stats-structure.md) instance that contains the requested statistics.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="03ecf-108">返回值</span><span class="sxs-lookup"><span data-stu-id="03ecf-108">Return Value</span></span>  
  
|<span data-ttu-id="03ecf-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="03ecf-109">HRESULT</span></span>|<span data-ttu-id="03ecf-110">说明</span><span class="sxs-lookup"><span data-stu-id="03ecf-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="03ecf-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="03ecf-111">S_OK</span></span>|<span data-ttu-id="03ecf-112">`GetStats` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="03ecf-112">`GetStats` returned successfully.</span></span>|  
|<span data-ttu-id="03ecf-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="03ecf-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="03ecf-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="03ecf-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="03ecf-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="03ecf-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="03ecf-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="03ecf-116">The call timed out.</span></span>|  
|<span data-ttu-id="03ecf-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="03ecf-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="03ecf-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="03ecf-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="03ecf-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="03ecf-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="03ecf-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="03ecf-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="03ecf-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="03ecf-121">E_FAIL</span></span>|<span data-ttu-id="03ecf-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="03ecf-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="03ecf-123">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="03ecf-123">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="03ecf-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="03ecf-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="03ecf-125">备注</span><span class="sxs-lookup"><span data-stu-id="03ecf-125">Remarks</span></span>  

 <span data-ttu-id="03ecf-126">CLR 只计算和返回由的字段指定的统计信息 `Flags` `pStats` 。</span><span class="sxs-lookup"><span data-stu-id="03ecf-126">The CLR calculates and returns only those statistics that are specified by the `Flags` field of `pStats`.</span></span>  
  
 <span data-ttu-id="03ecf-127">将 `Flags` 字段设置为一个或多个 [COR_GC_STAT_TYPES](cor-gc-stat-types-enumeration.md) 枚举的值，以指定要设置 [COR_GC_STATS](cor-gc-stats-structure.md) 结构中的哪些统计信息。</span><span class="sxs-lookup"><span data-stu-id="03ecf-127">Set the `Flags` field to one or more values of the [COR_GC_STAT_TYPES](cor-gc-stat-types-enumeration.md) enumeration to specify which statistics in the [COR_GC_STATS](cor-gc-stats-structure.md) structure are to be set.</span></span>  
  
 <span data-ttu-id="03ecf-128">用法的示例如下所示：</span><span class="sxs-lookup"><span data-stu-id="03ecf-128">An example of the usage is as follows:</span></span>  
  
```cpp  
COR_GC_STATS GCStats;  
GCStats.Flags = COR_GC_COUNTS | COR_GC_MEMORYUSAGE;  
pCLRGCManager->GetStats(&GCStats);  
```  
  
## <a name="requirements"></a><span data-ttu-id="03ecf-129">要求</span><span class="sxs-lookup"><span data-stu-id="03ecf-129">Requirements</span></span>  

 <span data-ttu-id="03ecf-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="03ecf-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="03ecf-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="03ecf-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="03ecf-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="03ecf-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="03ecf-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="03ecf-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03ecf-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="03ecf-134">See also</span></span>

- [<span data-ttu-id="03ecf-135">自动内存管理</span><span class="sxs-lookup"><span data-stu-id="03ecf-135">Automatic Memory Management</span></span>](../../../standard/automatic-memory-management.md)
- [<span data-ttu-id="03ecf-136">COR_GC_STATS 结构</span><span class="sxs-lookup"><span data-stu-id="03ecf-136">COR_GC_STATS Structure</span></span>](cor-gc-stats-structure.md)
- [<span data-ttu-id="03ecf-137">COR_GC_STAT_TYPES 枚举</span><span class="sxs-lookup"><span data-stu-id="03ecf-137">COR_GC_STAT_TYPES Enumeration</span></span>](cor-gc-stat-types-enumeration.md)
- [<span data-ttu-id="03ecf-138">垃圾回收</span><span class="sxs-lookup"><span data-stu-id="03ecf-138">Garbage Collection</span></span>](../../../standard/garbage-collection/index.md)
- [<span data-ttu-id="03ecf-139">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="03ecf-139">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="03ecf-140">ICLRGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="03ecf-140">ICLRGCManager Interface</span></span>](iclrgcmanager-interface.md)
- [<span data-ttu-id="03ecf-141">CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="03ecf-141">CLR Hosting Interfaces</span></span>](clr-hosting-interfaces.md)
- [<span data-ttu-id="03ecf-142">承载接口</span><span class="sxs-lookup"><span data-stu-id="03ecf-142">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="03ecf-143">承载</span><span class="sxs-lookup"><span data-stu-id="03ecf-143">Hosting</span></span>](index.md)
