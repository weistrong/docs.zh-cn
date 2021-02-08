---
description: 了解详细信息： ICLRGCManager 接口
title: ICLRGCManager 接口
ms.date: 03/30/2017
api_name:
- ICLRGCManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRGCManager
helpviewer_keywords:
- ICLRGCManager interface [.NET Framework hosting]
ms.assetid: fb511c9b-3fe4-41b0-822a-6ba4a079d1f5
topic_type:
- apiref
ms.openlocfilehash: 648b2b131e28da8aabc7028b6d745351cae772fe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789991"
---
# <a name="iclrgcmanager-interface"></a><span data-ttu-id="40061-103">ICLRGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="40061-103">ICLRGCManager Interface</span></span>

<span data-ttu-id="40061-104">提供允许主机与公共语言运行时的垃圾回收系统交互的方法。</span><span class="sxs-lookup"><span data-stu-id="40061-104">Provides methods that allow a host to interact with the common language runtime's garbage collection system.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="40061-105">从 .NET Framework 4.5 开始，你可以使用 [ICLRGCManager2：： SetGCStartupLimitsEx](iclrgcmanager2-setgcstartuplimitsex-method.md) 方法将垃圾回收段的大小和垃圾回收系统的第0代的最大大小设置为大于 `DWORD` [SetGCStartupLimits](iclrgcmanager-setgcstartuplimits-method.md) 方法施加的限制的值。</span><span class="sxs-lookup"><span data-stu-id="40061-105">Starting with the .NET Framework 4.5, you can use the [ICLRGCManager2::SetGCStartupLimitsEx](iclrgcmanager2-setgcstartuplimitsex-method.md) method to set the size of a garbage collection segment and the maximum size of the garbage collection system's generation 0 to values greater than the `DWORD` limit that is imposed by the [SetGCStartupLimits](iclrgcmanager-setgcstartuplimits-method.md) method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="40061-106">方法</span><span class="sxs-lookup"><span data-stu-id="40061-106">Methods</span></span>  
  
|<span data-ttu-id="40061-107">方法</span><span class="sxs-lookup"><span data-stu-id="40061-107">Method</span></span>|<span data-ttu-id="40061-108">说明</span><span class="sxs-lookup"><span data-stu-id="40061-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="40061-109">Collect 方法</span><span class="sxs-lookup"><span data-stu-id="40061-109">Collect Method</span></span>](iclrgcmanager-collect-method.md)|<span data-ttu-id="40061-110">强制执行指定代的垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="40061-110">Forces a garbage collection for the specified generation.</span></span>|  
|[<span data-ttu-id="40061-111">GetStats 方法</span><span class="sxs-lookup"><span data-stu-id="40061-111">GetStats Method</span></span>](iclrgcmanager-getstats-method.md)|<span data-ttu-id="40061-112">获取有关垃圾回收系统的当前统计信息集。</span><span class="sxs-lookup"><span data-stu-id="40061-112">Gets a set of current statistics about the garbage collection system.</span></span>|  
|[<span data-ttu-id="40061-113">SetGCStartupLimits 方法</span><span class="sxs-lookup"><span data-stu-id="40061-113">SetGCStartupLimits Method</span></span>](iclrgcmanager-setgcstartuplimits-method.md)|<span data-ttu-id="40061-114">设置垃圾回收段的大小以及垃圾回收系统的第0代的最大大小。</span><span class="sxs-lookup"><span data-stu-id="40061-114">Sets the size of a garbage collection segment and the maximum size of the garbage collection system's generation 0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="40061-115">备注</span><span class="sxs-lookup"><span data-stu-id="40061-115">Remarks</span></span>  

 <span data-ttu-id="40061-116">公共语言运行时 (CLR) 利用托管类型实现其垃圾回收机制 <xref:System.GC> 。</span><span class="sxs-lookup"><span data-stu-id="40061-116">The common language runtime (CLR) implements its garbage collection mechanism with the managed <xref:System.GC> type.</span></span> <span data-ttu-id="40061-117">有关垃圾回收系统的详细信息，请参阅 [垃圾](../../../standard/garbage-collection/index.md)回收。</span><span class="sxs-lookup"><span data-stu-id="40061-117">For more information about the garbage collection system, see [Garbage Collection](../../../standard/garbage-collection/index.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="40061-118">要求</span><span class="sxs-lookup"><span data-stu-id="40061-118">Requirements</span></span>  

 <span data-ttu-id="40061-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="40061-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="40061-120">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="40061-120">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="40061-121">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="40061-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="40061-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="40061-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="40061-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="40061-123">See also</span></span>

- [<span data-ttu-id="40061-124">自动内存管理</span><span class="sxs-lookup"><span data-stu-id="40061-124">Automatic Memory Management</span></span>](../../../standard/automatic-memory-management.md)
- [<span data-ttu-id="40061-125">COR_GC_STATS 结构</span><span class="sxs-lookup"><span data-stu-id="40061-125">COR_GC_STATS Structure</span></span>](cor-gc-stats-structure.md)
- [<span data-ttu-id="40061-126">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="40061-126">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="40061-127">CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="40061-127">CLR Hosting Interfaces</span></span>](clr-hosting-interfaces.md)
- [<span data-ttu-id="40061-128">承载接口</span><span class="sxs-lookup"><span data-stu-id="40061-128">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="40061-129">承载</span><span class="sxs-lookup"><span data-stu-id="40061-129">Hosting</span></span>](index.md)
