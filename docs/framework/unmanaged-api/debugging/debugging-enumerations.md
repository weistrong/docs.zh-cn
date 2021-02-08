---
description: 了解详细信息：调试枚举
title: 调试枚举
ms.date: 03/30/2017
helpviewer_keywords:
- debugging enumerations [.NET Framework]
- unmanaged enumerations [.NET Framework], debugging
- enumerations [.NET Framework debugging]
ms.assetid: 3af9f584-f1b4-4154-aeaa-8fce7c9f8b50
ms.openlocfilehash: 4a1d2fc9061fec7f5384418e4893c357f5d340ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801418"
---
# <a name="debugging-enumerations"></a><span data-ttu-id="4cf26-103">调试枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-103">Debugging Enumerations</span></span>

<span data-ttu-id="4cf26-104">本节介绍了调试 API 使用的非托管枚举。</span><span class="sxs-lookup"><span data-stu-id="4cf26-104">This section describes the unmanaged enumerations that the debugging API uses.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="4cf26-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="4cf26-105">In This Section</span></span>  

 [<span data-ttu-id="4cf26-106">CLR_DEBUGGING_PROCESS_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-106">CLR_DEBUGGING_PROCESS_FLAGS Enumeration</span></span>](clr-debugging-process-flags-enumeration.md)  
 <span data-ttu-id="4cf26-107">提供 [ICLRDebugging：： OpenVirtualProcess](iclrdebugging-openvirtualprocess-method.md) 方法使用的值。</span><span class="sxs-lookup"><span data-stu-id="4cf26-107">Provides values that are used by the [ICLRDebugging::OpenVirtualProcess](iclrdebugging-openvirtualprocess-method.md) method.</span></span>  
  
 [<span data-ttu-id="4cf26-108">CLRDataEnumMemoryFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-108">CLRDataEnumMemoryFlags Enumeration</span></span>](clrdataenummemoryflags-enumeration.md)  
 <span data-ttu-id="4cf26-109">指示对 [ICLRDataEnumMemoryRegions：： EnumMemoryRegions](iclrdataenummemoryregions-enummemoryregions-method.md) 方法的调用应包括哪些内存区域。</span><span class="sxs-lookup"><span data-stu-id="4cf26-109">Indicates which memory regions a call to the [ICLRDataEnumMemoryRegions::EnumMemoryRegions](iclrdataenummemoryregions-enummemoryregions-method.md) method should include.</span></span>  
  
 [<span data-ttu-id="4cf26-110">COR_PUB_ENUMPROCESS 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-110">COR_PUB_ENUMPROCESS Enumeration</span></span>](cor-pub-enumprocess-enumeration.md)  
 <span data-ttu-id="4cf26-111">标识要枚举的进程的类型。</span><span class="sxs-lookup"><span data-stu-id="4cf26-111">Identifies the type of process to be enumerated.</span></span>  
  
 [<span data-ttu-id="4cf26-112">CorDebugBlockingReason 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-112">CorDebugBlockingReason Enumeration</span></span>](cordebugblockingreason-enumeration.md)  
 <span data-ttu-id="4cf26-113">指定线程可能在给定对象上受到阻塞的原因。</span><span class="sxs-lookup"><span data-stu-id="4cf26-113">Specifies the reasons why a thread may become blocked on a given object.</span></span>  
  
 <span data-ttu-id="4cf26-114">CorDebugChainReason</span><span class="sxs-lookup"><span data-stu-id="4cf26-114">CorDebugChainReason</span></span>  
 <span data-ttu-id="4cf26-115">指示启动调用链的一个或多个原因。</span><span class="sxs-lookup"><span data-stu-id="4cf26-115">Indicates the reason or reasons for the initiation of a call chain.</span></span>  
  
 [<span data-ttu-id="4cf26-116">“Cor调试代码调用类型”枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-116">CorDebugCodeInvokeKind Enumeration</span></span>](cordebugcodeinvokekind-enumeration.md)  
 <span data-ttu-id="4cf26-117">描述导出函数如何调用托管代码。</span><span class="sxs-lookup"><span data-stu-id="4cf26-117">Describes how an exported function invokes managed code.</span></span>  
  
 [<span data-ttu-id="4cf26-118">“Cor调试代码调用目的”枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-118">CorDebugCodeInvokePurpose Enumeration</span></span>](cordebugcodeinvokepurpose-enumeration.md)  
 <span data-ttu-id="4cf26-119">描述为何导出的函数会调用托管代码。</span><span class="sxs-lookup"><span data-stu-id="4cf26-119">Describes why an exported function calls managed code.</span></span>  
  
 <span data-ttu-id="4cf26-120">CorDebugCreateProcessFlags</span><span class="sxs-lookup"><span data-stu-id="4cf26-120">CorDebugCreateProcessFlags</span></span>  
 <span data-ttu-id="4cf26-121">提供可在对 [ICorDebug：： CreateProcess](icordebug-createprocess-method.md) 方法的调用中使用的其他调试选项。</span><span class="sxs-lookup"><span data-stu-id="4cf26-121">Provides additional debugging options that can be used in a call to the [ICorDebug::CreateProcess](icordebug-createprocess-method.md) method.</span></span>  
  
 [<span data-ttu-id="4cf26-122">“Cor调试调试事件类型”枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-122">CorDebugDebugEventKind Enumeration</span></span>](cordebugdebugeventkind-enumeration.md)  
 <span data-ttu-id="4cf26-123">指示 [DecodeEvent](icordebugprocess6-decodeevent-method.md) 方法对其信息进行解码的事件类型。</span><span class="sxs-lookup"><span data-stu-id="4cf26-123">Indicates the type of event whose information is decoded by the [DecodeEvent](icordebugprocess6-decodeevent-method.md) method.</span></span>  
  
 [<span data-ttu-id="4cf26-124">“Cor调试解码事件标志窗口”枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-124">CorDebugDecodeEventFlagsWindows Enumeration</span></span>](cordebugdecodeeventflagswindows-enumeration.md)  
 <span data-ttu-id="4cf26-125">提供关于 Windows 平台上的调试事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="4cf26-125">Provides additional information about debug events on the Windows platform.</span></span>  
  
 <span data-ttu-id="4cf26-126">CorDebugExceptionCallbackType</span><span class="sxs-lookup"><span data-stu-id="4cf26-126">CorDebugExceptionCallbackType</span></span>  
 <span data-ttu-id="4cf26-127">指示从 [ICorDebugManagedCallback2：： Exception](icordebugmanagedcallback2-exception-method.md) 事件进行的回调类型。</span><span class="sxs-lookup"><span data-stu-id="4cf26-127">Indicates the type of callback that is made from an [ICorDebugManagedCallback2::Exception](icordebugmanagedcallback2-exception-method.md) event.</span></span>  
  
 [<span data-ttu-id="4cf26-128">CorDebugExceptionFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-128">CorDebugExceptionFlags Enumeration</span></span>](cordebugexceptionflags-enumeration.md)  
 <span data-ttu-id="4cf26-129">提供有关异常的附加信息。</span><span class="sxs-lookup"><span data-stu-id="4cf26-129">Provides additional information about an exception.</span></span>  
  
 <span data-ttu-id="4cf26-130">CorDebugExceptionUnwindCallbackType</span><span class="sxs-lookup"><span data-stu-id="4cf26-130">CorDebugExceptionUnwindCallbackType</span></span>  
 <span data-ttu-id="4cf26-131">指示在展开阶段正由回调发送信号的事件。</span><span class="sxs-lookup"><span data-stu-id="4cf26-131">Indicates the event that is being signaled by the callback during the unwind phase.</span></span>  
  
 [<span data-ttu-id="4cf26-132">CorDebugGCType 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-132">CorDebugGCType Enumeration</span></span>](cordebuggctype-enumeration.md)  
 <span data-ttu-id="4cf26-133">指示垃圾回收器是在工作站还是服务器上运行。</span><span class="sxs-lookup"><span data-stu-id="4cf26-133">Indicates whether the garbage collector is running on a workstation or a server.</span></span>  
  
 [<span data-ttu-id="4cf26-134">CorDebugGenerationTypes 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-134">CorDebugGenerationTypes Enumeration</span></span>](cordebuggenerationtypes-enumeration.md)  
 <span data-ttu-id="4cf26-135">指定托管堆上内存区域的生成。</span><span class="sxs-lookup"><span data-stu-id="4cf26-135">Specifies the generation of a region of memory on the managed heap.</span></span>  
  
 <span data-ttu-id="4cf26-136">CorDebugHandleType</span><span class="sxs-lookup"><span data-stu-id="4cf26-136">CorDebugHandleType</span></span>  
 <span data-ttu-id="4cf26-137">指示句柄类型。</span><span class="sxs-lookup"><span data-stu-id="4cf26-137">Indicates the handle type.</span></span>  
  
 [<span data-ttu-id="4cf26-138">CorDebugIlToNativeMappingTypes 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-138">CorDebugIlToNativeMappingTypes Enumeration</span></span>](cordebugiltonativemappingtypes-enumeration.md)  
 <span data-ttu-id="4cf26-139">指示本机指令的某一特定范围是否与特殊的代码区域相符。</span><span class="sxs-lookup"><span data-stu-id="4cf26-139">Indicates whether a particular range of native instructions corresponds to a special code region.</span></span>  
  
 <span data-ttu-id="4cf26-140">CorDebugIntercept</span><span class="sxs-lookup"><span data-stu-id="4cf26-140">CorDebugIntercept</span></span>  
 <span data-ttu-id="4cf26-141">指示可单步执行的代码的类型。</span><span class="sxs-lookup"><span data-stu-id="4cf26-141">Indicates the types of code that can be stepped into.</span></span>  
  
 [<span data-ttu-id="4cf26-142">CorDebugInterfaceVersion 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-142">CorDebugInterfaceVersion Enumeration</span></span>](cordebuginterfaceversion-enumeration.md)  
 <span data-ttu-id="4cf26-143">指定 .NET Framework 的版本，或在其中引入了接口的 .NET Framework 的版本。</span><span class="sxs-lookup"><span data-stu-id="4cf26-143">Specifies either a version of the .NET Framework, or the version of the .NET Framework in which an interface was introduced.</span></span>  
  
 <span data-ttu-id="4cf26-144">CorDebugInternalFrameType</span><span class="sxs-lookup"><span data-stu-id="4cf26-144">CorDebugInternalFrameType</span></span>  
 <span data-ttu-id="4cf26-145">标识堆栈帧的类型。</span><span class="sxs-lookup"><span data-stu-id="4cf26-145">Identifies the type of stack frame.</span></span>  
  
 [<span data-ttu-id="4cf26-146">CorDebugJITCompilerFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-146">CorDebugJITCompilerFlags Enumeration</span></span>](cordebugjitcompilerflags-enumeration.md)  
 <span data-ttu-id="4cf26-147">包含影响托管的实时 (JIT) 编译器的行为的值。</span><span class="sxs-lookup"><span data-stu-id="4cf26-147">Contains values that influence the behavior of the managed just-in-time (JIT) compiler.</span></span>  
  
 [<span data-ttu-id="4cf26-148">CorDebugJITCompilerFlagsDeprecated 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-148">CorDebugJITCompilerFlagsDeprecated Enumeration</span></span>](cordebugjitcompilerflagsdeprecated-enumeration.md)  
 <span data-ttu-id="4cf26-149">已过时。</span><span class="sxs-lookup"><span data-stu-id="4cf26-149">Obsolete.</span></span> <span data-ttu-id="4cf26-150">改为使用 `CORDEBUG_JIT_DEFAULT` [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) 枚举的成员。</span><span class="sxs-lookup"><span data-stu-id="4cf26-150">Use the `CORDEBUG_JIT_DEFAULT` member of the [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) enumeration instead.</span></span>  
  
 <span data-ttu-id="4cf26-151">CorDebugMappingResult</span><span class="sxs-lookup"><span data-stu-id="4cf26-151">CorDebugMappingResult</span></span>  
 <span data-ttu-id="4cf26-152">提供如何获取指令指针 (IP) 的值的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4cf26-152">Provides the details of how the value of the instruction pointer (IP) was obtained.</span></span>  
  
 [<span data-ttu-id="4cf26-153">CorDebugMDAFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-153">CorDebugMDAFlags Enumeration</span></span>](cordebugmdaflags-enumeration.md)  
 <span data-ttu-id="4cf26-154">指定在其上激发托管调试助手 (MDA) 的线程的状态。</span><span class="sxs-lookup"><span data-stu-id="4cf26-154">Specifies the status of the thread on which the managed debugging assistant (MDA) is fired.</span></span>  
  
 [<span data-ttu-id="4cf26-155">CorDebugNGenPolicy 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-155">CorDebugNGenPolicy Enumeration</span></span>](cordebugngenpolicy-enumeration.md)  
 <span data-ttu-id="4cf26-156">提供用于确定调试器是否从本机映像缓存中加载本机 (NGen) 映像的值。</span><span class="sxs-lookup"><span data-stu-id="4cf26-156">Provides a value that determines whether a debugger loads native (NGen) images from the native image cache.</span></span>  
  
 [<span data-ttu-id="4cf26-157">CorDebugPlatform 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-157">CorDebugPlatform Enumeration</span></span>](cordebugplatform-enumeration.md)  
 <span data-ttu-id="4cf26-158">提供 [ICorDebugDataTarget：： GetPlatform](icordebugdatatarget-getplatform-method.md) 方法使用的目标平台值。</span><span class="sxs-lookup"><span data-stu-id="4cf26-158">Provides target platform values that are used by the [ICorDebugDataTarget::GetPlatform](icordebugdatatarget-getplatform-method.md) method.</span></span>  
  
 [<span data-ttu-id="4cf26-159">“Cor调试记录格式”枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-159">CorDebugRecordFormat Enumeration</span></span>](cordebugrecordformat-enumeration.md)  
 <span data-ttu-id="4cf26-160">描述包含本机异常调试事件相关信息的字节数组的数据格式。</span><span class="sxs-lookup"><span data-stu-id="4cf26-160">Describes the format of the data in a byte array that contains information about a native exception debug event.</span></span>  
  
 <span data-ttu-id="4cf26-161">CorDebugRegister</span><span class="sxs-lookup"><span data-stu-id="4cf26-161">CorDebugRegister</span></span>  
 <span data-ttu-id="4cf26-162">指定与给定处理器体系结构关联的寄存器。</span><span class="sxs-lookup"><span data-stu-id="4cf26-162">Specifies the registers associated with a given processor architecture.</span></span>  
  
 [<span data-ttu-id="4cf26-163">CorDebugSetContextFlag 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-163">CorDebugSetContextFlag Enumeration</span></span>](cordebugsetcontextflag-enumeration.md)  
 <span data-ttu-id="4cf26-164">指示上下文是来自堆栈上的活动（或叶）帧，还是已通过从另一个帧展开来进行计算。</span><span class="sxs-lookup"><span data-stu-id="4cf26-164">Indicates whether the context is from the active (or leaf) frame on the stack or has been computed by unwinding from another frame.</span></span>  
  
 [<span data-ttu-id="4cf26-165">“Cor调试状态已更改”枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-165">CorDebugStateChange Enumeration</span></span>](cordebugstatechange-enumeration.md)  
 <span data-ttu-id="4cf26-166">描述基于进程变化必须删除的缓存数据数量。</span><span class="sxs-lookup"><span data-stu-id="4cf26-166">Describes the amount of cached data that must be discarded based on changes to the process.</span></span>  
  
 <span data-ttu-id="4cf26-167">CorDebugStepReason</span><span class="sxs-lookup"><span data-stu-id="4cf26-167">CorDebugStepReason</span></span>  
 <span data-ttu-id="4cf26-168">指示一个单步执行的结果。</span><span class="sxs-lookup"><span data-stu-id="4cf26-168">Indicates the outcome of an individual step.</span></span>  
  
 <span data-ttu-id="4cf26-169">CorDebugThreadState</span><span class="sxs-lookup"><span data-stu-id="4cf26-169">CorDebugThreadState</span></span>  
 <span data-ttu-id="4cf26-170">指定用于调试的线程的状态。</span><span class="sxs-lookup"><span data-stu-id="4cf26-170">Specifies the state of a thread for debugging.</span></span>  
  
 <span data-ttu-id="4cf26-171">\>CorDebugUnmappedStop</span><span class="sxs-lookup"><span data-stu-id="4cf26-171">\>CorDebugUnmappedStop</span></span>  
 <span data-ttu-id="4cf26-172">指定未映射代码的类型，这些代码可以中断分档器代码执行。</span><span class="sxs-lookup"><span data-stu-id="4cf26-172">Specifies the type of unmapped code that can trigger a halt in code execution by the stepper.</span></span>  
  
 <span data-ttu-id="4cf26-173">CorDebugUserState</span><span class="sxs-lookup"><span data-stu-id="4cf26-173">CorDebugUserState</span></span>  
 <span data-ttu-id="4cf26-174">指示线程的用户状态。</span><span class="sxs-lookup"><span data-stu-id="4cf26-174">Indicates the user state of a thread.</span></span>  
  
 [<span data-ttu-id="4cf26-175">CorGCReferenceType 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-175">CorGCReferenceType Enumeration</span></span>](corgcreferencetype-enumeration.md)  
 <span data-ttu-id="4cf26-176">标识要进行垃圾回收的对象的源。</span><span class="sxs-lookup"><span data-stu-id="4cf26-176">Identifies the source of an object to be garbage-collected.</span></span>  
  
 [<span data-ttu-id="4cf26-177">ILCodeKind 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-177">ILCodeKind Enumeration</span></span>](ilcodekind-enumeration.md)  
 <span data-ttu-id="4cf26-178">提供用于指定调试器是否能够访问在探查器 ReJIT 检测中添加的局部变量或代码的值。</span><span class="sxs-lookup"><span data-stu-id="4cf26-178">Provides values that specify whether the debugger is able to access local variables or code added in profiler ReJIT instrumentation.</span></span>  
  
 [<span data-ttu-id="4cf26-179">LoggingLevelEnum 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-179">LoggingLevelEnum Enumeration</span></span>](logginglevelenum-enumeration.md)  
 <span data-ttu-id="4cf26-180">指示在托管线程记录事件时写入事件日志的描述性消息的严重级别。</span><span class="sxs-lookup"><span data-stu-id="4cf26-180">Indicates the severity level of a descriptive message that is written to the event log when a managed thread logs an event.</span></span>  
  
 [<span data-ttu-id="4cf26-181">LogSwitchCallReason 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-181">LogSwitchCallReason Enumeration</span></span>](logswitchcallreason-enumeration.md)  
 <span data-ttu-id="4cf26-182">指示已对调试/跟踪开关执行的操作。</span><span class="sxs-lookup"><span data-stu-id="4cf26-182">Indicates the operation that was performed on a debugging/tracing switch.</span></span>  
  
 [<span data-ttu-id="4cf26-183">VariableLocationType 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-183">VariableLocationType Enumeration</span></span>](variablelocationtype-enumeration.md)  
 <span data-ttu-id="4cf26-184">指示变量的本机位置类型。</span><span class="sxs-lookup"><span data-stu-id="4cf26-184">Indicates the native location type of a variable.</span></span>  
  
 [<span data-ttu-id="4cf26-185">WriteableMetadataUpdateMode 枚举</span><span class="sxs-lookup"><span data-stu-id="4cf26-185">WriteableMetadataUpdateMode Enumeration</span></span>](writeablemetadataupdatemode-enumeration.md)  
 <span data-ttu-id="4cf26-186">提供用于指定元数据的内存中更新对调试器是否可见的值。</span><span class="sxs-lookup"><span data-stu-id="4cf26-186">Provides values that specify whether in-memory updates to metadata are visible to a debugger.</span></span>

 <span data-ttu-id="4cf26-187">[ClrDataSourceType 枚举](clrdatasourcetype-enumeration.md) 提供 CLRDATA_IL_ADDRESS_MAP 结构使用的值。</span><span class="sxs-lookup"><span data-stu-id="4cf26-187">[ClrDataSourceType Enumeration](clrdatasourcetype-enumeration.md) Provides values that are used by the CLRDATA_IL_ADDRESS_MAP structure.</span></span>

## <a name="related-sections"></a><span data-ttu-id="4cf26-188">相关章节</span><span class="sxs-lookup"><span data-stu-id="4cf26-188">Related Sections</span></span>  

 [<span data-ttu-id="4cf26-189">调试 Coclass</span><span class="sxs-lookup"><span data-stu-id="4cf26-189">Debugging Coclasses</span></span>](debugging-coclasses.md)  
  
 [<span data-ttu-id="4cf26-190">调试接口</span><span class="sxs-lookup"><span data-stu-id="4cf26-190">Debugging Interfaces</span></span>](debugging-interfaces.md)  
  
 [<span data-ttu-id="4cf26-191">调试全局静态函数</span><span class="sxs-lookup"><span data-stu-id="4cf26-191">Debugging Global Static Functions</span></span>](debugging-global-static-functions.md)  
  
 [<span data-ttu-id="4cf26-192">调试结构</span><span class="sxs-lookup"><span data-stu-id="4cf26-192">Debugging Structures</span></span>](debugging-structures.md)
