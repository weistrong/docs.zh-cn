---
description: 了解详细信息： ICorProfilerInfo3：： SetEnterLeaveFunctionHooks3WithInfo 方法
title: ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.SetEnterLeaveFunctionHooks3WithInfo Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo
helpviewer_keywords:
- SetEnterLeaveFunctionHooks3WithInfo method [.NET Framework profiling]
- ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo method [.NET Framework profiling]
ms.assetid: ca8ea534-e441-47b8-be85-466410988c0a
topic_type:
- apiref
ms.openlocfilehash: 15f6696635172972b09e68beeae13a7d6a8e195a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687007"
---
# <a name="icorprofilerinfo3setenterleavefunctionhooks3withinfo-method"></a><span data-ttu-id="ab3b8-103">ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo 方法</span><span class="sxs-lookup"><span data-stu-id="ab3b8-103">ICorProfilerInfo3::SetEnterLeaveFunctionHooks3WithInfo Method</span></span>

<span data-ttu-id="ab3b8-104">指定将在托管函数的 [FunctionEnter3WithInfo](functionenter3withinfo-function.md)、 [FunctionLeave3WithInfo](functionleave3withinfo-function.md)和 [FunctionTailcall3WithInfo](functiontailcall3withinfo-function.md) 挂钩上调用的探查器实现函数。</span><span class="sxs-lookup"><span data-stu-id="ab3b8-104">Specifies the profiler-implemented functions that will be called on the [FunctionEnter3WithInfo](functionenter3withinfo-function.md), [FunctionLeave3WithInfo](functionleave3withinfo-function.md), and [FunctionTailcall3WithInfo](functiontailcall3withinfo-function.md) hooks of managed functions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab3b8-105">语法</span><span class="sxs-lookup"><span data-stu-id="ab3b8-105">Syntax</span></span>  
  
```cpp  
HRESULT SetEnterLeaveFunctionHooks3WithInfo(  
            [in] FunctionEnter3WithInfo    *pFuncEnter3,  
            [in] FunctionLeave3withInfo    *pFuncLeave3,  
            [in] FunctionTailcall3WithInfo *pFuncTailcall3);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ab3b8-106">参数</span><span class="sxs-lookup"><span data-stu-id="ab3b8-106">Parameters</span></span>  

 `pFuncEnter3`  
 <span data-ttu-id="ab3b8-107">中指向要用作回调的实现的指针 `FunctionEnter3WithInfo` 。</span><span class="sxs-lookup"><span data-stu-id="ab3b8-107">[in] A pointer to the implementation to be used as the `FunctionEnter3WithInfo` callback.</span></span>  
  
 `pFuncLeave3`  
 <span data-ttu-id="ab3b8-108">中指向要用作回调的实现的指针 `FunctionLeave3WithInfo` 。</span><span class="sxs-lookup"><span data-stu-id="ab3b8-108">[in] A pointer to the implementation to be used as the `FunctionLeave3WithInfo` callback.</span></span>  
  
 `pFuncTailcall3`  
 <span data-ttu-id="ab3b8-109">中指向要用作回调的实现的指针 `FunctionTailcall3WithInfo` 。</span><span class="sxs-lookup"><span data-stu-id="ab3b8-109">[in] A pointer to the implementation to be used as the `FunctionTailcall3WithInfo` callback.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ab3b8-110">备注</span><span class="sxs-lookup"><span data-stu-id="ab3b8-110">Remarks</span></span>  

 <span data-ttu-id="ab3b8-111">[FunctionEnter3WithInfo](functionenter3withinfo-function.md)、 [FunctionLeave3WithInfo](functionleave3withinfo-function.md)和[FunctionTailcall3WithInfo](functiontailcall3withinfo-function.md)挂钩提供堆栈帧和参数检查。</span><span class="sxs-lookup"><span data-stu-id="ab3b8-111">The [FunctionEnter3WithInfo](functionenter3withinfo-function.md), [FunctionLeave3WithInfo](functionleave3withinfo-function.md), and [FunctionTailcall3WithInfo](functiontailcall3withinfo-function.md) hooks provide stack frame and argument inspection.</span></span> <span data-ttu-id="ab3b8-112">若要访问该信息， `COR_PRF_ENABLE_FUNCTION_ARGS` `COR_PRF_ENABLE_FUNCTION_RETVAL` 必须设置、和/或 `COR_PRF_ENABLE_FRAME_INFO` 标志。</span><span class="sxs-lookup"><span data-stu-id="ab3b8-112">To access that information, the `COR_PRF_ENABLE_FUNCTION_ARGS`, `COR_PRF_ENABLE_FUNCTION_RETVAL`, and/or `COR_PRF_ENABLE_FRAME_INFO` flags have to be set.</span></span> <span data-ttu-id="ab3b8-113">探查器可以使用 [ICorProfilerInfo：： SetEventMask](icorprofilerinfo-seteventmask-method.md) 方法来设置事件标志，然后使用 `SetEnterLeaveFunctionHooks3WithInfo` 方法来注册此函数的实现。</span><span class="sxs-lookup"><span data-stu-id="ab3b8-113">The profiler can use the [ICorProfilerInfo::SetEventMask](icorprofilerinfo-seteventmask-method.md) method to set the event flags, and then use the `SetEnterLeaveFunctionHooks3WithInfo` method to register your implementation of this function.</span></span>  
  
 <span data-ttu-id="ab3b8-114">一次只能有一组回调处于活动状态，最新版本优先。</span><span class="sxs-lookup"><span data-stu-id="ab3b8-114">Only one set of callbacks may be active at a time, and the newest version takes precedence.</span></span> <span data-ttu-id="ab3b8-115">因此，如果探查器同时调用 [SetEnterLeaveFunctionHooks2](icorprofilerinfo2-setenterleavefunctionhooks2-method.md) 和 `SetEnterLeaveFunctionHooks3WithInfo` ， `SetEnterLeaveFunctionHooks3WithInfo` 则使用。</span><span class="sxs-lookup"><span data-stu-id="ab3b8-115">Therefore, if a profiler calls both [SetEnterLeaveFunctionHooks2](icorprofilerinfo2-setenterleavefunctionhooks2-method.md) and `SetEnterLeaveFunctionHooks3WithInfo`, `SetEnterLeaveFunctionHooks3WithInfo` is used.</span></span>  
  
 <span data-ttu-id="ab3b8-116">`SetEnterLeaveFunctionHooks3WithInfo`只能从探查器的[ICorProfilerCallback：： Initialize](icorprofilercallback-initialize-method.md)回调调用此方法。</span><span class="sxs-lookup"><span data-stu-id="ab3b8-116">The `SetEnterLeaveFunctionHooks3WithInfo` method may be called only from the profiler's [ICorProfilerCallback::Initialize](icorprofilercallback-initialize-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ab3b8-117">要求</span><span class="sxs-lookup"><span data-stu-id="ab3b8-117">Requirements</span></span>  

 <span data-ttu-id="ab3b8-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ab3b8-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab3b8-119">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ab3b8-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ab3b8-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ab3b8-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ab3b8-121">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ab3b8-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab3b8-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="ab3b8-122">See also</span></span>

- [<span data-ttu-id="ab3b8-123">SetEnterLeaveFunctionHooks3</span><span class="sxs-lookup"><span data-stu-id="ab3b8-123">SetEnterLeaveFunctionHooks3</span></span>](icorprofilerinfo3-setenterleavefunctionhooks3-method.md)
- [<span data-ttu-id="ab3b8-124">FunctionEnter3</span><span class="sxs-lookup"><span data-stu-id="ab3b8-124">FunctionEnter3</span></span>](functionenter3-function.md)
- [<span data-ttu-id="ab3b8-125">FunctionLeave3</span><span class="sxs-lookup"><span data-stu-id="ab3b8-125">FunctionLeave3</span></span>](functionleave3-function.md)
- [<span data-ttu-id="ab3b8-126">FunctionTailcall3</span><span class="sxs-lookup"><span data-stu-id="ab3b8-126">FunctionTailcall3</span></span>](functiontailcall3-function.md)
- [<span data-ttu-id="ab3b8-127">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="ab3b8-127">FunctionEnter3WithInfo</span></span>](functionenter3withinfo-function.md)
- [<span data-ttu-id="ab3b8-128">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="ab3b8-128">FunctionLeave3WithInfo</span></span>](functionleave3withinfo-function.md)
- [<span data-ttu-id="ab3b8-129">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="ab3b8-129">FunctionTailcall3WithInfo</span></span>](functiontailcall3withinfo-function.md)
- [<span data-ttu-id="ab3b8-130">分析全局静态函数</span><span class="sxs-lookup"><span data-stu-id="ab3b8-130">Profiling Global Static Functions</span></span>](profiling-global-static-functions.md)
- [<span data-ttu-id="ab3b8-131">ICorProfilerInfo3 接口</span><span class="sxs-lookup"><span data-stu-id="ab3b8-131">ICorProfilerInfo3 Interface</span></span>](icorprofilerinfo3-interface.md)
- [<span data-ttu-id="ab3b8-132">分析接口</span><span class="sxs-lookup"><span data-stu-id="ab3b8-132">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="ab3b8-133">分析</span><span class="sxs-lookup"><span data-stu-id="ab3b8-133">Profiling</span></span>](index.md)
