---
description: 了解详细信息： ICorDebugManagedCallback 接口
title: ICorDebugManagedCallback 接口
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback
helpviewer_keywords:
- ICorDebugManagedCallback interface [.NET Framework debugging]
ms.assetid: b47f1d61-c7dc-4196-b926-0b08c94f7041
topic_type:
- apiref
ms.openlocfilehash: 0dd33e4295caa8f5ae41c65d9bd10152737156ca
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722810"
---
# <a name="icordebugmanagedcallback-interface"></a><span data-ttu-id="0197a-103">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="0197a-103">ICorDebugManagedCallback Interface</span></span>

<span data-ttu-id="0197a-104">提供用于处理调试器回调的方法。</span><span class="sxs-lookup"><span data-stu-id="0197a-104">Provides methods to process debugger callbacks.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0197a-105">方法</span><span class="sxs-lookup"><span data-stu-id="0197a-105">Methods</span></span>  
  
|<span data-ttu-id="0197a-106">方法</span><span class="sxs-lookup"><span data-stu-id="0197a-106">Method</span></span>|<span data-ttu-id="0197a-107">说明</span><span class="sxs-lookup"><span data-stu-id="0197a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0197a-108">Break 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-108">Break Method</span></span>](icordebugmanagedcallback-break-method.md)|<span data-ttu-id="0197a-109">当 <xref:System.Reflection.Emit.OpCodes.Break> 执行代码流中的指令时，通知调试器。</span><span class="sxs-lookup"><span data-stu-id="0197a-109">Notifies the debugger when a <xref:System.Reflection.Emit.OpCodes.Break> instruction in the code stream is executed.</span></span>|  
|[<span data-ttu-id="0197a-110">Breakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-110">Breakpoint Method</span></span>](icordebugmanagedcallback-breakpoint-method.md)|<span data-ttu-id="0197a-111">遇到断点时，通知调试器。</span><span class="sxs-lookup"><span data-stu-id="0197a-111">Notifies the debugger when a breakpoint is encountered.</span></span>|  
|[<span data-ttu-id="0197a-112">BreakpointSetError 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-112">BreakpointSetError Method</span></span>](icordebugmanagedcallback-breakpointseterror-method.md)|<span data-ttu-id="0197a-113">通知调试器，公共语言运行时 (CLR) 无法准确绑定在编译函数之前已设置的断点 (JIT) 。</span><span class="sxs-lookup"><span data-stu-id="0197a-113">Notifies the debugger that the common language runtime (CLR) was unable to accurately bind a breakpoint that was set before a function was just-in-time (JIT) compiled.</span></span>|  
|[<span data-ttu-id="0197a-114">ControlCTrap 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-114">ControlCTrap Method</span></span>](icordebugmanagedcallback-controlctrap-method.md)|<span data-ttu-id="0197a-115">通知调试器在被调试的进程中捕获了 CTRL + C。</span><span class="sxs-lookup"><span data-stu-id="0197a-115">Notifies the debugger that a CTRL+C is trapped in the process being debugged.</span></span>|  
|[<span data-ttu-id="0197a-116">CreateAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-116">CreateAppDomain Method</span></span>](icordebugmanagedcallback-createappdomain-method.md)|<span data-ttu-id="0197a-117">通知调试器已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="0197a-117">Notifies the debugger that an application domain has been created.</span></span>|  
|[<span data-ttu-id="0197a-118">CreateProcess 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-118">CreateProcess Method</span></span>](icordebugmanagedcallback-createprocess-method.md)|<span data-ttu-id="0197a-119">第一次附加或启动进程时，通知调试器。</span><span class="sxs-lookup"><span data-stu-id="0197a-119">Notifies the debugger when a process has been attached or started for the first time.</span></span>|  
|[<span data-ttu-id="0197a-120">CreateThread 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-120">CreateThread Method</span></span>](icordebugmanagedcallback-createthread-method.md)|<span data-ttu-id="0197a-121">通知调试器线程已开始执行托管代码。</span><span class="sxs-lookup"><span data-stu-id="0197a-121">Notifies the debugger that a thread has started executing managed code.</span></span>|  
|[<span data-ttu-id="0197a-122">DebuggerError 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-122">DebuggerError Method</span></span>](icordebugmanagedcallback-debuggererror-method.md)|<span data-ttu-id="0197a-123">通知调试器在尝试处理来自 CLR 的事件时出错。</span><span class="sxs-lookup"><span data-stu-id="0197a-123">Notifies the debugger that an error has occurred while attempting to handle an event from the CLR.</span></span>|  
|[<span data-ttu-id="0197a-124">EditAndContinueRemap 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-124">EditAndContinueRemap Method</span></span>](icordebugmanagedcallback-editandcontinueremap-method.md)|<span data-ttu-id="0197a-125">已弃用。</span><span class="sxs-lookup"><span data-stu-id="0197a-125">Deprecated.</span></span> <span data-ttu-id="0197a-126">通知调试器已将重新映射事件发送到 IDE。</span><span class="sxs-lookup"><span data-stu-id="0197a-126">Notifies the debugger that a remap event has been sent to the IDE.</span></span>|  
|[<span data-ttu-id="0197a-127">EvalComplete 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-127">EvalComplete Method</span></span>](icordebugmanagedcallback-evalcomplete-method.md)|<span data-ttu-id="0197a-128">通知调试器已完成计算。</span><span class="sxs-lookup"><span data-stu-id="0197a-128">Notifies the debugger that an evaluation has been completed.</span></span>|  
|[<span data-ttu-id="0197a-129">EvalException 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-129">EvalException Method</span></span>](icordebugmanagedcallback-evalexception-method.md)|<span data-ttu-id="0197a-130">通知调试器由于未处理的异常而终止了计算。</span><span class="sxs-lookup"><span data-stu-id="0197a-130">Notifies the debugger that an evaluation has been terminated with an unhandled exception.</span></span>|  
|[<span data-ttu-id="0197a-131">Exception 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-131">Exception Method</span></span>](icordebugmanagedcallback-exception-method.md)|<span data-ttu-id="0197a-132">通知调试器已从托管代码引发了异常。</span><span class="sxs-lookup"><span data-stu-id="0197a-132">Notifies the debugger that an exception has been thrown from managed code.</span></span>|  
|[<span data-ttu-id="0197a-133">ExitAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-133">ExitAppDomain Method</span></span>](icordebugmanagedcallback-exitappdomain-method.md)|<span data-ttu-id="0197a-134">通知调试器应用程序域已退出。</span><span class="sxs-lookup"><span data-stu-id="0197a-134">Notifies the debugger that an application domain has exited.</span></span>|  
|[<span data-ttu-id="0197a-135">ExitProcess 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-135">ExitProcess Method</span></span>](icordebugmanagedcallback-exitprocess-method.md)|<span data-ttu-id="0197a-136">通知调试器进程已退出。</span><span class="sxs-lookup"><span data-stu-id="0197a-136">Notifies the debugger that a process has exited.</span></span>|  
|[<span data-ttu-id="0197a-137">ExitThread 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-137">ExitThread Method</span></span>](icordebugmanagedcallback-exitthread-method.md)|<span data-ttu-id="0197a-138">通知调试器已退出正在执行的托管代码的线程。</span><span class="sxs-lookup"><span data-stu-id="0197a-138">Notifies the debugger that a thread that was executing managed code has exited.</span></span>|  
|[<span data-ttu-id="0197a-139">LoadAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-139">LoadAssembly Method</span></span>](icordebugmanagedcallback-loadassembly-method.md)|<span data-ttu-id="0197a-140">通知调试器已成功加载 CLR 程序集。</span><span class="sxs-lookup"><span data-stu-id="0197a-140">Notifies the debugger that a CLR assembly has been successfully loaded.</span></span>|  
|[<span data-ttu-id="0197a-141">LoadClass 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-141">LoadClass Method</span></span>](icordebugmanagedcallback-loadclass-method.md)|<span data-ttu-id="0197a-142">通知调试器已加载某个类。</span><span class="sxs-lookup"><span data-stu-id="0197a-142">Notifies the debugger that a class has been loaded.</span></span>|  
|[<span data-ttu-id="0197a-143">LoadModule 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-143">LoadModule Method</span></span>](icordebugmanagedcallback-loadmodule-method.md)|<span data-ttu-id="0197a-144">通知调试器已成功加载 CLR 模块。</span><span class="sxs-lookup"><span data-stu-id="0197a-144">Notifies the debugger that a CLR module has been successfully loaded.</span></span>|  
|[<span data-ttu-id="0197a-145">LogMessage 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-145">LogMessage Method</span></span>](icordebugmanagedcallback-logmessage-method.md)|<span data-ttu-id="0197a-146">通知调试器，CLR 托管线程在类中调用了方法 <xref:System.Diagnostics.EventLog> 来记录事件。</span><span class="sxs-lookup"><span data-stu-id="0197a-146">Notifies the debugger that a CLR managed thread has called a method in the <xref:System.Diagnostics.EventLog> class to log an event.</span></span>|  
|[<span data-ttu-id="0197a-147">LogSwitch 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-147">LogSwitch Method</span></span>](icordebugmanagedcallback-logswitch-method.md)|<span data-ttu-id="0197a-148">通知调试器，CLR 托管线程在类中调用了方法 <xref:System.Diagnostics.Switch> 来创建、修改或删除调试/跟踪开关。</span><span class="sxs-lookup"><span data-stu-id="0197a-148">Notifies the debugger that a CLR managed thread has called a method in the <xref:System.Diagnostics.Switch> class to create, modify, or delete a debugging/tracing switch.</span></span>|  
|[<span data-ttu-id="0197a-149">NameChange 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-149">NameChange Method</span></span>](icordebugmanagedcallback-namechange-method.md)|<span data-ttu-id="0197a-150">通知调试器应用程序域或线程的名称已更改。</span><span class="sxs-lookup"><span data-stu-id="0197a-150">Notifies the debugger that the name of either an application domain or thread has changed.</span></span>|  
|[<span data-ttu-id="0197a-151">StepComplete 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-151">StepComplete Method</span></span>](icordebugmanagedcallback-stepcomplete-method.md)|<span data-ttu-id="0197a-152">通知调试器某个步骤已完成。</span><span class="sxs-lookup"><span data-stu-id="0197a-152">Notifies the debugger that a step has completed.</span></span>|  
|[<span data-ttu-id="0197a-153">UnloadAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-153">UnloadAssembly Method</span></span>](icordebugmanagedcallback-unloadassembly-method.md)|<span data-ttu-id="0197a-154">通知调试器已卸载 CLR 程序集。</span><span class="sxs-lookup"><span data-stu-id="0197a-154">Notifies the debugger that a CLR assembly has been unloaded.</span></span>|  
|[<span data-ttu-id="0197a-155">UnloadClass 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-155">UnloadClass Method</span></span>](icordebugmanagedcallback-unloadclass-method.md)|<span data-ttu-id="0197a-156">通知调试器正在卸载某个类。</span><span class="sxs-lookup"><span data-stu-id="0197a-156">Notifies the debugger that a class is being unloaded.</span></span>|  
|[<span data-ttu-id="0197a-157">UnloadModule 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-157">UnloadModule Method</span></span>](icordebugmanagedcallback-unloadmodule-method.md)|<span data-ttu-id="0197a-158">通知调试器已卸载 CLR 模块 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="0197a-158">Notifies the debugger that a CLR module (DLL) has been unloaded.</span></span>|  
|[<span data-ttu-id="0197a-159">UpdateModuleSymbols 方法</span><span class="sxs-lookup"><span data-stu-id="0197a-159">UpdateModuleSymbols Method</span></span>](icordebugmanagedcallback-updatemodulesymbols-method.md)|<span data-ttu-id="0197a-160">通知调试器 CLR 模块的符号已更改。</span><span class="sxs-lookup"><span data-stu-id="0197a-160">Notifies the debugger that the symbols for a CLR module have changed.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0197a-161">备注</span><span class="sxs-lookup"><span data-stu-id="0197a-161">Remarks</span></span>  

 <span data-ttu-id="0197a-162">所有回调都是序列化的，在同一线程中调用，并在进程处于已同步状态的情况下调用。</span><span class="sxs-lookup"><span data-stu-id="0197a-162">All callbacks are serialized, called in the same thread, and called with the process in the synchronized state.</span></span>  
  
 <span data-ttu-id="0197a-163">每个回调实现都必须调用 [ICorDebugController：： Continue](icordebugcontroller-continue-method.md) 以继续执行。</span><span class="sxs-lookup"><span data-stu-id="0197a-163">Each callback implementation must call [ICorDebugController::Continue](icordebugcontroller-continue-method.md) to resume execution.</span></span> <span data-ttu-id="0197a-164">如果在 `ICorDebugController::Continue` 回调返回之前未调用，则该进程将保持停止状态，并且在调用之前不会进行更多的事件回调 `ICorDebugController::Continue` 。</span><span class="sxs-lookup"><span data-stu-id="0197a-164">If `ICorDebugController::Continue` is not called before the callback returns, the process will remain stopped and no more event callbacks will occur until `ICorDebugController::Continue` is called.</span></span>  
  
 <span data-ttu-id="0197a-165">如果调试程序正在 .NET Framework 版本2.0 应用程序进行调试，则必须实现 [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="0197a-165">A debugger must implement [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) if it is debugging .NET Framework version 2.0 applications.</span></span> <span data-ttu-id="0197a-166">或的实例 `ICorDebugManagedCallback` `ICorDebugManagedCallback2` 作为回调对象传递给 [ICorDebug：： SetManagedHandler](icordebug-setmanagedhandler-method.md)。</span><span class="sxs-lookup"><span data-stu-id="0197a-166">An instance of `ICorDebugManagedCallback` or `ICorDebugManagedCallback2` is passed as the callback object to [ICorDebug::SetManagedHandler](icordebug-setmanagedhandler-method.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0197a-167">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="0197a-167">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0197a-168">要求</span><span class="sxs-lookup"><span data-stu-id="0197a-168">Requirements</span></span>  

 <span data-ttu-id="0197a-169">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0197a-169">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0197a-170">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0197a-170">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0197a-171">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0197a-171">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0197a-172">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0197a-172">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0197a-173">请参阅</span><span class="sxs-lookup"><span data-stu-id="0197a-173">See also</span></span>

- [<span data-ttu-id="0197a-174">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="0197a-174">ICorDebug Interface</span></span>](icordebug-interface.md)
- [<span data-ttu-id="0197a-175">ICorDebugManagedCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="0197a-175">ICorDebugManagedCallback2 Interface</span></span>](icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="0197a-176">调试接口</span><span class="sxs-lookup"><span data-stu-id="0197a-176">Debugging Interfaces</span></span>](debugging-interfaces.md)
