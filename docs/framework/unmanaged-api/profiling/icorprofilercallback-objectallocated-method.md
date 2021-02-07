---
description: 了解详细信息： ICorProfilerCallback：： ObjectAllocated 方法
title: ICorProfilerCallback::ObjectAllocated 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ObjectAllocated
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ObjectAllocated
helpviewer_keywords:
- ObjectAllocated method [.NET Framework profiling]
- ICorProfilerCallback::ObjectAllocated method [.NET Framework profiling]
ms.assetid: eb412622-77cc-4abd-a2cd-c910fe8edd54
topic_type:
- apiref
ms.openlocfilehash: 58b58aeb4bb88d0df32cebc32440317a4d23632d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745159"
---
# <a name="icorprofilercallbackobjectallocated-method"></a><span data-ttu-id="4dd71-103">ICorProfilerCallback::ObjectAllocated 方法</span><span class="sxs-lookup"><span data-stu-id="4dd71-103">ICorProfilerCallback::ObjectAllocated Method</span></span>

<span data-ttu-id="4dd71-104">通知探查器已为对象分配堆中的内存。</span><span class="sxs-lookup"><span data-stu-id="4dd71-104">Notifies the profiler that memory within the heap has been allocated for an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4dd71-105">语法</span><span class="sxs-lookup"><span data-stu-id="4dd71-105">Syntax</span></span>  
  
```cpp  
HRESULT ObjectAllocated(  
    [in] ObjectID objectId,  
    [in] ClassID classId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4dd71-106">参数</span><span class="sxs-lookup"><span data-stu-id="4dd71-106">Parameters</span></span>  

 `objectId`  
 <span data-ttu-id="4dd71-107">中为其分配内存的对象的 ID。</span><span class="sxs-lookup"><span data-stu-id="4dd71-107">[in] The ID of the object for which memory was allocated.</span></span>  
  
 `classId`  
 <span data-ttu-id="4dd71-108">中对象为其实例的类的 ID。</span><span class="sxs-lookup"><span data-stu-id="4dd71-108">[in] The ID of the class of which the object is an instance.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4dd71-109">备注</span><span class="sxs-lookup"><span data-stu-id="4dd71-109">Remarks</span></span>  

 <span data-ttu-id="4dd71-110">`ObjectedAllocated`对于来自堆栈或非托管内存的分配，不调用方法。</span><span class="sxs-lookup"><span data-stu-id="4dd71-110">The `ObjectedAllocated` method is not called for allocations from either the stack or unmanaged memory.</span></span> <span data-ttu-id="4dd71-111">`classId`参数可以引用尚未加载的托管代码中的类。</span><span class="sxs-lookup"><span data-stu-id="4dd71-111">The `classId` parameter can refer to a class in managed code that has not been loaded yet.</span></span> <span data-ttu-id="4dd71-112">探查器将在回调后立即收到该类的类加载回调 `ObjectAllocated` 。</span><span class="sxs-lookup"><span data-stu-id="4dd71-112">The profiler will receive a class load callback for that class immediately after the `ObjectAllocated` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4dd71-113">要求</span><span class="sxs-lookup"><span data-stu-id="4dd71-113">Requirements</span></span>  

 <span data-ttu-id="4dd71-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4dd71-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4dd71-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="4dd71-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="4dd71-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4dd71-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4dd71-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4dd71-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4dd71-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="4dd71-118">See also</span></span>

- [<span data-ttu-id="4dd71-119">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="4dd71-119">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="4dd71-120">ClassLoadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="4dd71-120">ClassLoadStarted Method</span></span>](icorprofilercallback-classloadstarted-method.md)
- [<span data-ttu-id="4dd71-121">ClassLoadFinished 方法</span><span class="sxs-lookup"><span data-stu-id="4dd71-121">ClassLoadFinished Method</span></span>](icorprofilercallback-classloadfinished-method.md)
