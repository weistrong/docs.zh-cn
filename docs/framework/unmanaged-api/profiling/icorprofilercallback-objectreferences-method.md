---
description: 了解详细信息： ICorProfilerCallback：： ObjectReferences 方法
title: ICorProfilerCallback::ObjectReferences 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ObjectReferences
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ObjectReferences
helpviewer_keywords:
- ObjectReferences method [.NET Framework profiling]
- ICorProfilerCallback::ObjectReferences method [.NET Framework profiling]
ms.assetid: dd5e9b64-b4a3-4ba6-9be6-ddb540f4ffcf
topic_type:
- apiref
ms.openlocfilehash: 55ea6fae87ecb6534af322fc9d5055c8a247f37a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745107"
---
# <a name="icorprofilercallbackobjectreferences-method"></a><span data-ttu-id="d7a71-103">ICorProfilerCallback::ObjectReferences 方法</span><span class="sxs-lookup"><span data-stu-id="d7a71-103">ICorProfilerCallback::ObjectReferences Method</span></span>

<span data-ttu-id="d7a71-104">通知探查器有关指定的对象正在引用的内存中的对象。</span><span class="sxs-lookup"><span data-stu-id="d7a71-104">Notifies the profiler about objects in memory that are being referenced by the specified object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d7a71-105">语法</span><span class="sxs-lookup"><span data-stu-id="d7a71-105">Syntax</span></span>  
  
```cpp  
HRESULT ObjectReferences(  
    [in]  ObjectID objectId,  
    [in]  ClassID  classId,  
    [in]  ULONG    cObjectRefs,  
    [in, size_is(cObjectRefs)] ObjectID objectRefIds[] );  
```  
  
## <a name="parameters"></a><span data-ttu-id="d7a71-106">参数</span><span class="sxs-lookup"><span data-stu-id="d7a71-106">Parameters</span></span>  

 `objectId`  
 <span data-ttu-id="d7a71-107">中引用对象的对象的 ID。</span><span class="sxs-lookup"><span data-stu-id="d7a71-107">[in] The ID of the object that is referencing objects.</span></span>  
  
 `classId`  
 <span data-ttu-id="d7a71-108">中指定对象是其实例的类的 ID。</span><span class="sxs-lookup"><span data-stu-id="d7a71-108">[in] The ID of the class that the specified object is an instance of.</span></span>  
  
 `cObjectRefs`  
 <span data-ttu-id="d7a71-109">中指定的对象引用的对象数 (即数组中的元素数 `objectRefIds`) 。</span><span class="sxs-lookup"><span data-stu-id="d7a71-109">[in] The number of objects referenced by the specified object (that is, the number of elements in the `objectRefIds` array).</span></span>  
  
 `objectRefIds`  
 <span data-ttu-id="d7a71-110">中由引用的对象的 Id 数组 `objectId` 。</span><span class="sxs-lookup"><span data-stu-id="d7a71-110">[in] An array of IDs of objects that are being referenced by `objectId`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d7a71-111">备注</span><span class="sxs-lookup"><span data-stu-id="d7a71-111">Remarks</span></span>  

 <span data-ttu-id="d7a71-112">`ObjectReferences`完成垃圾回收后，将为堆中剩余的每个对象调用方法。</span><span class="sxs-lookup"><span data-stu-id="d7a71-112">The `ObjectReferences` method is called for each object remaining in the heap after a garbage collection has completed.</span></span> <span data-ttu-id="d7a71-113">如果探查器从此回调返回错误，则分析服务将停止调用此回调，直到下一次垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="d7a71-113">If the profiler returns an error from this callback, the profiling services will discontinue invoking this callback until the next garbage collection.</span></span>  
  
 <span data-ttu-id="d7a71-114">`ObjectReferences`回调可与[ICorProfilerCallback：： RootReferences](icorprofilercallback-rootreferences-method.md)回调结合使用，以便为运行时创建完整的对象引用关系图。</span><span class="sxs-lookup"><span data-stu-id="d7a71-114">The `ObjectReferences` callback can be used in conjunction with the [ICorProfilerCallback::RootReferences](icorprofilercallback-rootreferences-method.md) callback to create a complete object reference graph for the runtime.</span></span> <span data-ttu-id="d7a71-115">公共语言运行时 (CLR) 确保每个对象引用只通过方法报告一次 `ObjectReferences` 。</span><span class="sxs-lookup"><span data-stu-id="d7a71-115">The common language runtime (CLR) ensures that each object reference is reported only once by the `ObjectReferences` method.</span></span>  
  
 <span data-ttu-id="d7a71-116">返回的对象 Id 在 `ObjectReferences` 回调过程中无效，因为垃圾回收可能是在移动对象的中间。</span><span class="sxs-lookup"><span data-stu-id="d7a71-116">The object IDs returned by `ObjectReferences` are not valid during the callback itself, because the garbage collection might be in the middle of moving objects.</span></span> <span data-ttu-id="d7a71-117">因此，探查器不能尝试在调用过程中检查对象 `ObjectReferences` 。</span><span class="sxs-lookup"><span data-stu-id="d7a71-117">Therefore, profilers must not attempt to inspect objects during an `ObjectReferences` call.</span></span> <span data-ttu-id="d7a71-118">调用 [ICorProfilerCallback2：： GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md) 时，垃圾回收已完成，可安全完成检查。</span><span class="sxs-lookup"><span data-stu-id="d7a71-118">When [ICorProfilerCallback2::GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md) is called, the garbage collection is complete and inspection can be safely done.</span></span>  
  
 <span data-ttu-id="d7a71-119">如果为 null `ClassId` ， `objectId` 则表示具有正在卸载的类型。</span><span class="sxs-lookup"><span data-stu-id="d7a71-119">A null `ClassId` indicates that `objectId` has a type that is unloading.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d7a71-120">要求</span><span class="sxs-lookup"><span data-stu-id="d7a71-120">Requirements</span></span>  

 <span data-ttu-id="d7a71-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d7a71-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d7a71-122">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d7a71-122">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d7a71-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d7a71-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d7a71-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d7a71-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d7a71-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="d7a71-125">See also</span></span>

- [<span data-ttu-id="d7a71-126">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="d7a71-126">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
