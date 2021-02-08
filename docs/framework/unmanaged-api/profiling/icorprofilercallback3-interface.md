---
description: 了解详细信息： ICorProfilerCallback3 接口
title: ICorProfilerCallback3 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback3
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback3
helpviewer_keywords:
- ICorProfilerCallback3 interface [.NET Framework profiling]
ms.assetid: be83af41-3dec-4c77-8529-9dd6b8042af6
topic_type:
- apiref
ms.openlocfilehash: 70fba8768fef5da411b566d918308989a3f6e863
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788795"
---
# <a name="icorprofilercallback3-interface"></a><span data-ttu-id="a26c6-103">ICorProfilerCallback3 接口</span><span class="sxs-lookup"><span data-stu-id="a26c6-103">ICorProfilerCallback3 Interface</span></span>

<span data-ttu-id="a26c6-104">提供公共语言运行时 (CLR) 用来向探查器传达附加和分离状态信息的回调方法。</span><span class="sxs-lookup"><span data-stu-id="a26c6-104">Provides callback methods that the common language runtime (CLR) uses to communicate attach and detach state information to the profiler.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a26c6-105">方法</span><span class="sxs-lookup"><span data-stu-id="a26c6-105">Methods</span></span>  
  
|<span data-ttu-id="a26c6-106">方法</span><span class="sxs-lookup"><span data-stu-id="a26c6-106">Method</span></span>|<span data-ttu-id="a26c6-107">说明</span><span class="sxs-lookup"><span data-stu-id="a26c6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a26c6-108">InitializeForAttach 方法</span><span class="sxs-lookup"><span data-stu-id="a26c6-108">InitializeForAttach Method</span></span>](icorprofilercallback3-initializeforattach-method.md)|<span data-ttu-id="a26c6-109">由 CLR 调用，以使探查器能够在附加操作后初始化其状态。</span><span class="sxs-lookup"><span data-stu-id="a26c6-109">Called by the CLR to give the profiler an opportunity to initialize its state after an attach operation.</span></span>|  
|[<span data-ttu-id="a26c6-110">ProfilerAttachComplete 方法</span><span class="sxs-lookup"><span data-stu-id="a26c6-110">ProfilerAttachComplete Method</span></span>](icorprofilercallback3-profilerattachcomplete-method.md)|<span data-ttu-id="a26c6-111">由 CLR 调用以指示探查器现在可以调用追赶方法。</span><span class="sxs-lookup"><span data-stu-id="a26c6-111">Called by the CLR to indicate that the profiler can now call the catch-up methods.</span></span>|  
|[<span data-ttu-id="a26c6-112">ProfilerDetachSucceeded 方法</span><span class="sxs-lookup"><span data-stu-id="a26c6-112">ProfilerDetachSucceeded Method</span></span>](icorprofilercallback3-profilerdetachsucceeded-method.md)|<span data-ttu-id="a26c6-113">通知探查器公共语言运行时 (CLR) 将要卸载探查器 DLL。</span><span class="sxs-lookup"><span data-stu-id="a26c6-113">Notifies the profiler that the common language runtime (CLR) is about to unload the profiler DLL.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a26c6-114">备注</span><span class="sxs-lookup"><span data-stu-id="a26c6-114">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a26c6-115">要求</span><span class="sxs-lookup"><span data-stu-id="a26c6-115">Requirements</span></span>  

 <span data-ttu-id="a26c6-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a26c6-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a26c6-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a26c6-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a26c6-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a26c6-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a26c6-119">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a26c6-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a26c6-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="a26c6-120">See also</span></span>

- [<span data-ttu-id="a26c6-121">分析接口</span><span class="sxs-lookup"><span data-stu-id="a26c6-121">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="a26c6-122">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="a26c6-122">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="a26c6-123">ICorProfilerCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="a26c6-123">ICorProfilerCallback2 Interface</span></span>](icorprofilercallback2-interface.md)
- [<span data-ttu-id="a26c6-124">ICorProfilerCallback4 接口</span><span class="sxs-lookup"><span data-stu-id="a26c6-124">ICorProfilerCallback4 Interface</span></span>](icorprofilercallback4-interface.md)
