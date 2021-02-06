---
description: 了解详细信息： ICorProfilerInfo2：： SetEnterLeaveFunctionHooks2 方法
title: ICorProfilerInfo2::SetEnterLeaveFunctionHooks2 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.SetEnterLeaveFunctionHooks2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::SetEnterLeaveFunctionHooks2
helpviewer_keywords:
- ICorProfilerInfo2::SetEnterLeaveFunctionHooks2 method [.NET Framework profiling]
- SetEnterLeaveFunctionHooks2 method [.NET Framework profiling]
ms.assetid: 3c26b3e7-f72b-48a5-bf8c-edc122523a4b
topic_type:
- apiref
ms.openlocfilehash: 34f292d9bec4bcd334f824f7e3e1fd127331ba33
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646967"
---
# <a name="icorprofilerinfo2setenterleavefunctionhooks2-method"></a><span data-ttu-id="937eb-103">ICorProfilerInfo2::SetEnterLeaveFunctionHooks2 方法</span><span class="sxs-lookup"><span data-stu-id="937eb-103">ICorProfilerInfo2::SetEnterLeaveFunctionHooks2 Method</span></span>

<span data-ttu-id="937eb-104">指定要在已更新版本的托管函数 "enter"、"leave" 和 "tailcall" 挂钩上调用的探查器实现函数。</span><span class="sxs-lookup"><span data-stu-id="937eb-104">Specifies profiler-implemented functions to be called on the updated versions of the "enter", "leave", and "tailcall" hooks of managed functions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="937eb-105">语法</span><span class="sxs-lookup"><span data-stu-id="937eb-105">Syntax</span></span>  
  
```cpp  
HRESULT SetEnterLeaveFunctionHooks2(  
    [in] FunctionEnter2    *pFuncEnter,  
    [in] FunctionLeave2    *pFuncLeave,  
    [in] FunctionTailcall2 *pFuncTailcall);  
```  
  
## <a name="parameters"></a><span data-ttu-id="937eb-106">参数</span><span class="sxs-lookup"><span data-stu-id="937eb-106">Parameters</span></span>  

 `pFuncEnter`  
 <span data-ttu-id="937eb-107">中指向要用作 [FunctionEnter2](functionenter2-function.md) 回调的实现的指针。</span><span class="sxs-lookup"><span data-stu-id="937eb-107">[in] A pointer to the implementation to be used as the [FunctionEnter2](functionenter2-function.md) callback.</span></span>  
  
 `pFuncLeave`  
 <span data-ttu-id="937eb-108">中指向要用作 [FunctionLeave2](functionleave2-function.md) 回调的实现的指针。</span><span class="sxs-lookup"><span data-stu-id="937eb-108">[in] A pointer to the implementation to be used as the [FunctionLeave2](functionleave2-function.md) callback.</span></span>  
  
 `pFuncTailcall`  
 <span data-ttu-id="937eb-109">中指向要用作 [FunctionTailcall2](functiontailcall2-function.md) 回调的实现的指针。</span><span class="sxs-lookup"><span data-stu-id="937eb-109">[in] A pointer to the implementation to be used as the [FunctionTailcall2](functiontailcall2-function.md) callback.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="937eb-110">备注</span><span class="sxs-lookup"><span data-stu-id="937eb-110">Remarks</span></span>  

 <span data-ttu-id="937eb-111">此 `SetEnterLeaveFunctionHooks2` 方法类似于 [ICorProfilerInfo：： SetEnterLeaveFunctionHooks](icorprofilerinfo-setenterleavefunctionhooks-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="937eb-111">The `SetEnterLeaveFunctionHooks2` method is similar to the [ICorProfilerInfo::SetEnterLeaveFunctionHooks](icorprofilerinfo-setenterleavefunctionhooks-method.md) method.</span></span> <span data-ttu-id="937eb-112">使用前者来指定要用作输入/保留/tailcall 回调的较新版本的函数，并使用后者来指定要用作较早版本的 enter/leave/tailcall 回调的函数。</span><span class="sxs-lookup"><span data-stu-id="937eb-112">Use the former to specify functions to be used as the newer versions of the enter/leave/tailcall callbacks, and the latter to specify functions to be used as the older versions of the enter/leave/tailcall callbacks.</span></span>  
  
 <span data-ttu-id="937eb-113">一次只能有一个回调集处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="937eb-113">Only one set of callbacks may be active at a time.</span></span> <span data-ttu-id="937eb-114">因此，如果探查器调用 `ICorProfilerInfo::SetEnterLeaveFunctionHooks` 和 `SetEnterLeaveFunctionHooks2` ， `SetEnterLeaveFunctionHooks2` 则使用。</span><span class="sxs-lookup"><span data-stu-id="937eb-114">Thus, if a profiler calls both `ICorProfilerInfo::SetEnterLeaveFunctionHooks` and `SetEnterLeaveFunctionHooks2`, `SetEnterLeaveFunctionHooks2` is used.</span></span>  
  
 <span data-ttu-id="937eb-115">`SetEnterLeaveFunctionHooks2`只能从探查器的[ICorProfilerCallback：： Initialize](icorprofilercallback-initialize-method.md)回调调用此方法。</span><span class="sxs-lookup"><span data-stu-id="937eb-115">The `SetEnterLeaveFunctionHooks2` method may be called only from the profiler's [ICorProfilerCallback::Initialize](icorprofilercallback-initialize-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="937eb-116">要求</span><span class="sxs-lookup"><span data-stu-id="937eb-116">Requirements</span></span>  

 <span data-ttu-id="937eb-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="937eb-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="937eb-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="937eb-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="937eb-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="937eb-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="937eb-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="937eb-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="937eb-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="937eb-121">See also</span></span>

- [<span data-ttu-id="937eb-122">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="937eb-122">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="937eb-123">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="937eb-123">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
