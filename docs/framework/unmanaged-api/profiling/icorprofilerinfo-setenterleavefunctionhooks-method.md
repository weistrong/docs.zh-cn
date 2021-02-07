---
description: 了解详细信息： ICorProfilerInfo：： SetEnterLeaveFunctionHooks 方法
title: ICorProfilerInfo::SetEnterLeaveFunctionHooks 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.SetEnterLeaveFunctionHooks
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::SetEnterLeaveFunctionHooks
helpviewer_keywords:
- SetEnterLeaveFunctionHooks method [.NET Framework profiling]
- ICorProfilerInfo::SetEnterLeaveFunctionHooks method [.NET Framework profiling]
ms.assetid: 72399636-c219-4ffd-8ac8-39432c9d4641
topic_type:
- apiref
ms.openlocfilehash: 45c161a76f3ae568da6a83a2c45acb214a327ff1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687202"
---
# <a name="icorprofilerinfosetenterleavefunctionhooks-method"></a><span data-ttu-id="824b1-103">ICorProfilerInfo::SetEnterLeaveFunctionHooks 方法</span><span class="sxs-lookup"><span data-stu-id="824b1-103">ICorProfilerInfo::SetEnterLeaveFunctionHooks Method</span></span>

<span data-ttu-id="824b1-104">指定在托管函数的 "enter"、"leave" 和 "tailcall" 挂钩上调用的探查器实现函数。</span><span class="sxs-lookup"><span data-stu-id="824b1-104">Specifies profiler-implemented functions to be called on "enter", "leave", and "tailcall" hooks of managed functions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="824b1-105">语法</span><span class="sxs-lookup"><span data-stu-id="824b1-105">Syntax</span></span>  
  
```cpp  
HRESULT SetEnterLeaveFunctionHooks(  
    [in] FunctionEnter    *pFuncEnter,  
    [in] FunctionLeave    *pFuncLeave,  
    [in] FunctionTailcall *pFuncTailcall);  
```  
  
## <a name="parameters"></a><span data-ttu-id="824b1-106">参数</span><span class="sxs-lookup"><span data-stu-id="824b1-106">Parameters</span></span>  

 `pFuncEnter`  
 <span data-ttu-id="824b1-107">中指向要用作 [FunctionEnter](functionenter-function.md) 回调的实现的指针。</span><span class="sxs-lookup"><span data-stu-id="824b1-107">[in] A pointer to the implementation to be used as the [FunctionEnter](functionenter-function.md) callback.</span></span>  
  
 `pFuncLeave`  
 <span data-ttu-id="824b1-108">中指向要用作 [FunctionLeave](functionleave-function.md) 回调的实现的指针。</span><span class="sxs-lookup"><span data-stu-id="824b1-108">[in] A pointer to the implementation to be used as the [FunctionLeave](functionleave-function.md) callback.</span></span>  
  
 `pFuncTailcall`  
 <span data-ttu-id="824b1-109">中指向要用作 [FunctionTailcall](functiontailcall-function.md) 回调的实现的指针。</span><span class="sxs-lookup"><span data-stu-id="824b1-109">[in] A pointer to the implementation to be used as the [FunctionTailcall](functiontailcall-function.md) callback.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="824b1-110">备注</span><span class="sxs-lookup"><span data-stu-id="824b1-110">Remarks</span></span>  

 <span data-ttu-id="824b1-111">在 .NET Framework 版本1.0 中，每个函数指针均可为 null，以禁用相应的回调。</span><span class="sxs-lookup"><span data-stu-id="824b1-111">In the .NET Framework version 1.0, each function pointer can be null to disable that corresponding callback.</span></span>  
  
 <span data-ttu-id="824b1-112">一次只能有一个回调集处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="824b1-112">Only one set of callbacks can be active at a time.</span></span> <span data-ttu-id="824b1-113">因此，如果探查器同时调用 `SetEnterLeaveFunctionHooks` 和 [ICorProfilerInfo2：： SetEnterLeaveFunctionHooks2](icorprofilerinfo2-setenterleavefunctionhooks2-method.md)，则 `SetEnterLeaveFunctionHooks2` 优先使用。</span><span class="sxs-lookup"><span data-stu-id="824b1-113">Thus, if a profiler calls both `SetEnterLeaveFunctionHooks` and [ICorProfilerInfo2::SetEnterLeaveFunctionHooks2](icorprofilerinfo2-setenterleavefunctionhooks2-method.md), then `SetEnterLeaveFunctionHooks2` takes precedence.</span></span>  
  
 <span data-ttu-id="824b1-114">只能 `SetEnterLeaveFunctionHooks` 从探查器的 [ICorProfilerCallback：： Initialize](icorprofilercallback-initialize-method.md) 回调调用此方法。</span><span class="sxs-lookup"><span data-stu-id="824b1-114">The `SetEnterLeaveFunctionHooks` method can be called only from the profiler's [ICorProfilerCallback::Initialize](icorprofilercallback-initialize-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="824b1-115">要求</span><span class="sxs-lookup"><span data-stu-id="824b1-115">Requirements</span></span>  

 <span data-ttu-id="824b1-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="824b1-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="824b1-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="824b1-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="824b1-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="824b1-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="824b1-119">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="824b1-119">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="824b1-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="824b1-120">See also</span></span>

- [<span data-ttu-id="824b1-121">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="824b1-121">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
