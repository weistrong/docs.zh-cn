---
description: 了解详细信息： IGCHost 接口
title: IGCHost 接口
ms.date: 03/30/2017
api_name:
- IGCHost
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IGCHost
helpviewer_keywords:
- IGCHost interface [.NET Framework hosting]
ms.assetid: 9ad70ffd-6963-4ab2-8c84-3d86c3fb8deb
topic_type:
- apiref
ms.openlocfilehash: 73b1125eb66a38373da85769ab80ddcaf0b955c6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709589"
---
# <a name="igchost-interface"></a><span data-ttu-id="3546f-103">IGCHost 接口</span><span class="sxs-lookup"><span data-stu-id="3546f-103">IGCHost Interface</span></span>

<span data-ttu-id="3546f-104">提供一些方法，用于获取有关垃圾回收系统的信息并控制垃圾回收的某些方面。</span><span class="sxs-lookup"><span data-stu-id="3546f-104">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3546f-105">从 .NET Framework 4.5 开始，你可以使用 [IGCHost2：： SetGCStartupLimitsEx](igchost2-setgcstartuplimitsex-method.md) 方法将垃圾回收段的大小和垃圾回收系统的第0代的最大大小设置为大于 `DWORD` [SetGCStartupLimits](igchost-setgcstartuplimits-method.md) 方法施加的限制的值。</span><span class="sxs-lookup"><span data-stu-id="3546f-105">Starting with the .NET Framework 4.5, you can use the [IGCHost2::SetGCStartupLimitsEx](igchost2-setgcstartuplimitsex-method.md) method to set the size of a garbage collection segment and the maximum size of the garbage collection system's generation 0 to values greater than the `DWORD` limit that is imposed by the [SetGCStartupLimits](igchost-setgcstartuplimits-method.md) method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3546f-106">此接口仅供专家使用。</span><span class="sxs-lookup"><span data-stu-id="3546f-106">This interface is for expert usage only.</span></span> <span data-ttu-id="3546f-107">如果使用不当，可能会影响应用程序的性能。</span><span class="sxs-lookup"><span data-stu-id="3546f-107">It can affect the performance of an application if used improperly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3546f-108">方法</span><span class="sxs-lookup"><span data-stu-id="3546f-108">Methods</span></span>  
  
|<span data-ttu-id="3546f-109">方法</span><span class="sxs-lookup"><span data-stu-id="3546f-109">Method</span></span>|<span data-ttu-id="3546f-110">说明</span><span class="sxs-lookup"><span data-stu-id="3546f-110">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3546f-111">Collect 方法</span><span class="sxs-lookup"><span data-stu-id="3546f-111">Collect Method</span></span>](igchost-collect-method.md)|<span data-ttu-id="3546f-112">为给定的生成强制执行回收，而不考虑当前垃圾回收的状态。</span><span class="sxs-lookup"><span data-stu-id="3546f-112">Forces a collection to occur for the given generation, regardless of the state of the current garbage collection.</span></span>|  
|[<span data-ttu-id="3546f-113">GetStats 方法</span><span class="sxs-lookup"><span data-stu-id="3546f-113">GetStats Method</span></span>](igchost-getstats-method.md)|<span data-ttu-id="3546f-114">获取垃圾收集系统的当前状态的统计信息。</span><span class="sxs-lookup"><span data-stu-id="3546f-114">Gets the statistics for the current state of the garbage collection system.</span></span>|  
|[<span data-ttu-id="3546f-115">GetThreadStats 方法</span><span class="sxs-lookup"><span data-stu-id="3546f-115">GetThreadStats Method</span></span>](igchost-getthreadstats-method.md)|<span data-ttu-id="3546f-116">获取用于垃圾回收的每个线程的统计信息。</span><span class="sxs-lookup"><span data-stu-id="3546f-116">Gets the per-thread statistics for garbage collection.</span></span>|  
|[<span data-ttu-id="3546f-117">SetGCStartupLimits 方法</span><span class="sxs-lookup"><span data-stu-id="3546f-117">SetGCStartupLimits Method</span></span>](igchost-setgcstartuplimits-method.md)|<span data-ttu-id="3546f-118">设置第0代的段大小和最大大小。</span><span class="sxs-lookup"><span data-stu-id="3546f-118">Sets the segment size and the maximum size for generation 0.</span></span>|  
|[<span data-ttu-id="3546f-119">SetVirtualMemLimit 方法</span><span class="sxs-lookup"><span data-stu-id="3546f-119">SetVirtualMemLimit Method</span></span>](igchost-setvirtualmemlimit-method.md)|<span data-ttu-id="3546f-120">设置运行时的虚拟内存的最大大小。</span><span class="sxs-lookup"><span data-stu-id="3546f-120">Sets the maximum size of the runtime's virtual memory.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3546f-121">要求</span><span class="sxs-lookup"><span data-stu-id="3546f-121">Requirements</span></span>  

 <span data-ttu-id="3546f-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3546f-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3546f-123">**标头：** GCHost，GCHost</span><span class="sxs-lookup"><span data-stu-id="3546f-123">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="3546f-124">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3546f-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3546f-125">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3546f-125">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3546f-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="3546f-126">See also</span></span>

- [<span data-ttu-id="3546f-127">承载接口</span><span class="sxs-lookup"><span data-stu-id="3546f-127">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="3546f-128">CorRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="3546f-128">CorRuntimeHost Coclass</span></span>](corruntimehost-coclass.md)
