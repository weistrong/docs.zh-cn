---
description: 了解详细信息： FunctionEnter3 函数
title: FunctionEnter3 函数
ms.date: 03/30/2017
api_name:
- FunctionEnter3
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionEnter3
helpviewer_keywords:
- FunctionEnter3 function [.NET Framework profiling]
ms.assetid: ef782c53-dae7-4990-b4ad-fddb1e690d4e
topic_type:
- apiref
ms.openlocfilehash: 664b0ca5b40937eaa129e6843e55024802befbb7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648670"
---
# <a name="functionenter3-function"></a><span data-ttu-id="08807-103">FunctionEnter3 函数</span><span class="sxs-lookup"><span data-stu-id="08807-103">FunctionEnter3 Function</span></span>

<span data-ttu-id="08807-104">通知探查器控制正在传递到函数。</span><span class="sxs-lookup"><span data-stu-id="08807-104">Notifies the profiler that control is being passed to a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08807-105">语法</span><span class="sxs-lookup"><span data-stu-id="08807-105">Syntax</span></span>  
  
```cpp  
void __stdcall FunctionEnter3(FunctionOrRemappedID functionOrRemappedID);  
```  
  
## <a name="parameters"></a><span data-ttu-id="08807-106">参数</span><span class="sxs-lookup"><span data-stu-id="08807-106">Parameters</span></span>

- `functionOrRemappedID`

  <span data-ttu-id="08807-107">\[in] 控件传递到的函数的标识符。</span><span class="sxs-lookup"><span data-stu-id="08807-107">\[in] The identifier of the function to which control is passed.</span></span>

## <a name="remarks"></a><span data-ttu-id="08807-108">备注</span><span class="sxs-lookup"><span data-stu-id="08807-108">Remarks</span></span>  

 <span data-ttu-id="08807-109">`FunctionEnter3`回调函数将在调用函数时通知探查器，但不支持参数检查。</span><span class="sxs-lookup"><span data-stu-id="08807-109">The `FunctionEnter3` callback function notifies the profiler as functions are being called, but does not support argument inspection.</span></span> <span data-ttu-id="08807-110">使用 [ICorProfilerInfo3：： SetEnterLeaveFunctionHooks3 方法](icorprofilerinfo3-setenterleavefunctionhooks3-method.md) 注册此函数的实现。</span><span class="sxs-lookup"><span data-stu-id="08807-110">Use the [ICorProfilerInfo3::SetEnterLeaveFunctionHooks3 method](icorprofilerinfo3-setenterleavefunctionhooks3-method.md) to register your implementation of this function.</span></span>  
  
 <span data-ttu-id="08807-111">`FunctionEnter3`函数是回调; 必须实现它。</span><span class="sxs-lookup"><span data-stu-id="08807-111">The `FunctionEnter3` function is a callback; you must implement it.</span></span> <span data-ttu-id="08807-112">实现必须使用 `__declspec(naked)` 存储类特性。</span><span class="sxs-lookup"><span data-stu-id="08807-112">The implementation must use the `__declspec(naked)` storage-class attribute.</span></span>  
  
 <span data-ttu-id="08807-113">在调用此函数之前，执行引擎不会保存任何注册。</span><span class="sxs-lookup"><span data-stu-id="08807-113">The execution engine does not save any registers before calling this function.</span></span>  
  
- <span data-ttu-id="08807-114">进入时，必须保存使用的所有寄存器，包括 (FPU) 的浮点单元中的寄存器。</span><span class="sxs-lookup"><span data-stu-id="08807-114">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
- <span data-ttu-id="08807-115">退出时，必须通过弹出由其调用方推送的所有参数来还原堆栈。</span><span class="sxs-lookup"><span data-stu-id="08807-115">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08807-116">要求</span><span class="sxs-lookup"><span data-stu-id="08807-116">Requirements</span></span>  

 <span data-ttu-id="08807-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="08807-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="08807-118">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="08807-118">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="08807-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="08807-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="08807-120">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="08807-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08807-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="08807-121">See also</span></span>

- [<span data-ttu-id="08807-122">FunctionLeave3</span><span class="sxs-lookup"><span data-stu-id="08807-122">FunctionLeave3</span></span>](functionleave3-function.md)
- [<span data-ttu-id="08807-123">FunctionTailcall3</span><span class="sxs-lookup"><span data-stu-id="08807-123">FunctionTailcall3</span></span>](functiontailcall3-function.md)
- [<span data-ttu-id="08807-124">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="08807-124">FunctionEnter3WithInfo</span></span>](functionenter3withinfo-function.md)
- [<span data-ttu-id="08807-125">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="08807-125">FunctionLeave3WithInfo</span></span>](functionleave3withinfo-function.md)
- [<span data-ttu-id="08807-126">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="08807-126">FunctionTailcall3WithInfo</span></span>](functiontailcall3withinfo-function.md)
- [<span data-ttu-id="08807-127">SetEnterLeaveFunctionHooks3</span><span class="sxs-lookup"><span data-stu-id="08807-127">SetEnterLeaveFunctionHooks3</span></span>](icorprofilerinfo3-setenterleavefunctionhooks3-method.md)
- [<span data-ttu-id="08807-128">SetEnterLeaveFunctionHooks3WithInfo</span><span class="sxs-lookup"><span data-stu-id="08807-128">SetEnterLeaveFunctionHooks3WithInfo</span></span>](icorprofilerinfo3-setenterleavefunctionhooks3withinfo-method.md)
- [<span data-ttu-id="08807-129">SetFunctionIDMapper</span><span class="sxs-lookup"><span data-stu-id="08807-129">SetFunctionIDMapper</span></span>](icorprofilerinfo-setfunctionidmapper-method.md)
- [<span data-ttu-id="08807-130">SetFunctionIDMapper2</span><span class="sxs-lookup"><span data-stu-id="08807-130">SetFunctionIDMapper2</span></span>](icorprofilerinfo3-setfunctionidmapper2-method.md)
- [<span data-ttu-id="08807-131">分析全局静态函数</span><span class="sxs-lookup"><span data-stu-id="08807-131">Profiling Global Static Functions</span></span>](profiling-global-static-functions.md)
