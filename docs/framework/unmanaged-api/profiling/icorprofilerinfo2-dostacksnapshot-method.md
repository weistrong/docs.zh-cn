---
description: 了解详细信息： ICorProfilerInfo2：:D oStackSnapshot 方法
title: ICorProfilerInfo2::DoStackSnapshot 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.DoStackSnapshot
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::DoStackSnapshot
helpviewer_keywords:
- ICorProfilerInfo2::DoStackSnapshot method [.NET Framework profiling]
- DoStackSnapshot method [.NET Framework profiling]
ms.assetid: 287b11e9-7c52-4a13-ba97-751203fa97f4
topic_type:
- apiref
ms.openlocfilehash: e30e11dfe04da1e7a5adfef004036507b724963d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753245"
---
# <a name="icorprofilerinfo2dostacksnapshot-method"></a><span data-ttu-id="a2366-103">ICorProfilerInfo2::DoStackSnapshot 方法</span><span class="sxs-lookup"><span data-stu-id="a2366-103">ICorProfilerInfo2::DoStackSnapshot Method</span></span>

<span data-ttu-id="a2366-104">遍历指定线程的堆栈上的托管帧，并通过回调将信息发送到探查器。</span><span class="sxs-lookup"><span data-stu-id="a2366-104">Walks the managed frames on the stack for the specified thread, and sends information to the profiler through a callback.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a2366-105">语法</span><span class="sxs-lookup"><span data-stu-id="a2366-105">Syntax</span></span>  
  
```cpp  
HRESULT DoStackSnapshot(  
    [in] ThreadID thread,  
    [in] StackSnapshotCallback *callback,  
    [in] ULONG32 infoFlags,  
    [in] void *clientData,  
    [in, size_is(contextSize), length_is(contextSize)] BYTE context[],  
    [in] ULONG32 contextSize);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a2366-106">参数</span><span class="sxs-lookup"><span data-stu-id="a2366-106">Parameters</span></span>  

 `thread`  
 <span data-ttu-id="a2366-107">中目标线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="a2366-107">[in] The ID of the target thread.</span></span>  
  
 <span data-ttu-id="a2366-108">在中传递 null 会 `thread` 生成当前线程的快照。</span><span class="sxs-lookup"><span data-stu-id="a2366-108">Passing null in `thread` yields a snapshot of the current thread.</span></span> <span data-ttu-id="a2366-109">如果 `ThreadID` 传递了其他线程的，则公共语言运行时 (CLR) 挂起该线程，执行快照，然后恢复。</span><span class="sxs-lookup"><span data-stu-id="a2366-109">If a `ThreadID` of a different thread is passed, the common language runtime (CLR) suspends that thread, performs the snapshot, and resumes.</span></span>  
  
 `callback`  
 <span data-ttu-id="a2366-110">中指向 [StackSnapshotCallback](stacksnapshotcallback-function.md) 方法的实现的指针，CLR 调用此方法为探查器提供有关每个托管帧以及每次运行非托管帧的信息。</span><span class="sxs-lookup"><span data-stu-id="a2366-110">[in] A pointer to the implementation of the [StackSnapshotCallback](stacksnapshotcallback-function.md) method, which is called by the CLR to provide the profiler with information on each managed frame and each run of unmanaged frames.</span></span>  
  
 <span data-ttu-id="a2366-111">`StackSnapshotCallback`方法由探查器编写器实现。</span><span class="sxs-lookup"><span data-stu-id="a2366-111">The `StackSnapshotCallback` method is implemented by the profiler writer.</span></span>  
  
 `infoFlags`  
 <span data-ttu-id="a2366-112">中一个 [COR_PRF_SNAPSHOT_INFO](cor-prf-snapshot-info-enumeration.md) 枚举的值，该值指定要为每个帧传递回的数据量 `StackSnapshotCallback` 。</span><span class="sxs-lookup"><span data-stu-id="a2366-112">[in] A value of the [COR_PRF_SNAPSHOT_INFO](cor-prf-snapshot-info-enumeration.md) enumeration, which specifies the amount of data to be passed back for each frame by `StackSnapshotCallback`.</span></span>  
  
 `clientData`  
 <span data-ttu-id="a2366-113">中指向客户端数据的指针，它将直接传递给 `StackSnapshotCallback` 回调函数。</span><span class="sxs-lookup"><span data-stu-id="a2366-113">[in] A pointer to the client data, which is passed straight through to the `StackSnapshotCallback` callback function.</span></span>  
  
 `context`  
 <span data-ttu-id="a2366-114">中指向 Win32 结构的指针 `CONTEXT` ，该结构用于对堆栈审核进行种子设定。</span><span class="sxs-lookup"><span data-stu-id="a2366-114">[in] A pointer to a Win32 `CONTEXT` structure, which is used to seed the stack walk.</span></span> <span data-ttu-id="a2366-115">Win32 `CONTEXT` 结构包含 cpu 寄存器的值，表示特定时刻的 cpu 状态。</span><span class="sxs-lookup"><span data-stu-id="a2366-115">The Win32 `CONTEXT` structure contains values of the CPU registers and represents the state of the CPU at a particular moment in time.</span></span>  
  
 <span data-ttu-id="a2366-116">如果堆栈顶部是非托管的帮助程序代码，则 seed 有助于 CLR 确定开始堆栈审核的位置;否则，将忽略种子。</span><span class="sxs-lookup"><span data-stu-id="a2366-116">The seed helps the CLR determine where to begin the stack walk, if the top of the stack is unmanaged helper code; otherwise, the seed is ignored.</span></span> <span data-ttu-id="a2366-117">必须为异步审核提供种子。</span><span class="sxs-lookup"><span data-stu-id="a2366-117">A seed must be supplied for an asynchronous walk.</span></span> <span data-ttu-id="a2366-118">如果执行同步审核，则不需要种子。</span><span class="sxs-lookup"><span data-stu-id="a2366-118">If you are doing a synchronous walk, no seed is necessary.</span></span>  
  
 <span data-ttu-id="a2366-119">`context`仅当在参数中传递了 COR_PRF_SNAPSHOT_CONTEXT 标志时，此参数才有效 `infoFlags` 。</span><span class="sxs-lookup"><span data-stu-id="a2366-119">The `context` parameter is valid only if the COR_PRF_SNAPSHOT_CONTEXT flag was passed in the `infoFlags` parameter.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="a2366-120">中 `CONTEXT` 由参数引用的结构的大小 `context` 。</span><span class="sxs-lookup"><span data-stu-id="a2366-120">[in] The size of the `CONTEXT` structure, which is referenced by the `context` parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a2366-121">备注</span><span class="sxs-lookup"><span data-stu-id="a2366-121">Remarks</span></span>  

 <span data-ttu-id="a2366-122">传递 null 以 `thread` 生成当前线程的快照。</span><span class="sxs-lookup"><span data-stu-id="a2366-122">Passing null for `thread` yields a snapshot of the current thread.</span></span> <span data-ttu-id="a2366-123">仅当目标线程在此时挂起时，才能对其他线程执行快照操作。</span><span class="sxs-lookup"><span data-stu-id="a2366-123">Snapshots can be taken of other threads only if the target thread is suspended at the time.</span></span>  
  
 <span data-ttu-id="a2366-124">当探查器需要遍历堆栈时，它会调用 `DoStackSnapshot` 。</span><span class="sxs-lookup"><span data-stu-id="a2366-124">When the profiler wants to walk the stack, it calls `DoStackSnapshot`.</span></span> <span data-ttu-id="a2366-125">在 CLR 从该调用返回之前，它将调用 `StackSnapshotCallback` 几次，一次针对每个托管帧 (或运行堆栈上的非托管帧) 。</span><span class="sxs-lookup"><span data-stu-id="a2366-125">Before the CLR returns from that call, it calls your `StackSnapshotCallback` several times, once for each managed frame (or run of unmanaged frames) on the stack.</span></span> <span data-ttu-id="a2366-126">如果遇到非托管帧，则必须自行对其进行演练。</span><span class="sxs-lookup"><span data-stu-id="a2366-126">When unmanaged frames are encountered, you must walk them yourself.</span></span>  
  
 <span data-ttu-id="a2366-127">遍历堆栈的顺序与将帧推送到堆栈上的顺序相反：首先推送的叶 (上推) 帧，main (第一次推送) 帧。</span><span class="sxs-lookup"><span data-stu-id="a2366-127">The order in which the stack is walked is the reverse of how the frames were pushed onto the stack: leaf (last-pushed) frame first, main (first-pushed) frame last.</span></span>  
  
 <span data-ttu-id="a2366-128">有关如何对探查器进行编程以遍历托管堆栈的详细信息，请参阅 [.NET Framework 2.0：基础和更高版本中的探查器堆栈遍历](/previous-versions/dotnet/articles/bb264782(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="a2366-128">For more information about how to program the profiler to walk managed stacks, see [Profiler Stack Walking in the .NET Framework 2.0: Basics and Beyond](/previous-versions/dotnet/articles/bb264782(v=msdn.10)).</span></span>  
  
 <span data-ttu-id="a2366-129">堆栈审核可以是同步的，也可以是异步的，如以下各节所述。</span><span class="sxs-lookup"><span data-stu-id="a2366-129">A stack walk can be synchronous or asynchronous, as explained in the following sections.</span></span>  
  
## <a name="synchronous-stack-walk"></a><span data-ttu-id="a2366-130">同步堆栈遍历</span><span class="sxs-lookup"><span data-stu-id="a2366-130">Synchronous Stack Walk</span></span>  

 <span data-ttu-id="a2366-131">同步堆栈审核包括遍历当前线程的堆栈以响应回调。</span><span class="sxs-lookup"><span data-stu-id="a2366-131">A synchronous stack walk involves walking the stack of the current thread in response to a callback.</span></span> <span data-ttu-id="a2366-132">它不需要进行种子设定或暂停。</span><span class="sxs-lookup"><span data-stu-id="a2366-132">It does not require seeding or suspending.</span></span>  
  
 <span data-ttu-id="a2366-133">当你在为响应调用某个探查器的 [ICorProfilerCallback](icorprofilercallback-interface.md) (或 [ICorProfilerCallback2](icorprofilercallback2-interface.md)) 方法的 CLR 时进行同步调用，你可以调用 `DoStackSnapshot` 来遍历当前线程的堆栈。</span><span class="sxs-lookup"><span data-stu-id="a2366-133">You make a synchronous call when, in response to the CLR calling one of your profiler's [ICorProfilerCallback](icorprofilercallback-interface.md) (or [ICorProfilerCallback2](icorprofilercallback2-interface.md)) methods, you call `DoStackSnapshot` to walk the stack of the current thread.</span></span> <span data-ttu-id="a2366-134">当你想要在通知（如 [ICorProfilerCallback：： ObjectAllocated](icorprofilercallback-objectallocated-method.md)）上查看堆栈的外观时，这非常有用。</span><span class="sxs-lookup"><span data-stu-id="a2366-134">This is useful when you want to see what the stack looks like at a notification such as [ICorProfilerCallback::ObjectAllocated](icorprofilercallback-objectallocated-method.md).</span></span> <span data-ttu-id="a2366-135">只需 `DoStackSnapshot` 从方法中调用 `ICorProfilerCallback` ，并在和参数中传递 null `context` `thread` 。</span><span class="sxs-lookup"><span data-stu-id="a2366-135">You just call `DoStackSnapshot` from within your `ICorProfilerCallback` method, passing null in the `context` and `thread` parameters.</span></span>  
  
## <a name="asynchronous-stack-walk"></a><span data-ttu-id="a2366-136">异步堆栈遍历</span><span class="sxs-lookup"><span data-stu-id="a2366-136">Asynchronous Stack Walk</span></span>  

 <span data-ttu-id="a2366-137">异步堆栈审核需要遍历不同线程的堆栈，或遍历当前线程的堆栈，而不是响应回调，但通过劫持当前线程的指令指针。</span><span class="sxs-lookup"><span data-stu-id="a2366-137">An asynchronous stack walk entails walking the stack of a different thread, or walking the stack of the current thread, not in response to a callback, but by hijacking the current thread's instruction pointer.</span></span> <span data-ttu-id="a2366-138">如果堆栈顶部是非托管代码，而该代码不属于平台调用 (PInvoke) 或 COM 调用，但是 CLR 本身中的帮助程序代码，则异步审核需要种子。</span><span class="sxs-lookup"><span data-stu-id="a2366-138">An asynchronous walk requires a seed if the top of the stack is unmanaged code that is not part of a platform invoke (PInvoke) or COM call, but helper code in the CLR itself.</span></span> <span data-ttu-id="a2366-139">例如，执行实时 (JIT) 编译或垃圾回收的代码都是帮助器代码。</span><span class="sxs-lookup"><span data-stu-id="a2366-139">For example, code that does just-in-time (JIT) compiling or garbage collection is helper code.</span></span>  
  
 <span data-ttu-id="a2366-140">您可以通过直接挂起目标线程并自己遍历其堆栈来获取种子，直到找到最顶层的托管帧。</span><span class="sxs-lookup"><span data-stu-id="a2366-140">You obtain a seed by directly suspending the target thread and walking its stack yourself, until you find the topmost managed frame.</span></span> <span data-ttu-id="a2366-141">挂起目标线程后，获取目标线程的当前注册上下文。</span><span class="sxs-lookup"><span data-stu-id="a2366-141">After the target thread is suspended, get the target thread's current register context.</span></span> <span data-ttu-id="a2366-142">接下来，通过调用 [ICorProfilerInfo：： GetFunctionFromIP](icorprofilerinfo-getfunctionfromip-method.md) 确定寄存器上下文是否指向非托管代码，如果它返回的 `FunctionID` 值等于零，则该框架为非托管代码。</span><span class="sxs-lookup"><span data-stu-id="a2366-142">Next, determine whether the register context points to unmanaged code by calling [ICorProfilerInfo::GetFunctionFromIP](icorprofilerinfo-getfunctionfromip-method.md) — if it returns a `FunctionID` equal to zero, the frame is unmanaged code.</span></span> <span data-ttu-id="a2366-143">现在，遍历堆栈直至到达第一个托管帧，然后基于该帧的注册上下文计算种子上下文。</span><span class="sxs-lookup"><span data-stu-id="a2366-143">Now, walk the stack until you reach the first managed frame, and then calculate the seed context based on the register context for that frame.</span></span>  
  
 <span data-ttu-id="a2366-144">调用 `DoStackSnapshot` 种子上下文以开始异步堆栈遍历。</span><span class="sxs-lookup"><span data-stu-id="a2366-144">Call `DoStackSnapshot` with your seed context to begin the asynchronous stack walk.</span></span> <span data-ttu-id="a2366-145">如果未提供种子， `DoStackSnapshot` 可能会跳过堆栈顶部的托管帧，因此，将为您提供不完整的堆栈审核。</span><span class="sxs-lookup"><span data-stu-id="a2366-145">If you do not supply a seed, `DoStackSnapshot` might skip managed frames at the top of the stack and, consequently, will give you an incomplete stack walk.</span></span> <span data-ttu-id="a2366-146">如果提供了种子，则它必须指向 JIT 编译的或本机图像生成器 ( # A0) 生成的代码;否则， `DoStackSnapshot` 将返回失败代码 CORPROF_E_STACKSNAPSHOT_UNMANAGED_CTX。</span><span class="sxs-lookup"><span data-stu-id="a2366-146">If you do supply a seed, it must point to JIT-compiled or Native Image Generator (Ngen.exe)-generated code; otherwise, `DoStackSnapshot` returns the failure code, CORPROF_E_STACKSNAPSHOT_UNMANAGED_CTX.</span></span>  
  
 <span data-ttu-id="a2366-147">异步堆栈审核可能会导致死锁或访问冲突，除非你遵循以下准则：</span><span class="sxs-lookup"><span data-stu-id="a2366-147">Asynchronous stack walks can easily cause deadlocks or access violations, unless you follow these guidelines:</span></span>  
  
- <span data-ttu-id="a2366-148">当你直接挂起线程时，请记住，只有从未运行托管代码的线程才能挂起另一个线程。</span><span class="sxs-lookup"><span data-stu-id="a2366-148">When you directly suspend threads, remember that only a thread that has never run managed code can suspend another thread.</span></span>  
  
- <span data-ttu-id="a2366-149">始终在 [ICorProfilerCallback：： ThreadDestroyed](icorprofilercallback-threaddestroyed-method.md) 回调中阻止，直到该线程的堆栈遍历完成。</span><span class="sxs-lookup"><span data-stu-id="a2366-149">Always block in your [ICorProfilerCallback::ThreadDestroyed](icorprofilercallback-threaddestroyed-method.md) callback until that thread's stack walk is complete.</span></span>  
  
- <span data-ttu-id="a2366-150">当探查器调入可触发垃圾回收的 CLR 函数时，不要持有锁。</span><span class="sxs-lookup"><span data-stu-id="a2366-150">Do not hold a lock while your profiler calls into a CLR function that can trigger a garbage collection.</span></span> <span data-ttu-id="a2366-151">也就是说，如果拥有的线程可能发出调用来触发垃圾回收，则不要持有锁。</span><span class="sxs-lookup"><span data-stu-id="a2366-151">That is, do not hold a lock if the owning thread might make a call that triggers a garbage collection.</span></span>  
  
 <span data-ttu-id="a2366-152">如果 `DoStackSnapshot` 从探查器已创建的线程中调用，以便可以遍历单独目标线程的堆栈，还会发生死锁的风险。</span><span class="sxs-lookup"><span data-stu-id="a2366-152">There is also a risk of deadlock if you call `DoStackSnapshot` from a thread that your profiler has created so that you can walk the stack of a separate target thread.</span></span> <span data-ttu-id="a2366-153">第一次创建的线程 `ICorProfilerInfo*` 将进入 (包括) 的某些方法 `DoStackSnapshot` ，clr 将在该线程上执行每个线程特定于 CLR 的初始化。</span><span class="sxs-lookup"><span data-stu-id="a2366-153">The first time the thread you created enters certain `ICorProfilerInfo*` methods (including `DoStackSnapshot`), the CLR will perform per-thread, CLR-specific initialization on that thread.</span></span> <span data-ttu-id="a2366-154">如果探查器已挂起要尝试遍历其堆栈的目标线程，并且如果该目标线程发生了对每个线程初始化执行所需的锁，则会发生死锁。</span><span class="sxs-lookup"><span data-stu-id="a2366-154">If your profiler has suspended the target thread whose stack you are trying to walk, and if that target thread happened to own a lock necessary for performing this per-thread initialization, a deadlock will occur.</span></span> <span data-ttu-id="a2366-155">若要避免这种死锁，请在 `DoStackSnapshot` 探查器创建的线程中执行初始调用以遍历单独的目标线程，但不要首先挂起目标线程。</span><span class="sxs-lookup"><span data-stu-id="a2366-155">To avoid this deadlock, make an initial call into `DoStackSnapshot` from your profiler-created thread to walk a separate target thread, but do not suspend the target thread first.</span></span> <span data-ttu-id="a2366-156">此初始调用可确保在发生死锁的情况下，每个线程的初始化都可以完成。</span><span class="sxs-lookup"><span data-stu-id="a2366-156">This initial call ensures that the per-thread initialization can complete without deadlock.</span></span> <span data-ttu-id="a2366-157">如果 `DoStackSnapshot` 成功并报告至少一个帧，则在该点之后，此探查器创建的线程将会挂起任何目标线程，并调用 `DoStackSnapshot` 来遍历该目标线程的堆栈。</span><span class="sxs-lookup"><span data-stu-id="a2366-157">If `DoStackSnapshot` succeeds and reports at least one frame, after that point, it will be safe for that profiler-created thread to suspend any target thread and call `DoStackSnapshot` to walk the stack of that target thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a2366-158">要求</span><span class="sxs-lookup"><span data-stu-id="a2366-158">Requirements</span></span>  

 <span data-ttu-id="a2366-159">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a2366-159">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a2366-160">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a2366-160">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a2366-161">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a2366-161">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a2366-162">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a2366-162">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2366-163">请参阅</span><span class="sxs-lookup"><span data-stu-id="a2366-163">See also</span></span>

- [<span data-ttu-id="a2366-164">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="a2366-164">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="a2366-165">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="a2366-165">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
