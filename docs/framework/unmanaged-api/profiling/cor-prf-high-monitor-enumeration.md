---
description: 了解详细信息： COR_PRF_HIGH_MONITOR 枚举
title: COR_PRF_HIGH_MONITOR 枚举
ms.date: 04/10/2018
ms.assetid: 3ba543d8-15e5-4322-b6e7-1ebfc92ed7dd
ms.openlocfilehash: 800bad21af96d8bbdf73f2af799f474f11294705
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648761"
---
# <a name="cor_prf_high_monitor-enumeration"></a><span data-ttu-id="18937-103">COR_PRF_HIGH_MONITOR 枚举</span><span class="sxs-lookup"><span data-stu-id="18937-103">COR_PRF_HIGH_MONITOR Enumeration</span></span>

<span data-ttu-id="18937-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="18937-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
<span data-ttu-id="18937-105">除了在 [COR_PRF_MONITOR](cor-prf-monitor-enumeration.md) 枚举中找到的标记外，还提供了标志，在加载时，探查器可以为 [ICorProfilerInfo5：： SetEventMask2](icorprofilerinfo5-seteventmask2-method.md) 方法指定这些标志。</span><span class="sxs-lookup"><span data-stu-id="18937-105">Provides flags in addition to those found in the [COR_PRF_MONITOR](cor-prf-monitor-enumeration.md) enumeration that the profiler can specify to the [ICorProfilerInfo5::SetEventMask2](icorprofilerinfo5-seteventmask2-method.md) method when it is loading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="18937-106">语法</span><span class="sxs-lookup"><span data-stu-id="18937-106">Syntax</span></span>  
  
```cpp
typedef enum {  
    COR_PRF_HIGH_MONITOR_NONE                     = 0x00000000,  
    COR_PRF_HIGH_ADD_ASSEMBLY_REFERENCES          = 0x00000001,  
    COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED        = 0x00000002,
    COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS = 0x00000004,
    COR_PRF_HIGH_DISABLE_TIERED_COMPILATION       = 0x00000008,
    COR_PRF_HIGH_BASIC_GC                         = 0x00000010,
    COR_PRF_HIGH_MONITOR_GC_MOVED_OBJECTS         = 0x00000020,
    COR_PRF_HIGH_MONITOR_LARGEOBJECT_ALLOCATED    = 0x00000040,
    COR_PRF_HIGH_REQUIRE_PROFILE_IMAGE            = 0,  
    COR_PRF_HIGH_ALLOWABLE_AFTER_ATTACH           = COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED |
                                                    COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS |
                                                    COR_PRF_HIGH_BASIC_GC |
                                                    COR_PRF_HIGH_MONITOR_GC_MOVED_OBJECTS |
                                                    COR_PRF_HIGH_MONITOR_LARGEOBJECT_ALLOCATED,  
    COR_PRF_HIGH_MONITOR_IMMUTABLE                = COR_PRF_HIGH_DISABLE_TIERED_COMPILATION  
} COR_PRF_HIGH_MONITOR;  
```  
  
## <a name="members"></a><span data-ttu-id="18937-107">成员</span><span class="sxs-lookup"><span data-stu-id="18937-107">Members</span></span>  
  
|<span data-ttu-id="18937-108">成员</span><span class="sxs-lookup"><span data-stu-id="18937-108">Member</span></span>|<span data-ttu-id="18937-109">说明</span><span class="sxs-lookup"><span data-stu-id="18937-109">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_HIGH_MONITOR_NONE`|<span data-ttu-id="18937-110">不设置任何标志。</span><span class="sxs-lookup"><span data-stu-id="18937-110">No flags are set.</span></span>|  
|`COR_PRF_HIGH_ADD_ASSEMBLY_REFERENCES`|<span data-ttu-id="18937-111">控制在 CLR 程序集引用闭包遍历期间添加程序集引用的 [ICorProfilerCallback6：： GetAssemblyReference](icorprofilercallback6-getassemblyreferences-method.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="18937-111">Controls the [ICorProfilerCallback6::GetAssemblyReference](icorprofilercallback6-getassemblyreferences-method.md) callback for adding assembly references during the CLR assembly reference closure walk.</span></span>|  
|`COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED`|<span data-ttu-id="18937-112">控制与内存中模块关联的符号流更新的 [ICorProfilerCallback7：： ModuleInMemorySymbolsUpdated](icorprofilercallback7-moduleinmemorysymbolsupdated-method.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="18937-112">Controls the [ICorProfilerCallback7::ModuleInMemorySymbolsUpdated](icorprofilercallback7-moduleinmemorysymbolsupdated-method.md) callback for updates to the symbol stream associated with an in-memory module.</span></span>|  
|`COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS`|<span data-ttu-id="18937-113">控制 [ICorProfilerCallback9：:D ynamicmethodunloaded](icorprofilercallback9-dynamicmethodunloaded-method.md) 回调，用于指示动态方法何时被垃圾回收和卸载。</span><span class="sxs-lookup"><span data-stu-id="18937-113">Controls the [ICorProfilerCallback9::DynamicMethodUnloaded](icorprofilercallback9-dynamicmethodunloaded-method.md) callback for indicating when a dynamic method has been garbage collected and unloaded.</span></span> <br/> [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]|
|`COR_PRF_HIGH_DISABLE_TIERED_COMPILATION`|<span data-ttu-id="18937-114">仅适用于 .NET Core 3.0 和更高版本：禁用探查器的 [分层编译](../../../core/whats-new/dotnet-core-3-0.md) 。</span><span class="sxs-lookup"><span data-stu-id="18937-114">.NET Core 3.0 and later versions only: Disables [tiered compilation](../../../core/whats-new/dotnet-core-3-0.md) for profilers.</span></span>|
|`COR_PRF_HIGH_BASIC_GC`|<span data-ttu-id="18937-115">仅适用于 .NET Core 3.0 和更高版本：提供与相同的轻型 GC 分析选项 [`COR_PRF_MONITOR_GC`](cor-prf-monitor-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="18937-115">.NET Core 3.0 and later versions only: Provides a lightweight GC profiling option compared to [`COR_PRF_MONITOR_GC`](cor-prf-monitor-enumeration.md).</span></span> <span data-ttu-id="18937-116">仅控制  [GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md)、 [GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md)和 [GetGenerationBounds](icorprofilerinfo2-getgenerationbounds-method.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="18937-116">Controls only the  [GarbageCollectionStarted](icorprofilercallback2-garbagecollectionstarted-method.md), [GarbageCollectionFinished](icorprofilercallback2-garbagecollectionfinished-method.md), and [GetGenerationBounds](icorprofilerinfo2-getgenerationbounds-method.md) callbacks.</span></span> <span data-ttu-id="18937-117">不同于 `COR_PRF_MONITOR_GC` 标志，不 `COR_PRF_HIGH_BASIC_GC` 会禁用并发垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="18937-117">Unlike the `COR_PRF_MONITOR_GC` flag, `COR_PRF_HIGH_BASIC_GC` does not disable concurrent garbage collection.</span></span>|
|`COR_PRF_HIGH_MONITOR_GC_MOVED_OBJECTS`|<span data-ttu-id="18937-118">仅适用于 .NET Core 3.0 和更高版本：仅为压缩 Gc 启用 [MovedReferences](icorprofilercallback-movedreferences-method.md) 和 [MovedReferences2](icorprofilercallback4-movedreferences2-method.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="18937-118">.NET Core 3.0 and later versions only: Enables the [MovedReferences](icorprofilercallback-movedreferences-method.md) and [MovedReferences2](icorprofilercallback4-movedreferences2-method.md) callbacks for compacting GCs only.</span></span>|
|`COR_PRF_HIGH_MONITOR_LARGEOBJECT_ALLOCATED`|<span data-ttu-id="18937-119">仅限 .NET Core 3.0 及更高版本：类似于 [`COR_PRF_MONITOR_OBJECT_ALLOCATED`](cor-prf-monitor-enumeration.md) ，但仅提供有关大型对象堆的对象分配的信息 (LOH) 。</span><span class="sxs-lookup"><span data-stu-id="18937-119">.NET Core 3.0 and later versions only: Similar to [`COR_PRF_MONITOR_OBJECT_ALLOCATED`](cor-prf-monitor-enumeration.md), but provides information on object allocations for the large object heap (LOH) only.</span></span>|
|`COR_PRF_HIGH_REQUIRE_PROFILE_IMAGE`|<span data-ttu-id="18937-120">表示需要配置增强的映像的所有 `COR_PRF_HIGH_MONITOR` 标志。</span><span class="sxs-lookup"><span data-stu-id="18937-120">Represents all `COR_PRF_HIGH_MONITOR` flags that require profile-enhanced images.</span></span> <span data-ttu-id="18937-121">它对应于 `COR_PRF_REQUIRE_PROFILE_IMAGE` [COR_PRF_MONITOR](cor-prf-monitor-enumeration.md) 枚举中的标志。</span><span class="sxs-lookup"><span data-stu-id="18937-121">It corresponds to the `COR_PRF_REQUIRE_PROFILE_IMAGE` flag in the [COR_PRF_MONITOR](cor-prf-monitor-enumeration.md) enumeration.</span></span>|  
|`COR_PRF_HIGH_ALLOWABLE_AFTER_ATTACH`|<span data-ttu-id="18937-122">表示可以在将探查器附加到运行中的应用之后进行设置的所有 `COR_PRF_HIGH_MONITOR` 标志。</span><span class="sxs-lookup"><span data-stu-id="18937-122">Represents all `COR_PRF_HIGH_MONITOR` flags that can be set after the profiler is attached to a running app.</span></span>|  
|`COR_PRF_HIGH_MONITOR_IMMUTABLE`|<span data-ttu-id="18937-123">表示只能在初始化过程中进行设置的所有 `COR_PRF_HIGH_MONITOR` 标志。</span><span class="sxs-lookup"><span data-stu-id="18937-123">Represents all `COR_PRF_HIGH_MONITOR` flags that can be set only during initialization.</span></span> <span data-ttu-id="18937-124">如果尝试从其他位置更改这些标志中的任何一个标志，则会产生一个指示失败的 `HRESULT` 值。</span><span class="sxs-lookup"><span data-stu-id="18937-124">Trying to change any of these flags elsewhere results in an `HRESULT` value that indicates failure.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="18937-125">备注</span><span class="sxs-lookup"><span data-stu-id="18937-125">Remarks</span></span>

<span data-ttu-id="18937-126">`COR_PRF_HIGH_MONITOR`标志与 `pdwEventsHigh` [ICorProfilerInfo5：： GetEventMask2](icorprofilerinfo5-geteventmask2-method.md)和[ICorProfilerInfo5：： SetEventMask2](icorprofilerinfo5-seteventmask2-method.md)方法的参数一起使用。</span><span class="sxs-lookup"><span data-stu-id="18937-126">The `COR_PRF_HIGH_MONITOR` flags are used with the `pdwEventsHigh` parameter of the [ICorProfilerInfo5::GetEventMask2](icorprofilerinfo5-geteventmask2-method.md) and [ICorProfilerInfo5::SetEventMask2](icorprofilerinfo5-seteventmask2-method.md) methods.</span></span>  
  
<span data-ttu-id="18937-127">从 .NET Framework 4.6.1 开始，的值 `COR_PRF_HIGH_ALLOWABLE_AFTER_ATTACH` 从0更改为 `COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED` (0x00000002) 。</span><span class="sxs-lookup"><span data-stu-id="18937-127">Starting with the .NET Framework 4.6.1, the value of the `COR_PRF_HIGH_ALLOWABLE_AFTER_ATTACH` changed from 0 to `COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED` (0x00000002).</span></span> <span data-ttu-id="18937-128">从 .NET Framework 4.7.2 开始，其值从更改 `COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED` 为 `COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED | COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS` 。</span><span class="sxs-lookup"><span data-stu-id="18937-128">Starting with the .NET Framework 4.7.2, its value changed from `COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED` to `COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED | COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS`.</span></span>

<span data-ttu-id="18937-129">`COR_PRF_HIGH_MONITOR_IMMUTABLE` 旨在作为位掩码，表示只能在初始化期间设置的所有标志。</span><span class="sxs-lookup"><span data-stu-id="18937-129">`COR_PRF_HIGH_MONITOR_IMMUTABLE` is intended to be a bitmask that represents all flags that can only be set during initialization.</span></span> <span data-ttu-id="18937-130">尝试在其他任何位置更改这些标志会导致失败 `HRESULT` 。</span><span class="sxs-lookup"><span data-stu-id="18937-130">Trying to change any of these flags elsewhere results in a failed `HRESULT`.</span></span>

## <a name="requirements"></a><span data-ttu-id="18937-131">要求</span><span class="sxs-lookup"><span data-stu-id="18937-131">Requirements</span></span>

<span data-ttu-id="18937-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="18937-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
<span data-ttu-id="18937-133">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="18937-133">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="18937-134">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="18937-134">**Library:** CorGuids.lib</span></span>  
  
<span data-ttu-id="18937-135">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="18937-135">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18937-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="18937-136">See also</span></span>

- [<span data-ttu-id="18937-137">分析枚举</span><span class="sxs-lookup"><span data-stu-id="18937-137">Profiling Enumerations</span></span>](profiling-enumerations.md)
- [<span data-ttu-id="18937-138">COR_PRF_MONITOR 枚举</span><span class="sxs-lookup"><span data-stu-id="18937-138">COR_PRF_MONITOR Enumeration</span></span>](cor-prf-monitor-enumeration.md)
- [<span data-ttu-id="18937-139">ICorProfilerInfo5 接口</span><span class="sxs-lookup"><span data-stu-id="18937-139">ICorProfilerInfo5 Interface</span></span>](icorprofilerinfo5-interface.md)
