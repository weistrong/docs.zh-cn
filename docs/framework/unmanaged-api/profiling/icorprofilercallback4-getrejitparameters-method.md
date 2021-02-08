---
description: 了解详细信息： ICorProfilerCallback4：： GetReJITParameters 方法
title: ICorProfilerCallback4::GetReJITParameters 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback4.GetReJITParameters
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback4::GetReJITParameters
helpviewer_keywords:
- ICorProfilerCallback4::GetReJITParameters method [.NET Framework profiling]
- GetReJITParameters method, ICorProfilerCallback4 interface [.NET Framework profiling]
ms.assetid: 0e9bfe07-9f20-498c-b568-9017c8f6056c
topic_type:
- apiref
ms.openlocfilehash: f8dbf2c6ae80e41b8427fdaf0ef617a83138bb14
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788756"
---
# <a name="icorprofilercallback4getrejitparameters-method"></a><span data-ttu-id="58877-103">ICorProfilerCallback4::GetReJITParameters 方法</span><span class="sxs-lookup"><span data-stu-id="58877-103">ICorProfilerCallback4::GetReJITParameters Method</span></span>

<span data-ttu-id="58877-104">允许代码探查器为新的重新编译的方法体设置备用代码生成标志。</span><span class="sxs-lookup"><span data-stu-id="58877-104">Allows the code profiler to set alternate code generation flags for a new recompiled method body.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58877-105">语法</span><span class="sxs-lookup"><span data-stu-id="58877-105">Syntax</span></span>  
  
```cpp  
HRESULT GetReJITParameters(     [in] ModuleID moduleId,     [in] mdMethodDef methodId,     [in] ICorProfilerFunctionControl *pFunctionControl);  
```  
  
## <a name="parameters"></a><span data-ttu-id="58877-106">参数</span><span class="sxs-lookup"><span data-stu-id="58877-106">Parameters</span></span>  

 `moduleID`  
 <span data-ttu-id="58877-107">中包含 CLR 需要 JIT 重新编译参数的方法的模块。</span><span class="sxs-lookup"><span data-stu-id="58877-107">[in] The module that contains the method for which the CLR needs JIT recompilation parameters.</span></span>  
  
 `methodId`  
 <span data-ttu-id="58877-108">中 `MethodDef` CLR 需要 JIT 重新编译参数的方法的。</span><span class="sxs-lookup"><span data-stu-id="58877-108">[in] The `MethodDef` of the method for which the CLR needs JIT recompilation parameters.</span></span>  
  
 `pFunctionControl`  
 <span data-ttu-id="58877-109">中指向 [ICorProfilerFunctionControl](icorprofilerfunctioncontrol-interface.md) 接口的指针，探查器可以使用该接口为要重新编译的方法提供 JIT 重新编译信息。</span><span class="sxs-lookup"><span data-stu-id="58877-109">[in] A pointer to an [ICorProfilerFunctionControl](icorprofilerfunctioncontrol-interface.md) interface that the profiler can use to provide JIT recompilation information for the method being recompiled.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="58877-110">备注</span><span class="sxs-lookup"><span data-stu-id="58877-110">Remarks</span></span>  

 <span data-ttu-id="58877-111">CLR 发出 `GetReJITParameters` 回调，以便探查器可以指定用于重新编译给定方法的参数。</span><span class="sxs-lookup"><span data-stu-id="58877-111">The CLR issues a `GetReJITParameters` callback so that the profiler can specify the parameters for recompiling a given method.</span></span> <span data-ttu-id="58877-112">`GetReJITParameters`仅对每个函数发出一次回调; 探查器提供的参数将应用于该函数的所有实例。</span><span class="sxs-lookup"><span data-stu-id="58877-112">The `GetReJITParameters` callback is issued only once per function; the parameters supplied by the profiler apply to all instances of that function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="58877-113">要求</span><span class="sxs-lookup"><span data-stu-id="58877-113">Requirements</span></span>  

 <span data-ttu-id="58877-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="58877-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58877-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="58877-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="58877-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="58877-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="58877-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58877-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58877-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="58877-118">See also</span></span>

- [<span data-ttu-id="58877-119">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="58877-119">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="58877-120">ICorProfilerCallback4 接口</span><span class="sxs-lookup"><span data-stu-id="58877-120">ICorProfilerCallback4 Interface</span></span>](icorprofilercallback4-interface.md)
- [<span data-ttu-id="58877-121">JITCompilationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="58877-121">JITCompilationStarted Method</span></span>](icorprofilercallback-jitcompilationstarted-method.md)
- [<span data-ttu-id="58877-122">ReJITCompilationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="58877-122">ReJITCompilationStarted Method</span></span>](icorprofilercallback4-rejitcompilationstarted-method.md)
