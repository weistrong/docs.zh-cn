---
description: 了解详细信息： ICorProfilerModuleEnum 接口
title: ICorProfilerModuleEnum 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerModuleEnum
api_location:
- mscorwks.cll
api_type:
- COM
f1_keywords:
- ICorProfilerModuleEnum
helpviewer_keywords:
- ICorProfilerModuleEnum interface [.NET Framework profiling]
ms.assetid: 24d0fcfa-1601-4fba-868f-da8c97303467
topic_type:
- apiref
ms.openlocfilehash: 195379e9ad6bce94fc93465fe5e1418c5d8c076d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783815"
---
# <a name="icorprofilermoduleenum-interface"></a><span data-ttu-id="496ba-103">ICorProfilerModuleEnum 接口</span><span class="sxs-lookup"><span data-stu-id="496ba-103">ICorProfilerModuleEnum Interface</span></span>

<span data-ttu-id="496ba-104">提供用于按顺序循环访问应用程序或探查器加载的模块集合的方法。</span><span class="sxs-lookup"><span data-stu-id="496ba-104">Provides methods to sequentially iterate through a collection of modules loaded by the application or the profiler.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="496ba-105">方法</span><span class="sxs-lookup"><span data-stu-id="496ba-105">Methods</span></span>  
  
|<span data-ttu-id="496ba-106">方法</span><span class="sxs-lookup"><span data-stu-id="496ba-106">Method</span></span>|<span data-ttu-id="496ba-107">说明</span><span class="sxs-lookup"><span data-stu-id="496ba-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="496ba-108">Clone 方法</span><span class="sxs-lookup"><span data-stu-id="496ba-108">Clone Method</span></span>](icorprofilermoduleenum-clone-method.md)|<span data-ttu-id="496ba-109">获取指向此 `ICorProfilerModuleEnum` 接口副本的接口指针。</span><span class="sxs-lookup"><span data-stu-id="496ba-109">Gets an interface pointer to a copy of this `ICorProfilerModuleEnum` interface.</span></span>|  
|[<span data-ttu-id="496ba-110">GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="496ba-110">GetCount Method</span></span>](icorprofilermoduleenum-getcount-method.md)|<span data-ttu-id="496ba-111">获取已加载到应用程序的托管模块数。</span><span class="sxs-lookup"><span data-stu-id="496ba-111">Gets the number of managed modules that were loaded into the application.</span></span>|  
|[<span data-ttu-id="496ba-112">下一方法</span><span class="sxs-lookup"><span data-stu-id="496ba-112">Next Method</span></span>](icorprofilermoduleenum-next-method.md)|<span data-ttu-id="496ba-113">从对象的序列集合中获取指定的连续模块数，从该序列中的枚举器当前位置开始。</span><span class="sxs-lookup"><span data-stu-id="496ba-113">Gets the specified number of contiguous modules from a sequential collection of objects, starting at the enumerator's current position in the sequence.</span></span>|  
|[<span data-ttu-id="496ba-114">Reset 方法</span><span class="sxs-lookup"><span data-stu-id="496ba-114">Reset Method</span></span>](icorprofilermoduleenum-reset-method.md)|<span data-ttu-id="496ba-115">将枚举器的光标移动到序列的起始位置。</span><span class="sxs-lookup"><span data-stu-id="496ba-115">Moves the enumerator's cursor to the starting position of the sequence.</span></span>|  
|[<span data-ttu-id="496ba-116">Skip 方法</span><span class="sxs-lookup"><span data-stu-id="496ba-116">Skip Method</span></span>](icorprofilermoduleenum-skip-method.md)|<span data-ttu-id="496ba-117">前移枚举器的光标位置，以便跳过指定的元素数。</span><span class="sxs-lookup"><span data-stu-id="496ba-117">Advances the position of the enumerator's cursor so that the specified number of elements are skipped.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="496ba-118">备注</span><span class="sxs-lookup"><span data-stu-id="496ba-118">Remarks</span></span>  

 <span data-ttu-id="496ba-119">`ICorProfilerModuleEnum` 接口是一个枚举器。</span><span class="sxs-lookup"><span data-stu-id="496ba-119">The `ICorProfilerModuleEnum` interface is an enumerator.</span></span> <span data-ttu-id="496ba-120">它可以让数组接收器以其合适的速率从发送器拉取元素。</span><span class="sxs-lookup"><span data-stu-id="496ba-120">It allows the receiver of an array to pull elements from the sender at a rate that is appropriate for the receiver.</span></span> <span data-ttu-id="496ba-121">换而言之，接收器可以显式控制数组元素流，从而避免将大型数组作为方法形参传递方面的相关问题。</span><span class="sxs-lookup"><span data-stu-id="496ba-121">In other words, the receiver is able to explicitly control the flow of array elements, thereby avoiding the problems associated with passing large arrays as method parameters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="496ba-122">要求</span><span class="sxs-lookup"><span data-stu-id="496ba-122">Requirements</span></span>  

 <span data-ttu-id="496ba-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="496ba-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="496ba-124">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="496ba-124">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="496ba-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="496ba-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="496ba-126">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="496ba-126">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="496ba-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="496ba-127">See also</span></span>

- [<span data-ttu-id="496ba-128">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="496ba-128">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="496ba-129">分析接口</span><span class="sxs-lookup"><span data-stu-id="496ba-129">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="496ba-130">EnumModules 方法</span><span class="sxs-lookup"><span data-stu-id="496ba-130">EnumModules Method</span></span>](icorprofilerinfo3-enummodules-method.md)
