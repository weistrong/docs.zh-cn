---
description: 了解详细信息： COR_PRF_GC_GENERATION_RANGE 结构
title: COR_PRF_GC_GENERATION_RANGE 结构
ms.date: 03/30/2017
api_name:
- COR_PRF_GC_GENERATION_RANGE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_GC_GENERATION_RANGE
helpviewer_keywords:
- COR_PRF_GC_GENERATION_RANGE structure [.NET Framework profiling]
ms.assetid: e7e07273-8d10-4a68-807e-59634e3f8c5e
topic_type:
- apiref
ms.openlocfilehash: ea67a6e6b972b9406b84ad331e8af6189327c5ff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648891"
---
# <a name="cor_prf_gc_generation_range-structure"></a><span data-ttu-id="186ae-103">COR_PRF_GC_GENERATION_RANGE 结构</span><span class="sxs-lookup"><span data-stu-id="186ae-103">COR_PRF_GC_GENERATION_RANGE Structure</span></span>

<span data-ttu-id="186ae-104">描述一个正进行垃圾回收的内存范围（即块）。</span><span class="sxs-lookup"><span data-stu-id="186ae-104">Describes a range (that is, block) of memory that is undergoing garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="186ae-105">语法</span><span class="sxs-lookup"><span data-stu-id="186ae-105">Syntax</span></span>  
  
```cpp  
typedef struct COR_PRF_GC_GENERATION_RANGE {  
    COR_PRF_GC_GENERATION generation;  
    ObjectID rangeStart;  
    UINT_PTR rangeLength;  
    UINT_PTR rangeLengthReserved;  
} COR_PRF_GC_GENERATION_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="186ae-106">成员</span><span class="sxs-lookup"><span data-stu-id="186ae-106">Members</span></span>  
  
|<span data-ttu-id="186ae-107">成员</span><span class="sxs-lookup"><span data-stu-id="186ae-107">Member</span></span>|<span data-ttu-id="186ae-108">说明</span><span class="sxs-lookup"><span data-stu-id="186ae-108">Description</span></span>|  
|------------|-----------------|  
|`generation`|<span data-ttu-id="186ae-109">一个 [COR_PRF_GC_GENERATION](cor-prf-gc-generation-enumeration.md) 枚举的值，该值指定内存块所属的代。</span><span class="sxs-lookup"><span data-stu-id="186ae-109">A value of the [COR_PRF_GC_GENERATION](cor-prf-gc-generation-enumeration.md) enumeration that specifies the generation to which the block of memory belongs.</span></span>|  
|`rangeStart`|<span data-ttu-id="186ae-110">对象的 ID，该对象指定内存块的起始位置。</span><span class="sxs-lookup"><span data-stu-id="186ae-110">The ID of an object that specifies the starting location of the block of memory.</span></span>|  
|`rangeLength`|<span data-ttu-id="186ae-111">一个指向整数的指针，该整数指定内存块的已使用部分的大小， (即块中使用的内存量) 。</span><span class="sxs-lookup"><span data-stu-id="186ae-111">A pointer to an integer that specifies the size of the used portion of the memory block (that is, the amount of memory used within the block).</span></span>|  
|`rangeLengthReserved`|<span data-ttu-id="186ae-112">指向一个整数的指针，该整数指定内存块的大小 (即，为块) 预留的内存量。</span><span class="sxs-lookup"><span data-stu-id="186ae-112">A pointer to an integer that specifies the size of the memory block (that is, the amount of memory reserved for the block).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="186ae-113">备注</span><span class="sxs-lookup"><span data-stu-id="186ae-113">Remarks</span></span>  

 <span data-ttu-id="186ae-114">`rangeLength`仅当[ICorProfilerInfo2：： GetGenerationBounds](icorprofilerinfo2-getgenerationbounds-method.md)或[ICorProfilerInfo2：： GetObjectGeneration](icorprofilerinfo2-getobjectgeneration-method.md)（这两个均使用该 `COR_PRF_GC_GENERATION_RANGE` 结构）从[ICorProfilerCallback2：： GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md)或[ICorProfilerCallback2：： GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md)方法调用时，此值才是准确的。</span><span class="sxs-lookup"><span data-stu-id="186ae-114">The `rangeLength` value is guaranteed to be accurate only if [ICorProfilerInfo2::GetGenerationBounds](icorprofilerinfo2-getgenerationbounds-method.md) or [ICorProfilerInfo2::GetObjectGeneration](icorprofilerinfo2-getobjectgeneration-method.md), both of which use the `COR_PRF_GC_GENERATION_RANGE` structure, is called from the [ICorProfilerCallback2::GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md) or the [ICorProfilerCallback2::GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="186ae-115">要求</span><span class="sxs-lookup"><span data-stu-id="186ae-115">Requirements</span></span>  

 <span data-ttu-id="186ae-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="186ae-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="186ae-117">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="186ae-117">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="186ae-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="186ae-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="186ae-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="186ae-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="186ae-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="186ae-120">See also</span></span>

- [<span data-ttu-id="186ae-121">分析结构</span><span class="sxs-lookup"><span data-stu-id="186ae-121">Profiling Structures</span></span>](profiling-structures.md)
