---
description: 了解详细信息： ICorProfilerCallback7：： ModuleInMemorySymbolsUpdated 方法
title: ICorProfilerCallback7：： ModuleInMemorySymbolsUpdated 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback7.ModuleInMemorySymbolsUpdated
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.assetid: f362a896-3247-4894-9727-e48dbbcd2c78
ms.openlocfilehash: 74adf7edc5269824a924933eb3284a5964e1bac1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781722"
---
# <a name="icorprofilercallback7moduleinmemorysymbolsupdated-method"></a><span data-ttu-id="7d03f-103">ICorProfilerCallback7：： ModuleInMemorySymbolsUpdated 方法</span><span class="sxs-lookup"><span data-stu-id="7d03f-103">ICorProfilerCallback7::ModuleInMemorySymbolsUpdated Method</span></span>

<span data-ttu-id="7d03f-104">[仅在 .NET Framework 4.6.1 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="7d03f-104">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="7d03f-105">只要更新与内存中模块关联的符号流，就会通知探查器。</span><span class="sxs-lookup"><span data-stu-id="7d03f-105">Notifies the profiler whenever the symbol stream associated with an in-memory module is updated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d03f-106">语法</span><span class="sxs-lookup"><span data-stu-id="7d03f-106">Syntax</span></span>  
  
```cpp  
HRESULT ModuleInMemorySymbolsUpdated(  
     ModuleID moduleId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7d03f-107">参数</span><span class="sxs-lookup"><span data-stu-id="7d03f-107">Parameters</span></span>  

 <span data-ttu-id="7d03f-108">[in] `moduleId`</span><span class="sxs-lookup"><span data-stu-id="7d03f-108">[in] `moduleId`</span></span>  
 <span data-ttu-id="7d03f-109">已更新其符号流的内存中模块的标识符。</span><span class="sxs-lookup"><span data-stu-id="7d03f-109">The identifier of the in-memory module whose symbol stream is updated.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7d03f-110">备注</span><span class="sxs-lookup"><span data-stu-id="7d03f-110">Remarks</span></span>  

 <span data-ttu-id="7d03f-111">调用[ICorProfilerCallback5：： SetEventMask2](icorprofilerinfo5-seteventmask2-method.md)方法时，可通过设置[COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED](cor-prf-high-monitor-enumeration.md)事件掩码标志来控制此回调。</span><span class="sxs-lookup"><span data-stu-id="7d03f-111">This callback is controlled by setting the [COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED](cor-prf-high-monitor-enumeration.md) event mask flag when calling the [ICorProfilerCallback5::SetEventMask2](icorprofilerinfo5-seteventmask2-method.md) method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7d03f-112">当前不会对通过 api 隐式创建或修改的符号引发此事件 <xref:System.Reflection.Emit> 。</span><span class="sxs-lookup"><span data-stu-id="7d03f-112">This event is not currently raised for symbols implicitly created or modified via <xref:System.Reflection.Emit> APIs.</span></span>  
  
 <span data-ttu-id="7d03f-113">即使在对包含参数的托管方法的重载之一的调用中预先提供了符号 <xref:System.Reflection.Assembly.Load%2A?displayProperty=nameWithType> `rawSymbolStore` 来指定程序集的符号，运行时也不会实际将符号数据与模块相关联，直到发生 [ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="7d03f-113">Even when symbols are provided up front in a call to one of the overloads of the managed <xref:System.Reflection.Assembly.Load%2A?displayProperty=nameWithType> methods that includes a `rawSymbolStore` argument to specify the symbols for the assembly, the runtime may not actually associate the symbolic data with the module until after the [ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) callback has occurred.</span></span> <span data-ttu-id="7d03f-114">此事件提供稍后的机会来收集此类模块的符号。</span><span class="sxs-lookup"><span data-stu-id="7d03f-114">This event provides a later opportunity to collect symbols for such modules.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7d03f-115">要求</span><span class="sxs-lookup"><span data-stu-id="7d03f-115">Requirements</span></span>  

 <span data-ttu-id="7d03f-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7d03f-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7d03f-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7d03f-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7d03f-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7d03f-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7d03f-119">**.NET Framework 版本：**[!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7d03f-119">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d03f-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="7d03f-120">See also</span></span>

- [<span data-ttu-id="7d03f-121">ModuleLoadFinished 方法</span><span class="sxs-lookup"><span data-stu-id="7d03f-121">ModuleLoadFinished Method</span></span>](icorprofilercallback-moduleloadfinished-method.md)
- [<span data-ttu-id="7d03f-122">SetEventMask2 方法</span><span class="sxs-lookup"><span data-stu-id="7d03f-122">SetEventMask2 Method</span></span>](icorprofilerinfo5-seteventmask2-method.md)
- [<span data-ttu-id="7d03f-123">ICorProfilerCallback7 接口</span><span class="sxs-lookup"><span data-stu-id="7d03f-123">ICorProfilerCallback7 Interface</span></span>](icorprofilercallback7-interface.md)
