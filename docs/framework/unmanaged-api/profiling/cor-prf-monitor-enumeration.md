---
description: 了解详细信息： COR_PRF_MONITOR 枚举
title: COR_PRF_MONITOR 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_MONITOR
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_MONITOR
helpviewer_keywords:
- COR_PRF_MONITOR enumeration [.NET Framework profiling]
ms.assetid: 9294d702-b4e5-441c-a930-e63d27b86bfd
topic_type:
- apiref
ms.openlocfilehash: 5b0bd17713e47e40982e88f33721bf7d6d27fd00
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657783"
---
# <a name="cor_prf_monitor-enumeration"></a><span data-ttu-id="7cdda-103">COR_PRF_MONITOR 枚举</span><span class="sxs-lookup"><span data-stu-id="7cdda-103">COR_PRF_MONITOR Enumeration</span></span>

<span data-ttu-id="7cdda-104">包含用于指定探查器希望订阅的行为、功能或事件的值。</span><span class="sxs-lookup"><span data-stu-id="7cdda-104">Contains values that are used to specify behavior, capabilities, or events to which the profiler wishes to subscribe.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7cdda-105">语法</span><span class="sxs-lookup"><span data-stu-id="7cdda-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_MONITOR_NONE                = 0x00000000,  
    COR_PRF_MONITOR_FUNCTION_UNLOADS    = 0x00000001,  
    COR_PRF_MONITOR_CLASS_LOADS         = 0x00000002,  
    COR_PRF_MONITOR_MODULE_LOADS        = 0x00000004,  
    COR_PRF_MONITOR_ASSEMBLY_LOADS      = 0x00000008,  
    COR_PRF_MONITOR_APPDOMAIN_LOADS     = 0x00000010,  
    COR_PRF_MONITOR_JIT_COMPILATION     = 0x00000020,  
    COR_PRF_MONITOR_EXCEPTIONS          = 0x00000040,  
    COR_PRF_MONITOR_GC                  = 0x00000080,  
    COR_PRF_MONITOR_OBJECT_ALLOCATED    = 0x00000100,  
    COR_PRF_MONITOR_THREADS             = 0x00000200,  
    COR_PRF_MONITOR_REMOTING            = 0x00000400,  
    COR_PRF_MONITOR_CODE_TRANSITIONS    = 0x00000800,  
    COR_PRF_MONITOR_ENTERLEAVE          = 0x00001000,  
    COR_PRF_MONITOR_CCW                 = 0x00002000,  
    COR_PRF_MONITOR_REMOTING_COOKIE     = 0x00004000 |
                                          COR_PRF_MONITOR_REMOTING,  
    COR_PRF_MONITOR_REMOTING_ASYNC      = 0x00008000 |
                                          COR_PRF_MONITOR_REMOTING,  
    COR_PRF_MONITOR_SUSPENDS            = 0x00010000,  
    COR_PRF_MONITOR_CACHE_SEARCHES      = 0x00020000,  
    COR_PRF_ENABLE_REJIT                = 0x00040000,  
    COR_PRF_ENABLE_INPROC_DEBUGGING     = 0x00080000,  
    COR_PRF_ENABLE_JIT_MAPS             = 0x00100000,  
    COR_PRF_DISABLE_INLINING            = 0x00200000,  
    COR_PRF_DISABLE_OPTIMIZATIONS       = 0x00400000,  
    COR_PRF_ENABLE_OBJECT_ALLOCATED     = 0x00800000,  
    COR_PRF_MONITOR_CLR_EXCEPTIONS      = 0x01000000,  
    COR_PRF_MONITOR_ALL                 = 0x0107FFFF,  
    COR_PRF_ENABLE_FUNCTION_ARGS        = 0X02000000,  
    COR_PRF_ENABLE_FUNCTION_RETVAL      = 0X04000000,  
    COR_PRF_ENABLE_FRAME_INFO           = 0X08000000,  
    COR_PRF_ENABLE_STACK_SNAPSHOT       = 0X10000000,  
    COR_PRF_USE_PROFILE_IMAGES          = 0x20000000,  
    COR_PRF_DISABLE_TRANSPARENCY_CHECKS_UNDER_FULL_TRUST  
                                        = 0x40000000,  
    COR_PRF_DISABLE_ALL_NGEN_IMAGES     = 0x80000000,  
    COR_PRF_ALL                         = 0x8FFFFFFF,  
    COR_PRF_REQUIRE_PROFILE_IMAGE       = COR_PRF_USE_PROFILE_IMAGES |
                                          COR_PRF_MONITOR_CODE_TRANSITIONS |
                                          COR_PRF_MONITOR_ENTERLEAVE,  
    COR_PRF_ALLOWABLE_AFTER_ATTACH      = COR_PRF_MONITOR_THREADS |  
                                          COR_PRF_MONITOR_MODULE_LOADS |  
                                          COR_PRF_MONITOR_ASSEMBLY_LOADS |  
                                          COR_PRF_MONITOR_APPDOMAIN_LOADS |  
                                          COR_PRF_ENABLE_STACK_SNAPSHOT |  
                                          COR_PRF_MONITOR_GC |  
                                          COR_PRF_MONITOR_SUSPENDS |  
                                          COR_PRF_MONITOR_CLASS_LOADS |  
                                          COR_PRF_MONITOR_JIT_COMPILATION,  
    COR_PRF_MONITOR_IMMUTABLE           = COR_PRF_MONITOR_CODE_TRANSITIONS |  
                                          COR_PRF_MONITOR_REMOTING |  
                                          COR_PRF_MONITOR_REMOTING_COOKIE |  
                                          COR_PRF_MONITOR_REMOTING_ASYNC |  
                                          COR_PRF_ENABLE_REJIT |  
                                          COR_PRF_ENABLE_INPROC_DEBUGGING |  
                                          COR_PRF_ENABLE_JIT_MAPS |  
                                          COR_PRF_DISABLE_OPTIMIZATIONS |  
                                          COR_PRF_DISABLE_INLINING |  
                                          COR_PRF_ENABLE_OBJECT_ALLOCATED |  
                                          COR_PRF_ENABLE_FUNCTION_ARGS |  
                                          COR_PRF_ENABLE_FUNCTION_RETVAL |  
                                          COR_PRF_ENABLE_FRAME_INFO |  
                                          COR_PRF_USE_PROFILE_IMAGES |  
                     COR_PRF_DISABLE_TRANSPARENCY_CHECKS_UNDER_FULL_TRUST |  
                                          COR_PRF_DISABLE_ALL_NGEN_IMAGES  
} COR_PRF_MONITOR;  
```  
  
## <a name="members"></a><span data-ttu-id="7cdda-106">成员</span><span class="sxs-lookup"><span data-stu-id="7cdda-106">Members</span></span>  

 <span data-ttu-id="7cdda-107">以下各节 `COR_PRF_MONITOR` 按类别列出枚举成员。</span><span class="sxs-lookup"><span data-stu-id="7cdda-107">The following sections list `COR_PRF_MONITOR` enumeration members by category.</span></span> <span data-ttu-id="7cdda-108">类别为：</span><span class="sxs-lookup"><span data-stu-id="7cdda-108">The categories are:</span></span>  
  
- [<span data-ttu-id="7cdda-109">未设置标志</span><span class="sxs-lookup"><span data-stu-id="7cdda-109">No flags set</span></span>](#None)  
  
- [<span data-ttu-id="7cdda-110">回调标志</span><span class="sxs-lookup"><span data-stu-id="7cdda-110">Callback flags</span></span>](#Callback)  
  
- [<span data-ttu-id="7cdda-111">功能启用标志</span><span class="sxs-lookup"><span data-stu-id="7cdda-111">Feature-enabling flags</span></span>](#Feature)  
  
- [<span data-ttu-id="7cdda-112">配置标志</span><span class="sxs-lookup"><span data-stu-id="7cdda-112">Configuration flags</span></span>](#Config)  
  
- [<span data-ttu-id="7cdda-113">复合标志</span><span class="sxs-lookup"><span data-stu-id="7cdda-113">Composite flags</span></span>](#Composite)  
  
<a name="None"></a>

### <a name="no-flags-set"></a><span data-ttu-id="7cdda-114">未设置标志</span><span class="sxs-lookup"><span data-stu-id="7cdda-114">No flags set</span></span>  
  
|<span data-ttu-id="7cdda-115">成员</span><span class="sxs-lookup"><span data-stu-id="7cdda-115">Member</span></span>|<span data-ttu-id="7cdda-116">说明</span><span class="sxs-lookup"><span data-stu-id="7cdda-116">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_MONITOR_NONE`|<span data-ttu-id="7cdda-117">不设置任何标志。</span><span class="sxs-lookup"><span data-stu-id="7cdda-117">No flags are set.</span></span>|  
  
<a name="Callback"></a>

### <a name="callback-flags"></a><span data-ttu-id="7cdda-118">回调标志</span><span class="sxs-lookup"><span data-stu-id="7cdda-118">Callback flags</span></span>  
  
|<span data-ttu-id="7cdda-119">成员</span><span class="sxs-lookup"><span data-stu-id="7cdda-119">Member</span></span>|<span data-ttu-id="7cdda-120">说明</span><span class="sxs-lookup"><span data-stu-id="7cdda-120">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_MONITOR_ALL`|<span data-ttu-id="7cdda-121">启用所有回调事件。</span><span class="sxs-lookup"><span data-stu-id="7cdda-121">Enables all callback events.</span></span>|  
|`COR_PRF_MONITOR_APPDOMAIN_LOADS`|<span data-ttu-id="7cdda-122">控制 `AppDomainCreation*` `AppDomainShutdown*` [ICorProfilerCallback](icorprofilercallback-interface.md) 接口中的和回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-122">Controls the `AppDomainCreation*` and `AppDomainShutdown*` callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_ASSEMBLY_LOADS`|<span data-ttu-id="7cdda-123">控制 `AssemblyLoad*` `AssemblyUnload*` [ICorProfilerCallback](icorprofilercallback-interface.md) 接口中的和回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-123">Controls the `AssemblyLoad*` and `AssemblyUnload*` callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_CACHE_SEARCHES`|<span data-ttu-id="7cdda-124">控制 `JITCachedFunctionSearch*` [ICorProfilerCallback](icorprofilercallback-interface.md) 接口中的回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-124">Controls the `JITCachedFunctionSearch*` callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span><br /><br /> <span data-ttu-id="7cdda-125">此标志的行为在 .NET Framework 版本 2.0 中发生了变化。</span><span class="sxs-lookup"><span data-stu-id="7cdda-125">The behavior of this flag is changed in the .NET Framework version 2.0.</span></span>|  
|`COR_PRF_MONITOR_CCW`|<span data-ttu-id="7cdda-126">控制 `COMClassicVTable*` [ICorProfilerCallback](icorprofilercallback-interface.md) 接口中的回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-126">Controls the `COMClassicVTable*` callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_CLASS_LOADS`|<span data-ttu-id="7cdda-127">控制 `ClassLoad*` `ClassUnload*` [ICorProfilerCallback](icorprofilercallback-interface.md) 接口中的和回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-127">Controls the `ClassLoad*` and `ClassUnload*` callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_CLR_EXCEPTIONS`|<span data-ttu-id="7cdda-128">控制 `ExceptionCLRCatcher*` [ICorProfilerCallback](icorprofilercallback-interface.md) 接口中的回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-128">Controls the `ExceptionCLRCatcher*` callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_CODE_TRANSITIONS`|<span data-ttu-id="7cdda-129">控制[ICorProfilerCallback](icorprofilercallback-interface.md)接口中的[UnmanagedToManagedTransition](icorprofilercallback-unmanagedtomanagedtransition-method.md)和[ManagedToUnmanagedTransition](icorprofilercallback-managedtounmanagedtransition-method.md)回调</span><span class="sxs-lookup"><span data-stu-id="7cdda-129">Controls the [UnmanagedToManagedTransition](icorprofilercallback-unmanagedtomanagedtransition-method.md) and [ManagedToUnmanagedTransition](icorprofilercallback-managedtounmanagedtransition-method.md) callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface</span></span>|  
|`COR_PRF_MONITOR_ENTERLEAVE`|<span data-ttu-id="7cdda-130">控制 `FunctionEnter*` 、 `FunctionLeave*` 和 `FunctionTailCall*` [分析全局静态函数](profiling-global-static-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="7cdda-130">Controls the `FunctionEnter*`,  `FunctionLeave*`, and `FunctionTailCall*`[profiling global static functions](profiling-global-static-functions.md).</span></span>|  
|`COR_PRF_MONITOR_EXCEPTIONS`|<span data-ttu-id="7cdda-131">控制 [ExceptionThrown](icorprofilercallback-exceptionthrown-method.md) 回调，并控制 `ExceptionSearch*` `ExceptionOSHandler*` `ExceptionUnwind*` `ExceptionCatcher*` [ICorProfilerCallback](icorprofilercallback-interface.md) 接口中的、、和回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-131">Controls the [ExceptionThrown](icorprofilercallback-exceptionthrown-method.md) callback and the `ExceptionSearch*`, `ExceptionOSHandler*`, `ExceptionUnwind*`, and `ExceptionCatcher*` callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_FUNCTION_UNLOADS`|<span data-ttu-id="7cdda-132">控制[ICorProfilerCallback](icorprofilercallback-interface.md)接口中的[FunctionUnloadStarted](icorprofilercallback-functionunloadstarted-method.md)回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-132">Controls the [FunctionUnloadStarted](icorprofilercallback-functionunloadstarted-method.md) callback in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_GC`|<span data-ttu-id="7cdda-133">控制接口中的[GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md)、 [GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md)、 [MovedReferences](icorprofilercallback-movedreferences-method.md)、 [MovedReferences2](icorprofilercallback4-movedreferences2-method.md)、 [SurvivingReferences](icorprofilercallback2-survivingreferences-method.md)、 [SurvivingReferences2](icorprofilercallback4-survivingreferences2-method.md)、ObjectReferences、 [ObjectsAllocatedByClass](icorprofilercallback-objectsallocatedbyclass-method.md)、 [RootReferences](icorprofilercallback-rootreferences-method.md)、 [](icorprofilercallback2-handlecreated-method.md) [RootReferences2](icorprofilercallback2-rootreferences2-method.md) [、HandleCreated、](icorprofilercallback-objectreferences-method.md) [HandleDestroyed 和](icorprofilercallback2-handledestroyed-method.md) [FinalizeableObjectQueued](icorprofilercallback2-finalizeableobjectqueued-method.md)回调 `ICorProfilerCallback*` 。</span><span class="sxs-lookup"><span data-stu-id="7cdda-133">Controls the [GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md),   [GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md),  [MovedReferences](icorprofilercallback-movedreferences-method.md), [MovedReferences2](icorprofilercallback4-movedreferences2-method.md),    [SurvivingReferences](icorprofilercallback2-survivingreferences-method.md),  [SurvivingReferences2](icorprofilercallback4-survivingreferences2-method.md), [ObjectReferences](icorprofilercallback-objectreferences-method.md),   [ObjectsAllocatedByClass](icorprofilercallback-objectsallocatedbyclass-method.md),  [RootReferences](icorprofilercallback-rootreferences-method.md), [RootReferences2](icorprofilercallback2-rootreferences2-method.md), [HandleCreated](icorprofilercallback2-handlecreated-method.md),  [HandleDestroyed](icorprofilercallback2-handledestroyed-method.md), and [FinalizeableObjectQueued](icorprofilercallback2-finalizeableobjectqueued-method.md) callbacks in the `ICorProfilerCallback*` interfaces.</span></span> <span data-ttu-id="7cdda-134">当 `COR_PRF_MONITOR_GC` 分配时，将关闭并发垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="7cdda-134">When `COR_PRF_MONITOR_GC` is allocated, concurrent garbage collection is turned off.</span></span>|  
|`COR_PRF_MONITOR_JIT_COMPILATION`|<span data-ttu-id="7cdda-135">控制 `JITCompilation*` [ICorProfilerCallback](icorprofilercallback-interface.md)接口中的、 [JITFunctionPitched](icorprofilercallback-jitfunctionpitched-method.md)和[JITInlining](icorprofilercallback-jitinlining-method.md)回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-135">Controls the `JITCompilation*`, [JITFunctionPitched](icorprofilercallback-jitfunctionpitched-method.md), and [JITInlining](icorprofilercallback-jitinlining-method.md) callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_MODULE_LOADS`|<span data-ttu-id="7cdda-136">控制 `ModuleLoad*` `ModuleUnload*` [ICorProfilerCallback](icorprofilercallback-interface.md)接口中的、和[ModuleAttachedToAssembly](icorprofilercallback-moduleattachedtoassembly-method.md)回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-136">Controls the `ModuleLoad*`,  `ModuleUnload*`, and [ModuleAttachedToAssembly](icorprofilercallback-moduleattachedtoassembly-method.md) callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_OBJECT_ALLOCATED`|<span data-ttu-id="7cdda-137">控制[ICorProfilerCallback](icorprofilercallback-interface.md)接口中的[ObjectAllocated](icorprofilercallback-objectallocated-method.md)回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-137">Controls the [ObjectAllocated](icorprofilercallback-objectallocated-method.md) callback in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_REMOTING`|<span data-ttu-id="7cdda-138">控制 `Remoting*` [ICorProfilerCallback](icorprofilercallback-interface.md) 接口中的回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-138">Controls the `Remoting*` callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_REMOTING_ASYNC`|<span data-ttu-id="7cdda-139">控制 `Remoting*` 回调是否将监视异步事件。</span><span class="sxs-lookup"><span data-stu-id="7cdda-139">Controls whether the `Remoting*` callbacks will monitor asynchronous events.</span></span>|  
|`COR_PRF_MONITOR_REMOTING_COOKIE`|<span data-ttu-id="7cdda-140">控制是否向 `Remoting*` 回调传递 Cookie。</span><span class="sxs-lookup"><span data-stu-id="7cdda-140">Controls whether a cookie is passed to the `Remoting*` callbacks.</span></span>|  
|`COR_PRF_MONITOR_SUSPENDS`|<span data-ttu-id="7cdda-141">控制 `RuntimeSuspend*` `RuntimeResume*` [ICorProfilerCallback](icorprofilercallback-interface.md)接口中的、、 [RuntimeThreadSuspended](icorprofilercallback-runtimethreadsuspended-method.md)和[RuntimeThreadResumed](icorprofilercallback-runtimethreadresumed-method.md)回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-141">Controls the `RuntimeSuspend*`, `RuntimeResume*`, [RuntimeThreadSuspended](icorprofilercallback-runtimethreadsuspended-method.md), and [RuntimeThreadResumed](icorprofilercallback-runtimethreadresumed-method.md) callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) interface.</span></span>|  
|`COR_PRF_MONITOR_THREADS`|<span data-ttu-id="7cdda-142">控制[ICorProfilerCallback](icorprofilercallback-interface.md)和[ICorProfilerCallback2](icorprofilercallback2-interface.md)接口中的[ThreadCreated](icorprofilercallback-threadcreated-method.md)、 [ThreadDestroyed](icorprofilercallback-threaddestroyed-method.md)、 [ThreadAssignedToOSThread](icorprofilercallback-threadassignedtoosthread-method.md)和[ThreadNameChanged](icorprofilercallback2-threadnamechanged-method.md)回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-142">Controls the [ThreadCreated](icorprofilercallback-threadcreated-method.md),  [ThreadDestroyed](icorprofilercallback-threaddestroyed-method.md),  [ThreadAssignedToOSThread](icorprofilercallback-threadassignedtoosthread-method.md), and [ThreadNameChanged](icorprofilercallback2-threadnamechanged-method.md) callbacks in the [ICorProfilerCallback](icorprofilercallback-interface.md) and [ICorProfilerCallback2](icorprofilercallback2-interface.md) interfaces.</span></span>|  
  
<a name="Feature"></a>

### <a name="feature-enabling-flags"></a><span data-ttu-id="7cdda-143">功能启用标志</span><span class="sxs-lookup"><span data-stu-id="7cdda-143">Feature-enabling flags</span></span>  
  
|<span data-ttu-id="7cdda-144">成员</span><span class="sxs-lookup"><span data-stu-id="7cdda-144">Member</span></span>|<span data-ttu-id="7cdda-145">说明</span><span class="sxs-lookup"><span data-stu-id="7cdda-145">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_ENABLE_FRAME_INFO`|<span data-ttu-id="7cdda-146">`ClassID`通过使用 FunctionEnter2 回调返回的值调用[GetFunctionInfo2](icorprofilerinfo2-getfunctioninfo2-method.md)方法，实现对泛型函数的准确检索 `COR_PRF_FRAME_INFO` 。 [](functionenter2-function.md)</span><span class="sxs-lookup"><span data-stu-id="7cdda-146">Enables the retrieval of an exact `ClassID` for a generic function by calling the [GetFunctionInfo2](icorprofilerinfo2-getfunctioninfo2-method.md) method with a `COR_PRF_FRAME_INFO` value returned by the [FunctionEnter2](functionenter2-function.md) callback.</span></span>|  
|`COR_PRF_ENABLE_FUNCTION_ARGS`|<span data-ttu-id="7cdda-147">使用 [FunctionEnter2](functionenter2-function.md) 回调或 [FunctionEnter3WithInfo](functionenter3withinfo-function.md) 回调和 [GetFunctionEnter3Info](icorprofilerinfo3-getfunctionenter3info-method.md) 方法启用参数跟踪。</span><span class="sxs-lookup"><span data-stu-id="7cdda-147">Enables argument tracing using the [FunctionEnter2](functionenter2-function.md) callback or the [FunctionEnter3WithInfo](functionenter3withinfo-function.md) callback and the [GetFunctionEnter3Info](icorprofilerinfo3-getfunctionenter3info-method.md) method.</span></span>|  
|`COR_PRF_ENABLE_FUNCTION_RETVAL`|<span data-ttu-id="7cdda-148">启用使用 [FunctionLeave2](functionleave2-function.md) 回调或 [FunctionLeave3WithInfo](functionleave3withinfo-function.md) 回调和 [GetFunctionLeave3Info](icorprofilerinfo3-getfunctionleave3info-method.md) 方法跟踪返回值。</span><span class="sxs-lookup"><span data-stu-id="7cdda-148">Enables tracing of return values by using the [FunctionLeave2](functionleave2-function.md) callback or the [FunctionLeave3WithInfo](functionleave3withinfo-function.md) callback and [GetFunctionLeave3Info](icorprofilerinfo3-getfunctionleave3info-method.md) method.</span></span>|  
|`COR_PRF_ENABLE_INPROC_DEBUGGING`|<span data-ttu-id="7cdda-149">已弃用。</span><span class="sxs-lookup"><span data-stu-id="7cdda-149">Deprecated.</span></span><br /><br /> <span data-ttu-id="7cdda-150">不支持进程内调试。</span><span class="sxs-lookup"><span data-stu-id="7cdda-150">In process debugging is not supported.</span></span> <span data-ttu-id="7cdda-151">此标志无效。</span><span class="sxs-lookup"><span data-stu-id="7cdda-151">This flag has no effect.</span></span>|  
|`COR_PRF_ENABLE_JIT_MAPS`|<span data-ttu-id="7cdda-152">已弃用。</span><span class="sxs-lookup"><span data-stu-id="7cdda-152">Deprecated.</span></span><br /><br /> <span data-ttu-id="7cdda-153">允许探查器使用 [GetILToNativeMapping](icorprofilerinfo-getiltonativemapping-method.md)获取 IL 到本机映射。</span><span class="sxs-lookup"><span data-stu-id="7cdda-153">Allows the profiler to obtain IL-to-native maps by using [GetILToNativeMapping](icorprofilerinfo-getiltonativemapping-method.md).</span></span> <span data-ttu-id="7cdda-154">从 .NET Framework 2.0 开始，运行时始终跟踪从 IL 到本机代码的映射；因此，始终认为要设置此标志。</span><span class="sxs-lookup"><span data-stu-id="7cdda-154">Starting with the .NET Framework 2.0, the runtime always tracks IL-to-native maps; therefore, this flag is always considered to be set.</span></span>|  
|`COR_PRF_ENABLE_OBJECT_ALLOCATED`|<span data-ttu-id="7cdda-155">通知运行时：探查器可能需要对象分配通知。</span><span class="sxs-lookup"><span data-stu-id="7cdda-155">Informs the runtime that the profiler may want object allocation notifications.</span></span> <span data-ttu-id="7cdda-156">在初始化期间必须设置此标志。</span><span class="sxs-lookup"><span data-stu-id="7cdda-156">This flag must be set during initialization.</span></span> <span data-ttu-id="7cdda-157">它允许探查器随后使用该 `COR_PRF_MONITOR_OBJECT_ALLOCATED` 标志来接收 [ObjectAllocated](icorprofilercallback-objectallocated-method.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="7cdda-157">It allows the profiler to subsequently use the `COR_PRF_MONITOR_OBJECT_ALLOCATED` flag to receive [ObjectAllocated](icorprofilercallback-objectallocated-method.md) callbacks.</span></span>|  
|`COR_PRF_ENABLE_REJIT`|<span data-ttu-id="7cdda-158">启用对 [RequestReJIT](icorprofilerinfo4-requestrejit-method.md) 和 [RequestRevert](icorprofilerinfo4-requestrevert-method.md) 方法的调用。</span><span class="sxs-lookup"><span data-stu-id="7cdda-158">Enables calls to the [RequestReJIT](icorprofilerinfo4-requestrejit-method.md) and [RequestRevert](icorprofilerinfo4-requestrevert-method.md) methods.</span></span> <span data-ttu-id="7cdda-159">探查器必须在启动时设置此标志。</span><span class="sxs-lookup"><span data-stu-id="7cdda-159">The profiler must set this flag on startup.</span></span>  <span data-ttu-id="7cdda-160">如果探查器指定此标志，它还必须指定 `COR_PRF_DISABLE_ALL_NGEN_IMAGES`。</span><span class="sxs-lookup"><span data-stu-id="7cdda-160">If the profiler specifies this flag, it must also specify `COR_PRF_DISABLE_ALL_NGEN_IMAGES`.</span></span>|  
|`COR_PRF_ENABLE_STACK_SNAPSHOT`|<span data-ttu-id="7cdda-161">启用对 [DoStackSnapshot](icorprofilerinfo2-dostacksnapshot-method.md) 方法的调用。</span><span class="sxs-lookup"><span data-stu-id="7cdda-161">Enables calls to the [DoStackSnapshot](icorprofilerinfo2-dostacksnapshot-method.md) method.</span></span>|  
  
<a name="Config"></a>

### <a name="configuration-flags"></a><span data-ttu-id="7cdda-162">配置标志</span><span class="sxs-lookup"><span data-stu-id="7cdda-162">Configuration flags</span></span>  
  
|<span data-ttu-id="7cdda-163">成员</span><span class="sxs-lookup"><span data-stu-id="7cdda-163">Member</span></span>|<span data-ttu-id="7cdda-164">说明</span><span class="sxs-lookup"><span data-stu-id="7cdda-164">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_DISABLE_ALL_NGEN_IMAGES`|<span data-ttu-id="7cdda-165">阻止所有本机映像（包括增强型探查器映像）进行加载。</span><span class="sxs-lookup"><span data-stu-id="7cdda-165">Prevents all native images (including profiler-enhanced images) from loading.</span></span>  <span data-ttu-id="7cdda-166">如果此标志和 `COR_PRF_USE_PROFILE_IMAGES` 标志都已指定，将使用 `COR_PRF_DISABLE_ALL_NGEN_IMAGES`。</span><span class="sxs-lookup"><span data-stu-id="7cdda-166">If this flag and the `COR_PRF_USE_PROFILE_IMAGES` flag are both specified, `COR_PRF_DISABLE_ALL_NGEN_IMAGES` is used.</span></span>|  
|`COR_PRF_DISABLE_INLINING`|<span data-ttu-id="7cdda-167">禁用所有内联。</span><span class="sxs-lookup"><span data-stu-id="7cdda-167">Disables all inlining.</span></span>|  
|`COR_PRF_DISABLE_OPTIMIZATIONS`|<span data-ttu-id="7cdda-168">禁用所有代码优化。</span><span class="sxs-lookup"><span data-stu-id="7cdda-168">Disables all code optimizations.</span></span>|  
|`COR_PRF_DISABLE_TRANSPARENCY_CHECKS_UNDER_FULL_TRUST`|<span data-ttu-id="7cdda-169">禁用正常情况下在实时 (JIT) 编译和完全信任程序集类加载过程中完成的安全透明度检查。</span><span class="sxs-lookup"><span data-stu-id="7cdda-169">Disables security transparency checks that are normally done during just-in-time (JIT) compilation and class loading for full-trust assemblies.</span></span> <span data-ttu-id="7cdda-170">这可以使某些检测更容易执行。</span><span class="sxs-lookup"><span data-stu-id="7cdda-170">This can make some instrumentation easier to perform.</span></span>|  
|`COR_PRF_USE_PROFILE_IMAGES`|<span data-ttu-id="7cdda-171">导致执行本机映像搜索，以查找增强型探查器映像。</span><span class="sxs-lookup"><span data-stu-id="7cdda-171">Causes the native image search to look for profiler-enhanced images.</span></span> <span data-ttu-id="7cdda-172">对于给定程序集，如果找不到增强型探查器映像，则公共语言运行时将回退到该程序集的 JIT。</span><span class="sxs-lookup"><span data-stu-id="7cdda-172">If no profiler-enhanced image is found for a given assembly, the common language runtime falls back to JIT for that assembly.</span></span> <span data-ttu-id="7cdda-173">如果此标志和 `COR_PRF_DISABLE_ALL_NGEN_IMAGES` 标志都已指定，将使用 `COR_PRF_DISABLE_ALL_NGEN_IMAGES`。</span><span class="sxs-lookup"><span data-stu-id="7cdda-173">If this flag and the `COR_PRF_DISABLE_ALL_NGEN_IMAGES` flag are both specified, `COR_PRF_DISABLE_ALL_NGEN_IMAGES` is used.</span></span>|  
  
<a name="Composite"></a>

### <a name="composite-flags"></a><span data-ttu-id="7cdda-174">复合标志</span><span class="sxs-lookup"><span data-stu-id="7cdda-174">Composite flags</span></span>  
  
|<span data-ttu-id="7cdda-175">成员</span><span class="sxs-lookup"><span data-stu-id="7cdda-175">Member</span></span>|<span data-ttu-id="7cdda-176">说明</span><span class="sxs-lookup"><span data-stu-id="7cdda-176">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_ALL`|<span data-ttu-id="7cdda-177">表示所有 `COR_PRF_MONITOR` 标志值。</span><span class="sxs-lookup"><span data-stu-id="7cdda-177">Represents all `COR_PRF_MONITOR` flag values.</span></span>|  
|`COR_PRF_ALLOWABLE_AFTER_ATTACH`|<span data-ttu-id="7cdda-178">表示可以在将探查器附加到运行中的应用之后进行设置的所有 `COR_PRF_MONITOR` 标志。</span><span class="sxs-lookup"><span data-stu-id="7cdda-178">Represents all `COR_PRF_MONITOR` flags that can be set after the profiler is attached to a running app.</span></span> <span data-ttu-id="7cdda-179">语法部分指示此位掩码中存在的各个标志。</span><span class="sxs-lookup"><span data-stu-id="7cdda-179">The syntax section indicates the individual flags that are present in this bitmask.</span></span>|  
|`COR_PRF_MONITOR_ALL`|<span data-ttu-id="7cdda-180">启用所有回调事件。</span><span class="sxs-lookup"><span data-stu-id="7cdda-180">Enables all callback events.</span></span>|  
|`COR_PRF_MONITOR_IMMUTABLE`|<span data-ttu-id="7cdda-181">表示只能在初始化过程中进行设置的所有 `COR_PRF_MONITOR` 标志。</span><span class="sxs-lookup"><span data-stu-id="7cdda-181">Represents all `COR_PRF_MONITOR` flags that can be set only during initialization.</span></span> <span data-ttu-id="7cdda-182">如果在初始化后尝试更改这些标志中的任一标志，则会返回一个指示失败的 `HRESULT` 值。</span><span class="sxs-lookup"><span data-stu-id="7cdda-182">Trying to change any of these flags after initialization returns an `HRESULT` value that indicates failure.</span></span>|  
|`COR_PRF_REQUIRE_PROFILE_IMAGE`|<span data-ttu-id="7cdda-183">表示需要配置增强的映像的所有 `COR_PRF_MONITOR` 标志。</span><span class="sxs-lookup"><span data-stu-id="7cdda-183">Represents all `COR_PRF_MONITOR` flags that require profile-enhanced images.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7cdda-184">备注</span><span class="sxs-lookup"><span data-stu-id="7cdda-184">Remarks</span></span>  

 <span data-ttu-id="7cdda-185">将 `COR_PRF_MONITOR` 值与 [ICorProfilerInfo：： GetEventMask](icorprofilerinfo-geteventmask-method.md) 和 [ICorProfilerInfo：： SetEventMask](icorprofilerinfo-seteventmask-method.md) 方法一起使用，以定义公共语言运行时对探查器发出的事件通知。</span><span class="sxs-lookup"><span data-stu-id="7cdda-185">A `COR_PRF_MONITOR` value is used with the [ICorProfilerInfo::GetEventMask](icorprofilerinfo-geteventmask-method.md) and [ICorProfilerInfo::SetEventMask](icorprofilerinfo-seteventmask-method.md) methods to define the event notifications that the common language runtime makes to the profiler.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7cdda-186">要求</span><span class="sxs-lookup"><span data-stu-id="7cdda-186">Requirements</span></span>  

 <span data-ttu-id="7cdda-187">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7cdda-187">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7cdda-188">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7cdda-188">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7cdda-189">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7cdda-189">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7cdda-190">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7cdda-190">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7cdda-191">请参阅</span><span class="sxs-lookup"><span data-stu-id="7cdda-191">See also</span></span>

- [<span data-ttu-id="7cdda-192">分析枚举</span><span class="sxs-lookup"><span data-stu-id="7cdda-192">Profiling Enumerations</span></span>](profiling-enumerations.md)
- [<span data-ttu-id="7cdda-193">GetEventMask 方法</span><span class="sxs-lookup"><span data-stu-id="7cdda-193">GetEventMask Method</span></span>](icorprofilerinfo-geteventmask-method.md)
- [<span data-ttu-id="7cdda-194">SetEventMask 方法</span><span class="sxs-lookup"><span data-stu-id="7cdda-194">SetEventMask Method</span></span>](icorprofilerinfo-seteventmask-method.md)
