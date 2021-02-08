---
description: 了解详细信息： FunctionEnter 函数
title: FunctionEnter 函数
ms.date: 03/30/2017
api_name:
- FunctionEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionEnter
helpviewer_keywords:
- FunctionEnter function [.NET Framework profiling]
ms.assetid: bf4ffa50-4506-4dd4-aa13-a0457b47ca74
topic_type:
- apiref
ms.openlocfilehash: 07b91a81480e453be16e840b89fa822cb91002ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788951"
---
# <a name="functionenter-function"></a><span data-ttu-id="bb1f6-103">FunctionEnter 函数</span><span class="sxs-lookup"><span data-stu-id="bb1f6-103">FunctionEnter Function</span></span>

<span data-ttu-id="bb1f6-104">通知探查器控制正在传递到函数。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-104">Notifies the profiler that control is being passed to a function.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="bb1f6-105">此 `FunctionEnter` 函数在 .NET Framework 版本2.0 中已弃用，其使用将导致性能下降。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-105">The `FunctionEnter` function is deprecated in the .NET Framework version 2.0, and its use will incur a performance penalty.</span></span> <span data-ttu-id="bb1f6-106">改为使用 [FunctionEnter2](functionenter2-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-106">Use the [FunctionEnter2](functionenter2-function.md) function instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb1f6-107">语法</span><span class="sxs-lookup"><span data-stu-id="bb1f6-107">Syntax</span></span>  
  
```cpp  
void __stdcall FunctionEnter (  
    [in]  FunctionID funcID  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bb1f6-108">参数</span><span class="sxs-lookup"><span data-stu-id="bb1f6-108">Parameters</span></span>

- `funcID`

  <span data-ttu-id="bb1f6-109">\[in] 控件传递到的函数的标识符。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-109">\[in] The identifier of the function to which control is passed.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb1f6-110">备注</span><span class="sxs-lookup"><span data-stu-id="bb1f6-110">Remarks</span></span>  

 <span data-ttu-id="bb1f6-111">`FunctionEnter`函数是回调; 必须实现它。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-111">The `FunctionEnter` function is a callback; you must implement it.</span></span> <span data-ttu-id="bb1f6-112">实现必须使用 `__declspec` `naked`) 存储类特性的 (。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-112">The implementation must use the `__declspec`(`naked`) storage-class attribute.</span></span>  
  
 <span data-ttu-id="bb1f6-113">在调用此函数之前，执行引擎不会保存任何注册。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-113">The execution engine does not save any registers before calling this function.</span></span>  
  
- <span data-ttu-id="bb1f6-114">进入时，必须保存使用的所有寄存器，包括 (FPU) 的浮点单元中的寄存器。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-114">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
- <span data-ttu-id="bb1f6-115">退出时，必须通过弹出由其调用方推送的所有参数来还原堆栈。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-115">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
 <span data-ttu-id="bb1f6-116">的实现 `FunctionEnter` 不应被阻止，因为它将延迟垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-116">The implementation of `FunctionEnter` should not block because it will delay garbage collection.</span></span> <span data-ttu-id="bb1f6-117">实现不应尝试垃圾回收，因为堆栈可能不处于垃圾回收友好状态。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-117">The implementation should not attempt a garbage collection because the stack may not be in a garbage collection-friendly state.</span></span> <span data-ttu-id="bb1f6-118">如果尝试垃圾回收，则运行时将被阻止，直到 `FunctionEnter` 返回。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-118">If a garbage collection is attempted, the runtime will block until `FunctionEnter` returns.</span></span>  
  
 <span data-ttu-id="bb1f6-119">此外，该 `FunctionEnter` 函数不得调入托管代码或以任何方式导致托管的内存分配。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-119">Also, the `FunctionEnter` function must not call into managed code or in any way cause a managed memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bb1f6-120">要求</span><span class="sxs-lookup"><span data-stu-id="bb1f6-120">Requirements</span></span>  

 <span data-ttu-id="bb1f6-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bb1f6-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb1f6-122">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="bb1f6-122">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="bb1f6-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bb1f6-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bb1f6-124">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="bb1f6-124">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb1f6-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="bb1f6-125">See also</span></span>

- [<span data-ttu-id="bb1f6-126">FunctionEnter2 函数</span><span class="sxs-lookup"><span data-stu-id="bb1f6-126">FunctionEnter2 Function</span></span>](functionenter2-function.md)
- [<span data-ttu-id="bb1f6-127">FunctionLeave2 函数</span><span class="sxs-lookup"><span data-stu-id="bb1f6-127">FunctionLeave2 Function</span></span>](functionleave2-function.md)
- [<span data-ttu-id="bb1f6-128">FunctionTailcall2 函数</span><span class="sxs-lookup"><span data-stu-id="bb1f6-128">FunctionTailcall2 Function</span></span>](functiontailcall2-function.md)
- [<span data-ttu-id="bb1f6-129">SetEnterLeaveFunctionHooks2 方法</span><span class="sxs-lookup"><span data-stu-id="bb1f6-129">SetEnterLeaveFunctionHooks2 Method</span></span>](icorprofilerinfo2-setenterleavefunctionhooks2-method.md)
- [<span data-ttu-id="bb1f6-130">分析全局静态函数</span><span class="sxs-lookup"><span data-stu-id="bb1f6-130">Profiling Global Static Functions</span></span>](profiling-global-static-functions.md)
