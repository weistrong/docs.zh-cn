---
description: 了解详细信息： ICorProfilerInfo2：： GetObjectGeneration 方法
title: ICorProfilerInfo2::GetObjectGeneration 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetObjectGeneration
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetObjectGeneration
helpviewer_keywords:
- GetObjectGeneration method [.NET Framework profiling]
- ICorProfilerInfo2::GetObjectGeneration method [.NET Framework profiling]
ms.assetid: b0d25f76-0bd5-4aa6-96cf-bfec0e1de28b
topic_type:
- apiref
ms.openlocfilehash: f4927c081393a11f7dad7d59cce311b82072659c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716414"
---
# <a name="icorprofilerinfo2getobjectgeneration-method"></a><span data-ttu-id="3a5c8-103">ICorProfilerInfo2::GetObjectGeneration 方法</span><span class="sxs-lookup"><span data-stu-id="3a5c8-103">ICorProfilerInfo2::GetObjectGeneration Method</span></span>

<span data-ttu-id="3a5c8-104">获取包含指定对象的堆段。</span><span class="sxs-lookup"><span data-stu-id="3a5c8-104">Gets the segment of the heap that contains the specified object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a5c8-105">语法</span><span class="sxs-lookup"><span data-stu-id="3a5c8-105">Syntax</span></span>  
  
```cpp  
HRESULT GetObjectGeneration(  
    [in] ObjectID objectId,  
    [out] COR_PRF_GC_GENERATION_RANGE *range);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3a5c8-106">参数</span><span class="sxs-lookup"><span data-stu-id="3a5c8-106">Parameters</span></span>  

 `objectId`  
 <span data-ttu-id="3a5c8-107">中对象的 ID。</span><span class="sxs-lookup"><span data-stu-id="3a5c8-107">[in] The ID of the object.</span></span>  
  
 `range`  
 <span data-ttu-id="3a5c8-108">弄指向 [COR_PRF_GC_GENERATION_RANGE](cor-prf-gc-generation-range-structure.md) 结构的指针，该结构描述一个范围 (即，生成中正在进行垃圾回收的内存块) 。</span><span class="sxs-lookup"><span data-stu-id="3a5c8-108">[out] A pointer to a [COR_PRF_GC_GENERATION_RANGE](cor-prf-gc-generation-range-structure.md) structure, which describes a range (that is, a block) of memory within the generation that is undergoing garbage collection.</span></span> <span data-ttu-id="3a5c8-109">此范围包含指定的对象。</span><span class="sxs-lookup"><span data-stu-id="3a5c8-109">This range contains the specified object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3a5c8-110">备注</span><span class="sxs-lookup"><span data-stu-id="3a5c8-110">Remarks</span></span>  

 <span data-ttu-id="3a5c8-111">`GetObjectGeneration`如果垃圾回收未进行，则可以从任何探查器回调调用方法。</span><span class="sxs-lookup"><span data-stu-id="3a5c8-111">The `GetObjectGeneration` method may be called from any profiler callback, provided that garbage collection is not in progress.</span></span> <span data-ttu-id="3a5c8-112">也就是说，它可从任何回调调用， [ICorProfilerCallback2：： GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md) 和 [ICorProfilerCallback2：： GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md)之间发生的回调除外。</span><span class="sxs-lookup"><span data-stu-id="3a5c8-112">That is, it may be called from any callback except those that occur between [ICorProfilerCallback2::GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md) and [ICorProfilerCallback2::GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a5c8-113">要求</span><span class="sxs-lookup"><span data-stu-id="3a5c8-113">Requirements</span></span>  

 <span data-ttu-id="3a5c8-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3a5c8-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a5c8-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3a5c8-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3a5c8-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3a5c8-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3a5c8-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3a5c8-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a5c8-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="3a5c8-118">See also</span></span>

- [<span data-ttu-id="3a5c8-119">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="3a5c8-119">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="3a5c8-120">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="3a5c8-120">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
