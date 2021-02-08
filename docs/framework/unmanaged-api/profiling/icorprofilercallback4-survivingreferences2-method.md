---
description: 了解详细信息： ICorProfilerCallback4：： SurvivingReferences2 方法
title: ICorProfilerCallback4::SurvivingReferences2 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback4.SurvivingReferences2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback4::SurvivingReferences2
helpviewer_keywords:
- ICorProfilerCallback4::SurvivingReferences2 method [.NET Framework profiling]
- SurvivingReferences2 method, ICorProfilerCallback4 interface [.NET Framework profiling]
ms.assetid: 02b51888-5d89-4e50-a915-45b7e329aad9
topic_type:
- apiref
ms.openlocfilehash: d092729c77b0c4feb253bb2f54968f7ff8bdbb2a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788678"
---
# <a name="icorprofilercallback4survivingreferences2-method"></a><span data-ttu-id="84ed6-103">ICorProfilerCallback4::SurvivingReferences2 方法</span><span class="sxs-lookup"><span data-stu-id="84ed6-103">ICorProfilerCallback4::SurvivingReferences2 Method</span></span>

<span data-ttu-id="84ed6-104">将堆中对象的布局报告为非压缩垃圾回收的结果。</span><span class="sxs-lookup"><span data-stu-id="84ed6-104">Reports the layout of objects in the heap as a result of a non-compacting garbage collection.</span></span> <span data-ttu-id="84ed6-105">如果探查器实现了 [ICorProfilerCallback4](icorprofilercallback4-interface.md) 接口，则调用此方法。</span><span class="sxs-lookup"><span data-stu-id="84ed6-105">This method is called if the profiler has implemented the [ICorProfilerCallback4](icorprofilercallback4-interface.md) interface.</span></span> <span data-ttu-id="84ed6-106">此回调可替换 [ICorProfilerCallback2：： SurvivingReferences](icorprofilercallback2-survivingreferences-method.md) 方法，因为它可以报告长度超过在 ULONG 中可表达的内容的更大范围的对象。</span><span class="sxs-lookup"><span data-stu-id="84ed6-106">This callback replaces the [ICorProfilerCallback2::SurvivingReferences](icorprofilercallback2-survivingreferences-method.md) method, because it can report larger ranges of objects whose lengths exceed what can be expressed in a ULONG.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84ed6-107">语法</span><span class="sxs-lookup"><span data-stu-id="84ed6-107">Syntax</span></span>  
  
```cpp  
HRESULT SurvivingReferences2(  
    [in] ULONG  cSurvivingObjectIDRanges,  
    [in, size_is(cSurvivingObjectIDRanges)] ObjectID  
                objectIDRangeStart[] ,  
    [in, size_is(cSurvivingObjectIDRanges)] SIZE_T  
                cObjectIDRangeLength[] );  
```  
  
## <a name="parameters"></a><span data-ttu-id="84ed6-108">参数</span><span class="sxs-lookup"><span data-stu-id="84ed6-108">Parameters</span></span>  

 `cSurvivingObjectIDRanges`  
 <span data-ttu-id="84ed6-109">[in] 作为非压缩垃圾回收的结果而仍存在的连续对象块的数量。</span><span class="sxs-lookup"><span data-stu-id="84ed6-109">[in] The number of blocks of contiguous objects that survived as the result of the non-compacting garbage collection.</span></span> <span data-ttu-id="84ed6-110">即，`cSurvivingObjectIDRanges` 的值是 `objectIDRangeStart` 和 `cObjectIDRangeLength` 数组的大小，分别存储每个对象块的 `ObjectID` 和长度。</span><span class="sxs-lookup"><span data-stu-id="84ed6-110">That is, the value of `cSurvivingObjectIDRanges` is the size of the `objectIDRangeStart` and `cObjectIDRangeLength` arrays, which store an `ObjectID` and a length, respectively, for each block of objects.</span></span>  
  
 <span data-ttu-id="84ed6-111">`SurvivingReferences2` 接来下的两个参数为并行数组。</span><span class="sxs-lookup"><span data-stu-id="84ed6-111">The next two arguments of `SurvivingReferences2` are parallel arrays.</span></span> <span data-ttu-id="84ed6-112">即，`objectIDRangeStart` 和 `cObjectIDRangeLength` 涉及同一连续对象块。</span><span class="sxs-lookup"><span data-stu-id="84ed6-112">In other words, `objectIDRangeStart` and `cObjectIDRangeLength` concern the same block of contiguous objects.</span></span>  
  
 `objectIDRangeStart`  
 <span data-ttu-id="84ed6-113">[in] `ObjectID` 值的数组，其中每个值均为内存中连续活动对象块的起始地址。</span><span class="sxs-lookup"><span data-stu-id="84ed6-113">[in] An array of `ObjectID` values, each of which is the starting address of a block of contiguous, live objects in memory.</span></span>  
  
 `cObjectIDRangeLength`  
 <span data-ttu-id="84ed6-114">[in] 整数数组，其中每个整数均为内存中保留下来的连续对象块的大小。</span><span class="sxs-lookup"><span data-stu-id="84ed6-114">[in] An array of integers, each of which is the size of a surviving block of contiguous objects in memory.</span></span>  
  
 <span data-ttu-id="84ed6-115">`objectIDRangeStart` 数组中引用的每个块均指定了大小。</span><span class="sxs-lookup"><span data-stu-id="84ed6-115">A size is specified for each block that is referenced in the `objectIDRangeStart` array.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="84ed6-116">备注</span><span class="sxs-lookup"><span data-stu-id="84ed6-116">Remarks</span></span>  

 <span data-ttu-id="84ed6-117">应按以下方式解释 `objectIDRangeStart` 和 `cObjectIDRangeLength` 数组的元素，以确定垃圾回收后对象是否仍存在。</span><span class="sxs-lookup"><span data-stu-id="84ed6-117">The elements of the `objectIDRangeStart` and `cObjectIDRangeLength` arrays should be interpreted as follows to determine whether an object survived the garbage collection.</span></span> <span data-ttu-id="84ed6-118">假定 `ObjectID` 值 (`ObjectID`) 在以下范围内：</span><span class="sxs-lookup"><span data-stu-id="84ed6-118">Assume that an `ObjectID` value (`ObjectID`) lies within the following range:</span></span>  
  
 `ObjectIDRangeStart[i]` <= `ObjectID` < `ObjectIDRangeStart[i]` + `cObjectIDRangeLength[i]`  
  
 <span data-ttu-id="84ed6-119">对于以下范围内 `i` 的任何值，此对象在垃圾回收后仍存在：</span><span class="sxs-lookup"><span data-stu-id="84ed6-119">For any value of `i` that is in the following range, the object has survived the garbage collection:</span></span>  
  
 <span data-ttu-id="84ed6-120">0 <= `i` < `cSurvivingObjectIDRanges`</span><span class="sxs-lookup"><span data-stu-id="84ed6-120">0 <= `i` < `cSurvivingObjectIDRanges`</span></span>  
  
 <span data-ttu-id="84ed6-121">非压缩垃圾回收将回收“死”对象占用的内存，但不会压缩释放的空间。</span><span class="sxs-lookup"><span data-stu-id="84ed6-121">A non-compacting garbage collection reclaims the memory occupied by "dead" objects, but does not compact that freed space.</span></span> <span data-ttu-id="84ed6-122">由此，内存返回到堆中，但“活”对象不会移动。</span><span class="sxs-lookup"><span data-stu-id="84ed6-122">As a result, memory is returned to the heap, but no "live" objects are moved.</span></span>  
  
 <span data-ttu-id="84ed6-123">公共语言运行时 (CLR) 调用 `SurvivingReferences2` 进行非压缩垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="84ed6-123">The common language runtime (CLR) calls `SurvivingReferences2` for non-compacting garbage collections.</span></span> <span data-ttu-id="84ed6-124">对于压缩垃圾回收，将改为调用 [MovedReferences2](icorprofilercallback4-movedreferences2-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="84ed6-124">For compacting garbage collections, [MovedReferences2](icorprofilercallback4-movedreferences2-method.md) is called instead.</span></span> <span data-ttu-id="84ed6-125">单个垃圾回收可针对一个生成进行压缩，而针对另一个生成不进行压缩。</span><span class="sxs-lookup"><span data-stu-id="84ed6-125">A single garbage collection can be compacting for one generation and non-compacting for another.</span></span> <span data-ttu-id="84ed6-126">对于任何特定代上的垃圾回收，探查器都将接收 `SurvivingReferences2` 回调或 [MovedReferences2](icorprofilercallback4-movedreferences2-method.md) 回调，但不能同时接收二者。</span><span class="sxs-lookup"><span data-stu-id="84ed6-126">For a garbage collection on any particular generation, the profiler will receive either a `SurvivingReferences2` callback or a [MovedReferences2](icorprofilercallback4-movedreferences2-method.md) callback, but not both.</span></span>  
  
 <span data-ttu-id="84ed6-127">由于内部缓冲有限、服务器垃圾回收期间的多个回调以及其他原因，在特定的垃圾回收过程中，可能收到多个 `SurvivingReferences2` 回调。</span><span class="sxs-lookup"><span data-stu-id="84ed6-127">Multiple `SurvivingReferences2` callbacks might be received during a particular garbage collection, because of limited internal buffering, multiple callbacks during server garbage collection, and other reasons.</span></span> <span data-ttu-id="84ed6-128">如果在垃圾回收期间收到多个回调，则信息是累积的；所有 `SurvivingReferences2` 回调中报告的任何引用都将在垃圾回收后仍然存在。</span><span class="sxs-lookup"><span data-stu-id="84ed6-128">In the case of multiple callbacks during a garbage collection, the information is cumulative; all references that are reported in any `SurvivingReferences2` callback survive the garbage collection.</span></span>  
  
 <span data-ttu-id="84ed6-129">如果探查器同时实现 [ICorProfilerCallback](icorprofilercallback-interface.md) 和 [ICorProfilerCallback4](icorprofilercallback4-interface.md) 接口，则在 `SurvivingReferences2` [ICorProfilerCallback2：： SurvivingReferences](icorprofilercallback2-survivingreferences-method.md) 方法之前调用方法，但仅在 `SurvivingReferences2` 成功返回时调用。</span><span class="sxs-lookup"><span data-stu-id="84ed6-129">If the profiler implements both the [ICorProfilerCallback](icorprofilercallback-interface.md) and the [ICorProfilerCallback4](icorprofilercallback4-interface.md) interfaces, the `SurvivingReferences2` method is called before the [ICorProfilerCallback2::SurvivingReferences](icorprofilercallback2-survivingreferences-method.md) method, but only if `SurvivingReferences2` returns successfully.</span></span> <span data-ttu-id="84ed6-130">探查器可以返回一个 HRESULT，指示由 `SurvivingReferences2` 方法引发的故障，以避免调用第二种方法。</span><span class="sxs-lookup"><span data-stu-id="84ed6-130">Profilers can return an HRESULT that indicates failure from the `SurvivingReferences2` method to avoid calling the second method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="84ed6-131">要求</span><span class="sxs-lookup"><span data-stu-id="84ed6-131">Requirements</span></span>  

 <span data-ttu-id="84ed6-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="84ed6-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="84ed6-133">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="84ed6-133">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="84ed6-134">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="84ed6-134">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="84ed6-135">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="84ed6-135">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84ed6-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="84ed6-136">See also</span></span>

- [<span data-ttu-id="84ed6-137">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="84ed6-137">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="84ed6-138">ICorProfilerCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="84ed6-138">ICorProfilerCallback2 Interface</span></span>](icorprofilercallback2-interface.md)
- [<span data-ttu-id="84ed6-139">ICorProfilerCallback4 接口</span><span class="sxs-lookup"><span data-stu-id="84ed6-139">ICorProfilerCallback4 Interface</span></span>](icorprofilercallback4-interface.md)
