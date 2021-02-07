---
description: 了解详细信息： StackSnapshotCallback 函数
title: StackSnapshotCallback 函数
ms.date: 03/30/2017
api_name:
- StackSnapshotCallback
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- StackSnapshotCallback
helpviewer_keywords:
- StackSnapshotCallback function [.NET Framework profiling]
ms.assetid: d0f235b2-91fe-4f82-b7d5-e5c64186eea8
topic_type:
- apiref
ms.openlocfilehash: a49588bc3277956acad612afd0fcab3fa7edffbd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736838"
---
# <a name="stacksnapshotcallback-function"></a><span data-ttu-id="0f1c5-103">StackSnapshotCallback 函数</span><span class="sxs-lookup"><span data-stu-id="0f1c5-103">StackSnapshotCallback Function</span></span>

<span data-ttu-id="0f1c5-104">在堆栈遍历期间，为探查器提供有关每个托管帧和每个托管帧的每个运行的信息，由 [ICorProfilerInfo2：:D ostacksnapshot](icorprofilerinfo2-dostacksnapshot-method.md) 方法启动。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-104">Provides the profiler with information about each managed frame and each run of unmanaged frames on the stack during a stack walk, which is initiated by the [ICorProfilerInfo2::DoStackSnapshot](icorprofilerinfo2-dostacksnapshot-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f1c5-105">语法</span><span class="sxs-lookup"><span data-stu-id="0f1c5-105">Syntax</span></span>  
  
```cpp  
HRESULT __stdcall StackSnapshotCallback (  
    [in] FunctionID funcId,  
    [in] UINT_PTR ip,  
    [in] COR_PRF_FRAME_INFO frameInfo,  
    [in] ULONG32 contextSize,  
    [in] BYTE context[],  
    [in] void *clientData  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0f1c5-106">参数</span><span class="sxs-lookup"><span data-stu-id="0f1c5-106">Parameters</span></span>  

 `funcId`  
 <span data-ttu-id="0f1c5-107">中如果此值为零，则此回调适用于非托管帧的运行;否则，它是托管函数的标识符，此回调适用于托管帧。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-107">[in] If this value is zero, this callback is for a run of unmanaged frames; otherwise, it is the identifier of a managed function and this callback is for a managed frame.</span></span>  
  
 `ip`  
 <span data-ttu-id="0f1c5-108">中帧中的本机代码指令指针的值。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-108">[in] The value of the native code instruction pointer in the frame.</span></span>  
  
 `frameInfo`  
 <span data-ttu-id="0f1c5-109">中一个 `COR_PRF_FRAME_INFO` 值，该值引用有关堆栈帧的信息。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-109">[in] A `COR_PRF_FRAME_INFO` value that references information about the stack frame.</span></span> <span data-ttu-id="0f1c5-110">此值仅在此回调期间有效。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-110">This value is valid for use only during this callback.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="0f1c5-111">中 `CONTEXT` 由参数引用的结构的大小 `context` 。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-111">[in] The size of the `CONTEXT` structure, which is referenced by the `context` parameter.</span></span>  
  
 `context`  
 <span data-ttu-id="0f1c5-112">中指向 Win32 `CONTEXT` 结构的指针，该结构表示此帧的 CPU 的状态。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-112">[in] A pointer to a Win32 `CONTEXT` structure that represents the state of the CPU for this frame.</span></span>  
  
 <span data-ttu-id="0f1c5-113">`context`仅当传入 COR_PRF_SNAPSHOT_CONTEXT 标志时，此参数才有效 `ICorProfilerInfo2::DoStackSnapshot` 。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-113">The `context` parameter is valid only if the COR_PRF_SNAPSHOT_CONTEXT flag was passed in `ICorProfilerInfo2::DoStackSnapshot`.</span></span>  
  
 `clientData`  
 <span data-ttu-id="0f1c5-114">中指向客户端数据的指针，该数据是通过从直接传递的 `ICorProfilerInfo2::DoStackSnapshot` 。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-114">[in] A pointer to the client data, which is passed straight through from `ICorProfilerInfo2::DoStackSnapshot`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0f1c5-115">备注</span><span class="sxs-lookup"><span data-stu-id="0f1c5-115">Remarks</span></span>  

 <span data-ttu-id="0f1c5-116">`StackSnapshotCallback`函数由探查器编写器实现。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-116">The `StackSnapshotCallback` function is implemented by the profiler writer.</span></span> <span data-ttu-id="0f1c5-117">必须限制中完成的工作的复杂性 `StackSnapshotCallback` 。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-117">You must limit the complexity of work done in `StackSnapshotCallback`.</span></span> <span data-ttu-id="0f1c5-118">例如， `ICorProfilerInfo2::DoStackSnapshot` 以异步方式使用时，目标线程可能会持有锁。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-118">For example, when using `ICorProfilerInfo2::DoStackSnapshot` in an asynchronous manner, the target thread may be holding locks.</span></span> <span data-ttu-id="0f1c5-119">如果中 `StackSnapshotCallback` 的代码需要相同的锁，则可能会不幸死锁。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-119">If code within `StackSnapshotCallback` requires the same locks, a deadlock could ensue.</span></span>  
  
 <span data-ttu-id="0f1c5-120">`ICorProfilerInfo2::DoStackSnapshot`方法对 `StackSnapshotCallback` 每个托管帧调用一次函数，或在每次运行非托管帧时调用函数。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-120">The `ICorProfilerInfo2::DoStackSnapshot` method calls the `StackSnapshotCallback` function once per managed frame or once per run of unmanaged frames.</span></span> <span data-ttu-id="0f1c5-121">如果 `StackSnapshotCallback` 调用来运行非托管帧，则探查器可能会使用参数) 引用 (注册上下文 `context` 来执行其自己的非托管堆栈遍历。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-121">If `StackSnapshotCallback` is called for a run of unmanaged frames, the profiler may use the register context (referenced by the `context` parameter) to perform its own unmanaged stack walk.</span></span> <span data-ttu-id="0f1c5-122">在这种情况下，Win32 `CONTEXT` 结构表示在非托管帧运行内最近推送的帧的 CPU 状态。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-122">In this case, the Win32 `CONTEXT` structure represents the CPU state for the most recently pushed frame within the run of unmanaged frames.</span></span> <span data-ttu-id="0f1c5-123">尽管 Win32 `CONTEXT` 结构包含所有寄存器的值，但你只应依赖于堆栈指针寄存器、帧指针寄存器、指令指针寄存器和非易失性 (的值，这些值将保留) 整数寄存器。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-123">Although the Win32 `CONTEXT` structure includes values for all registers, you should rely only on the values of the stack pointer register, frame pointer register, instruction pointer register, and the nonvolatile (that is, preserved) integer registers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f1c5-124">要求</span><span class="sxs-lookup"><span data-stu-id="0f1c5-124">Requirements</span></span>  

 <span data-ttu-id="0f1c5-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0f1c5-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f1c5-126">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="0f1c5-126">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="0f1c5-127">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0f1c5-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0f1c5-128">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0f1c5-128">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f1c5-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="0f1c5-129">See also</span></span>

- [<span data-ttu-id="0f1c5-130">DoStackSnapshot 方法</span><span class="sxs-lookup"><span data-stu-id="0f1c5-130">DoStackSnapshot Method</span></span>](icorprofilerinfo2-dostacksnapshot-method.md)
- [<span data-ttu-id="0f1c5-131">分析全局静态函数</span><span class="sxs-lookup"><span data-stu-id="0f1c5-131">Profiling Global Static Functions</span></span>](profiling-global-static-functions.md)
