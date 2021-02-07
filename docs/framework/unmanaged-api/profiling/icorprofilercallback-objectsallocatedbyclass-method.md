---
description: 了解详细信息： ICorProfilerCallback：： ObjectsAllocatedByClass 方法
title: ICorProfilerCallback::ObjectsAllocatedByClass 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ObjectsAllocatedByClass
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ObjectsAllocatedByClass
helpviewer_keywords:
- ObjectsAllocatedByClass method [.NET Framework profiling]
- ICorProfilerCallback::ObjectsAllocatedByClass method [.NET Framework profiling]
ms.assetid: 91d688f3-a80e-419d-9755-ff94bc04188a
topic_type:
- apiref
ms.openlocfilehash: df9f3dde27664de7db4afb264b221f640753ddb3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745055"
---
# <a name="icorprofilercallbackobjectsallocatedbyclass-method"></a><span data-ttu-id="d2501-103">ICorProfilerCallback::ObjectsAllocatedByClass 方法</span><span class="sxs-lookup"><span data-stu-id="d2501-103">ICorProfilerCallback::ObjectsAllocatedByClass Method</span></span>

<span data-ttu-id="d2501-104">通知探查器自最近一次垃圾回收后已创建的每个指定类的实例数。</span><span class="sxs-lookup"><span data-stu-id="d2501-104">Notifies the profiler about the number of instances of each specified class that have been created since the most recent garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d2501-105">语法</span><span class="sxs-lookup"><span data-stu-id="d2501-105">Syntax</span></span>  
  
```cpp  
HRESULT ObjectsAllocatedByClass(  
    [in] ULONG   cClassCount,  
    [in, size_is(cClassCount)] ClassID classIds[] ,  
    [in, size_is(cClassCount)] ULONG   cObjects[] );  
```  
  
## <a name="parameters"></a><span data-ttu-id="d2501-106">参数</span><span class="sxs-lookup"><span data-stu-id="d2501-106">Parameters</span></span>  

 `cClassCount`  
 <span data-ttu-id="d2501-107">中和数组的大小 `classIds` `cObjects` 。</span><span class="sxs-lookup"><span data-stu-id="d2501-107">[in] The size of the `classIds` and `cObjects` arrays.</span></span>  
  
 `classIds`  
 <span data-ttu-id="d2501-108">中类 Id 的数组，其中每个 ID 指定一个包含一个或多个实例的类。</span><span class="sxs-lookup"><span data-stu-id="d2501-108">[in] An array of class IDs, where each ID specifies a class with one or more instances.</span></span>  
  
 `cObjects`  
 <span data-ttu-id="d2501-109">中一个整数数组，其中每个整数指定数组中相应类的实例数 `classIds` 。</span><span class="sxs-lookup"><span data-stu-id="d2501-109">[in] An array of integers, where each integer specifies the number of instances for the corresponding class in the `classIds` array.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d2501-110">备注</span><span class="sxs-lookup"><span data-stu-id="d2501-110">Remarks</span></span>  

 <span data-ttu-id="d2501-111">`classIds`和 `cObjects` 数组是并行数组。</span><span class="sxs-lookup"><span data-stu-id="d2501-111">The `classIds` and `cObjects` arrays are parallel arrays.</span></span> <span data-ttu-id="d2501-112">例如， `classIds[i]` 和 `cObjects[i]` 引用相同的类。</span><span class="sxs-lookup"><span data-stu-id="d2501-112">For example, `classIds[i]` and `cObjects[i]` reference the same class.</span></span> <span data-ttu-id="d2501-113">如果自上次垃圾回收后未创建类的任何实例，则忽略类。</span><span class="sxs-lookup"><span data-stu-id="d2501-113">If no instance of a class has been created since the previous garbage collection, the class is omitted.</span></span> <span data-ttu-id="d2501-114">`ObjectsAllocatedByClass`回调不会报告在大型对象堆中分配的对象。</span><span class="sxs-lookup"><span data-stu-id="d2501-114">The `ObjectsAllocatedByClass` callback will not report objects allocated in the large object heap.</span></span>  
  
 <span data-ttu-id="d2501-115">报告的数字 `ObjectsAllocatedByClass` 仅限估算值。</span><span class="sxs-lookup"><span data-stu-id="d2501-115">The numbers reported by `ObjectsAllocatedByClass` are only estimates.</span></span> <span data-ttu-id="d2501-116">对于确切计数，请使用 [ICorProfilerCallback：： ObjectAllocated](icorprofilercallback-objectallocated-method.md)。</span><span class="sxs-lookup"><span data-stu-id="d2501-116">For exact counts, use [ICorProfilerCallback::ObjectAllocated](icorprofilercallback-objectallocated-method.md).</span></span>  
  
 <span data-ttu-id="d2501-117">`classIds`如果相应的 `cObjects` 数组包含正在卸载的类型，则数组可能包含一个或多个 null 项。</span><span class="sxs-lookup"><span data-stu-id="d2501-117">The `classIds` array may contain one or more null entries if the corresponding `cObjects` array has types that are unloading.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d2501-118">要求</span><span class="sxs-lookup"><span data-stu-id="d2501-118">Requirements</span></span>  

 <span data-ttu-id="d2501-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d2501-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d2501-120">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d2501-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d2501-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d2501-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d2501-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d2501-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2501-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="d2501-123">See also</span></span>

- [<span data-ttu-id="d2501-124">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="d2501-124">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
