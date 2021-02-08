---
description: 了解详细信息： ICorProfilerCallback4：： ReJITCompilationFinished 方法
title: ICorProfilerCallback4::ReJITCompilationFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback4.ReJITCompilationFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback4::ReJITCompilationFinished
helpviewer_keywords:
- ICorProfilerCallback4::ReJITCompilationFinished method [.NET Framework profiling]
- ReJITCompilationFinished method, ICorProfilerCallback4 interface [.NET Framework profiling]
ms.assetid: 3b5cff02-2005-44eb-a2bc-50214c4b0e1d
topic_type:
- apiref
ms.openlocfilehash: 2d7270b5a8cf31fd81505c148429da5f7025319a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788717"
---
# <a name="icorprofilercallback4rejitcompilationfinished-method"></a><span data-ttu-id="931b3-103">ICorProfilerCallback4::ReJITCompilationFinished 方法</span><span class="sxs-lookup"><span data-stu-id="931b3-103">ICorProfilerCallback4::ReJITCompilationFinished Method</span></span>

<span data-ttu-id="931b3-104">通知探查器实时 (JIT) 编译器已经完成了对函数的重新编译。</span><span class="sxs-lookup"><span data-stu-id="931b3-104">Notifies the profiler that the just-in-time (JIT) compiler has finished recompiling a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="931b3-105">语法</span><span class="sxs-lookup"><span data-stu-id="931b3-105">Syntax</span></span>  
  
```cpp  
HRESULT ReJITCompilationFinished(  
    [in] FunctionID functionId,    [in] ReJITID rejitId,  
    [in] HRESULT    hrStatus,  
    [in] BOOL       fIsSafeToBlock);  
```  
  
## <a name="parameters"></a><span data-ttu-id="931b3-106">参数</span><span class="sxs-lookup"><span data-stu-id="931b3-106">Parameters</span></span>  

 `functionId`  
 <span data-ttu-id="931b3-107">中已重新编译的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="931b3-107">[in] The ID of the function that was recompiled.</span></span>  
  
 `rejitId`  
 <span data-ttu-id="931b3-108">[in] JIT 重新编译的函数的标识。</span><span class="sxs-lookup"><span data-stu-id="931b3-108">[in] The identity of the JIT-recompiled function.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="931b3-109">中一个值，该值指示 JIT 重新编译是否成功。</span><span class="sxs-lookup"><span data-stu-id="931b3-109">[in] A value that indicates whether the JIT recompilation was successful.</span></span>  
  
 `fIsSafeToBlock`  
 <span data-ttu-id="931b3-110">[in] `true` 指示阻止可能会导致运行时等待调用线程从该回调返回; `false` 指示阻止操作不会影响运行时的操作。</span><span class="sxs-lookup"><span data-stu-id="931b3-110">[in] `true` to indicate that blocking may cause the runtime to wait for the calling thread to return from this callback; `false` to indicate that blocking will not affect the operation of the runtime.</span></span>  
  
 <span data-ttu-id="931b3-111">的值 `true` 不会损害运行时，但会影响分析结果。</span><span class="sxs-lookup"><span data-stu-id="931b3-111">A value of `true` does not harm the runtime, but can affect the profiling results.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="931b3-112">要求</span><span class="sxs-lookup"><span data-stu-id="931b3-112">Requirements</span></span>  

 <span data-ttu-id="931b3-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="931b3-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="931b3-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="931b3-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="931b3-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="931b3-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="931b3-116">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="931b3-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="931b3-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="931b3-117">See also</span></span>

- [<span data-ttu-id="931b3-118">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="931b3-118">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="931b3-119">ICorProfilerCallback4 接口</span><span class="sxs-lookup"><span data-stu-id="931b3-119">ICorProfilerCallback4 Interface</span></span>](icorprofilercallback4-interface.md)
- [<span data-ttu-id="931b3-120">JITCompilationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="931b3-120">JITCompilationStarted Method</span></span>](icorprofilercallback-jitcompilationstarted-method.md)
- [<span data-ttu-id="931b3-121">ReJITCompilationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="931b3-121">ReJITCompilationStarted Method</span></span>](icorprofilercallback4-rejitcompilationstarted-method.md)
