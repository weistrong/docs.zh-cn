---
description: 了解详细信息： ICLRGCManager2 接口
title: ICLRGCManager2 接口
ms.date: 03/30/2017
api_name:
- ICLRGCManager2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRGCManager2
helpviewer_keywords:
- ICLRGCManager2 interface [.NET Framework hosting]
ms.assetid: 4b5ffd7b-9ad7-41cd-9bba-34030ae3da7e
topic_type:
- apiref
ms.openlocfilehash: 455b3a99d10fa43bf325e9f7075d255dd55ae38b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789952"
---
# <a name="iclrgcmanager2-interface"></a><span data-ttu-id="7272b-103">ICLRGCManager2 接口</span><span class="sxs-lookup"><span data-stu-id="7272b-103">ICLRGCManager2 Interface</span></span>

<span data-ttu-id="7272b-104">提供允许主机与公共语言运行时的垃圾回收系统交互的方法。</span><span class="sxs-lookup"><span data-stu-id="7272b-104">Provides methods that allow a host to interact with the common language runtime's garbage collection system.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7272b-105">方法</span><span class="sxs-lookup"><span data-stu-id="7272b-105">Methods</span></span>  
  
|<span data-ttu-id="7272b-106">方法</span><span class="sxs-lookup"><span data-stu-id="7272b-106">Method</span></span>|<span data-ttu-id="7272b-107">说明</span><span class="sxs-lookup"><span data-stu-id="7272b-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7272b-108">SetGCStartupLimitsEx 方法</span><span class="sxs-lookup"><span data-stu-id="7272b-108">SetGCStartupLimitsEx Method</span></span>](iclrgcmanager2-setgcstartuplimitsex-method.md)|<span data-ttu-id="7272b-109">设置垃圾回收段的大小以及垃圾回收系统的第0代的最大大小。</span><span class="sxs-lookup"><span data-stu-id="7272b-109">Sets the size of a garbage collection segment and the maximum size of the garbage collection system's generation 0.</span></span> <span data-ttu-id="7272b-110">启用0代和大于的段大小 `DWORD` 。</span><span class="sxs-lookup"><span data-stu-id="7272b-110">Enables generation 0 and segment sizes larger than `DWORD`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7272b-111">备注</span><span class="sxs-lookup"><span data-stu-id="7272b-111">Remarks</span></span>  

 <span data-ttu-id="7272b-112">此接口继承自 [ICLRGCManager 接口](iclrgcmanager-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="7272b-112">This interface inherits from the [ICLRGCManager Interface](iclrgcmanager-interface.md).</span></span>  
  
 <span data-ttu-id="7272b-113">公共语言运行时 (CLR) 利用托管类型实现其垃圾回收机制 <xref:System.GC> 。</span><span class="sxs-lookup"><span data-stu-id="7272b-113">The common language runtime (CLR) implements its garbage collection mechanism with the managed <xref:System.GC> type.</span></span> <span data-ttu-id="7272b-114">有关垃圾回收系统的详细信息，请参阅 [垃圾](../../../standard/garbage-collection/index.md)回收。</span><span class="sxs-lookup"><span data-stu-id="7272b-114">For more information about the garbage collection system, see [Garbage Collection](../../../standard/garbage-collection/index.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7272b-115">要求</span><span class="sxs-lookup"><span data-stu-id="7272b-115">Requirements</span></span>  

 <span data-ttu-id="7272b-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7272b-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7272b-117">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="7272b-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7272b-118">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7272b-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7272b-119">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7272b-119">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7272b-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="7272b-120">See also</span></span>

- [<span data-ttu-id="7272b-121">自动内存管理</span><span class="sxs-lookup"><span data-stu-id="7272b-121">Automatic Memory Management</span></span>](../../../standard/automatic-memory-management.md)
- [<span data-ttu-id="7272b-122">COR_GC_STATS 结构</span><span class="sxs-lookup"><span data-stu-id="7272b-122">COR_GC_STATS Structure</span></span>](cor-gc-stats-structure.md)
- [<span data-ttu-id="7272b-123">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="7272b-123">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="7272b-124">.NET Framework 4 和 4.5 中添加的 CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="7272b-124">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)
- [<span data-ttu-id="7272b-125">承载接口</span><span class="sxs-lookup"><span data-stu-id="7272b-125">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="7272b-126">承载</span><span class="sxs-lookup"><span data-stu-id="7272b-126">Hosting</span></span>](index.md)
