---
description: 了解详细信息： FunctionTailcall 函数
title: FunctionTailcall 函数
ms.date: 03/30/2017
api_name:
- FunctionTailcall
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionTailcall
helpviewer_keywords:
- FunctionTailcall function [.NET Framework profiling]
ms.assetid: 66347e03-9a97-41e8-8f9d-89b80803f7b5
topic_type:
- apiref
ms.openlocfilehash: 8da3efde7d925fdb02232ca98662f8d6a6fd0adf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687306"
---
# <a name="functiontailcall-function"></a><span data-ttu-id="9aaac-103">FunctionTailcall 函数</span><span class="sxs-lookup"><span data-stu-id="9aaac-103">FunctionTailcall Function</span></span>

<span data-ttu-id="9aaac-104">通知探查器，当前正在执行的函数即将对另一个函数执行尾调用。</span><span class="sxs-lookup"><span data-stu-id="9aaac-104">Notifies the profiler that the currently executing function is about to perform a tail call to another function.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="9aaac-105">`FunctionTailcall`.NET Framework 版本2.0 中不推荐使用该函数。</span><span class="sxs-lookup"><span data-stu-id="9aaac-105">The `FunctionTailcall` function is deprecated in the .NET Framework version 2.0.</span></span> <span data-ttu-id="9aaac-106">它将继续运行，但会导致性能下降。</span><span class="sxs-lookup"><span data-stu-id="9aaac-106">It will continue to work, but will incur a performance penalty.</span></span> <span data-ttu-id="9aaac-107">改为使用 [FunctionTailcall2](functiontailcall2-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="9aaac-107">Use the [FunctionTailcall2](functiontailcall2-function.md) function instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9aaac-108">语法</span><span class="sxs-lookup"><span data-stu-id="9aaac-108">Syntax</span></span>  
  
```cpp
void __stdcall FunctionTailcall (  
    [in] FunctionID funcID  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9aaac-109">参数</span><span class="sxs-lookup"><span data-stu-id="9aaac-109">Parameters</span></span>

- `funcID`

  <span data-ttu-id="9aaac-110">\[in] 要进行尾调用的当前正在执行的函数的标识符。</span><span class="sxs-lookup"><span data-stu-id="9aaac-110">\[in] The identifier of the currently executing function that is about to make a tail call.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aaac-111">备注</span><span class="sxs-lookup"><span data-stu-id="9aaac-111">Remarks</span></span>  

 <span data-ttu-id="9aaac-112">尾调用的目标函数将使用当前堆栈帧，并将直接返回到进行尾调用的函数的调用方。</span><span class="sxs-lookup"><span data-stu-id="9aaac-112">The target function of the tail call will use the current stack frame, and will return directly to the caller of the function that made the tail call.</span></span> <span data-ttu-id="9aaac-113">这意味着将不会为作为尾调用目标的函数发出 [FunctionLeave](functionleave-function.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="9aaac-113">This means that a [FunctionLeave](functionleave-function.md) callback will not be issued for a function that is the target of a tail call.</span></span>  
  
 <span data-ttu-id="9aaac-114">`FunctionTailcall`函数是回调; 必须实现它。</span><span class="sxs-lookup"><span data-stu-id="9aaac-114">The `FunctionTailcall` function is a callback; you must implement it.</span></span> <span data-ttu-id="9aaac-115">实现必须使用 `__declspec` `naked`) 存储类特性的 (。</span><span class="sxs-lookup"><span data-stu-id="9aaac-115">The implementation must use the `__declspec`(`naked`) storage-class attribute.</span></span>  
  
 <span data-ttu-id="9aaac-116">在调用此函数之前，执行引擎不会保存任何注册。</span><span class="sxs-lookup"><span data-stu-id="9aaac-116">The execution engine does not save any registers before calling this function.</span></span>  
  
- <span data-ttu-id="9aaac-117">进入时，必须保存使用的所有寄存器，包括 (FPU) 的浮点单元中的寄存器。</span><span class="sxs-lookup"><span data-stu-id="9aaac-117">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
- <span data-ttu-id="9aaac-118">退出时，必须通过弹出由其调用方推送的所有参数来还原堆栈。</span><span class="sxs-lookup"><span data-stu-id="9aaac-118">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
 <span data-ttu-id="9aaac-119">的实现 `FunctionTailcall` 不应被阻止，因为它将延迟垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="9aaac-119">The implementation of `FunctionTailcall` should not block because it will delay garbage collection.</span></span> <span data-ttu-id="9aaac-120">实现不应尝试垃圾回收，因为堆栈可能不处于垃圾回收友好状态。</span><span class="sxs-lookup"><span data-stu-id="9aaac-120">The implementation should not attempt a garbage collection because the stack may not be in a garbage collection-friendly state.</span></span> <span data-ttu-id="9aaac-121">如果尝试垃圾回收，则运行时将被阻止，直到 `FunctionTailcall` 返回。</span><span class="sxs-lookup"><span data-stu-id="9aaac-121">If a garbage collection is attempted, the runtime will block until `FunctionTailcall` returns.</span></span>  
  
 <span data-ttu-id="9aaac-122">此外，该 `FunctionTailcall` 函数不得调入托管代码或以任何方式导致托管的内存分配。</span><span class="sxs-lookup"><span data-stu-id="9aaac-122">Also, the `FunctionTailcall` function must not call into managed code or in any way cause a managed memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9aaac-123">要求</span><span class="sxs-lookup"><span data-stu-id="9aaac-123">Requirements</span></span>  

 <span data-ttu-id="9aaac-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9aaac-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9aaac-125">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="9aaac-125">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="9aaac-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9aaac-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9aaac-127">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="9aaac-127">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9aaac-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="9aaac-128">See also</span></span>

- [<span data-ttu-id="9aaac-129">FunctionEnter2 函数</span><span class="sxs-lookup"><span data-stu-id="9aaac-129">FunctionEnter2 Function</span></span>](functionenter2-function.md)
- [<span data-ttu-id="9aaac-130">FunctionLeave2 函数</span><span class="sxs-lookup"><span data-stu-id="9aaac-130">FunctionLeave2 Function</span></span>](functionleave2-function.md)
- [<span data-ttu-id="9aaac-131">SetEnterLeaveFunctionHooks2 方法</span><span class="sxs-lookup"><span data-stu-id="9aaac-131">SetEnterLeaveFunctionHooks2 Method</span></span>](icorprofilerinfo2-setenterleavefunctionhooks2-method.md)
- [<span data-ttu-id="9aaac-132">分析全局静态函数</span><span class="sxs-lookup"><span data-stu-id="9aaac-132">Profiling Global Static Functions</span></span>](profiling-global-static-functions.md)
