---
description: 了解详细信息： ICorProfilerCallback：： RootReferences 方法
title: ICorProfilerCallback::RootReferences 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RootReferences
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RootReferences
helpviewer_keywords:
- RootReferences method [.NET Framework profiling]
- ICorProfilerCallback::RootReferences method [.NET Framework profiling]
ms.assetid: dbdf853b-d1a4-4828-8ef7-53d121d8e6ae
topic_type:
- apiref
ms.openlocfilehash: e09434c425784e646c9856693abdfd4ac0d49273
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788860"
---
# <a name="icorprofilercallbackrootreferences-method"></a><span data-ttu-id="c9dc5-103">ICorProfilerCallback::RootReferences 方法</span><span class="sxs-lookup"><span data-stu-id="c9dc5-103">ICorProfilerCallback::RootReferences Method</span></span>

<span data-ttu-id="c9dc5-104">在垃圾回收后通知探查器有关根引用的信息。</span><span class="sxs-lookup"><span data-stu-id="c9dc5-104">Notifies the profiler with information about root references after garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9dc5-105">语法</span><span class="sxs-lookup"><span data-stu-id="c9dc5-105">Syntax</span></span>  
  
```cpp  
HRESULT RootReferences(  
    [in] ULONG    cRootRefs,  
    [in, size_is(cRootRefs)] ObjectID rootRefIds[] );  
```  
  
## <a name="parameters"></a><span data-ttu-id="c9dc5-106">参数</span><span class="sxs-lookup"><span data-stu-id="c9dc5-106">Parameters</span></span>  

 `cRootRefs`  
 <span data-ttu-id="c9dc5-107">中数组中的引用数 `rootRefIds` 。</span><span class="sxs-lookup"><span data-stu-id="c9dc5-107">[in] The number of references in the `rootRefIds` array.</span></span>  
  
 `rootRefIds`  
 <span data-ttu-id="c9dc5-108">中对象 Id 的数组，这些对象 Id 引用静态对象或堆栈上的对象。</span><span class="sxs-lookup"><span data-stu-id="c9dc5-108">[in] An array of object IDs that reference either a static object or an object on the stack.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c9dc5-109">备注</span><span class="sxs-lookup"><span data-stu-id="c9dc5-109">Remarks</span></span>  

 <span data-ttu-id="c9dc5-110">同时 `RootReferences` 调用和 [ICorProfilerCallback2：： RootReferences2](icorprofilercallback2-rootreferences2-method.md) 来通知探查器。</span><span class="sxs-lookup"><span data-stu-id="c9dc5-110">Both `RootReferences` and [ICorProfilerCallback2::RootReferences2](icorprofilercallback2-rootreferences2-method.md) are called to notify the profiler.</span></span> <span data-ttu-id="c9dc5-111">探查器通常会实现一个或另一个，但不能同时实现两者，因为传入的信息 `RootReferences2` 是传入的的 `RootReferences` 超集。</span><span class="sxs-lookup"><span data-stu-id="c9dc5-111">Profilers will normally implement one or the other, but not both, because the information passed in `RootReferences2` is a superset of that passed in `RootReferences`.</span></span>  
  
 <span data-ttu-id="c9dc5-112">`rootRefIds`数组可以包含空对象。</span><span class="sxs-lookup"><span data-stu-id="c9dc5-112">It is possible for the `rootRefIds` array to contain a null object.</span></span> <span data-ttu-id="c9dc5-113">例如，在堆栈上声明的所有对象引用都被垃圾回收器视为根，并将始终报告。</span><span class="sxs-lookup"><span data-stu-id="c9dc5-113">For example, all object references declared on the stack are treated as roots by the garbage collector and will always be reported.</span></span>  
  
 <span data-ttu-id="c9dc5-114">返回的对象 Id 在 `RootReferences` 回调过程中无效，因为垃圾回收可能正处于将对象从旧地址移到新地址的过程中。</span><span class="sxs-lookup"><span data-stu-id="c9dc5-114">The object IDs returned by `RootReferences` are not valid during the callback itself, because the garbage collection might be in the middle of moving objects from old addresses to new addresses.</span></span> <span data-ttu-id="c9dc5-115">因此，探查器不能尝试在调用过程中检查对象 `RootReferences` 。</span><span class="sxs-lookup"><span data-stu-id="c9dc5-115">Therefore, profilers must not attempt to inspect objects during a `RootReferences` call.</span></span> <span data-ttu-id="c9dc5-116">调用 [ICorProfilerCallback2：： GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md) 时，所有对象已移动到它们的新位置，并且可以安全检查。</span><span class="sxs-lookup"><span data-stu-id="c9dc5-116">When [ICorProfilerCallback2::GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md) is called, all objects have been moved to their new locations and can be safely inspected.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c9dc5-117">要求</span><span class="sxs-lookup"><span data-stu-id="c9dc5-117">Requirements</span></span>  

 <span data-ttu-id="c9dc5-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c9dc5-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c9dc5-119">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c9dc5-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c9dc5-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c9dc5-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c9dc5-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c9dc5-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9dc5-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="c9dc5-122">See also</span></span>

- [<span data-ttu-id="c9dc5-123">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="c9dc5-123">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
