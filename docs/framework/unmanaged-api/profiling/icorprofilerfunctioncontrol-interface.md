---
description: 了解详细信息： ICorProfilerFunctionControl 接口
title: ICorProfilerFunctionControl 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionControl
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionControl
helpviewer_keywords:
- ICorProfilerFunctionControl interface [.NET Framework profiling]
ms.assetid: 4e3d3141-4662-4166-8f05-bc857c1b4216
topic_type:
- apiref
ms.openlocfilehash: 7b4ac58d2b8754108b4e10493596776987a93a49
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753310"
---
# <a name="icorprofilerfunctioncontrol-interface"></a><span data-ttu-id="5f781-103">ICorProfilerFunctionControl 接口</span><span class="sxs-lookup"><span data-stu-id="5f781-103">ICorProfilerFunctionControl Interface</span></span>

<span data-ttu-id="5f781-104">提供允许代码探查器与公共语言运行时 (CLR) 进行通信的方法，从而在重新编译特定方法时控制 JIT 探查器应生成代码的方式。</span><span class="sxs-lookup"><span data-stu-id="5f781-104">Provides methods that allow a code profiler to communicate with the common language runtime (CLR) to control how the JIT compiler should generate code when recompiling a specific method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5f781-105">方法</span><span class="sxs-lookup"><span data-stu-id="5f781-105">Methods</span></span>  
  
|<span data-ttu-id="5f781-106">方法</span><span class="sxs-lookup"><span data-stu-id="5f781-106">Method</span></span>|<span data-ttu-id="5f781-107">说明</span><span class="sxs-lookup"><span data-stu-id="5f781-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5f781-108">SetCodegenFlags 方法</span><span class="sxs-lookup"><span data-stu-id="5f781-108">SetCodegenFlags Method</span></span>](icorprofilerfunctioncontrol-setcodegenflags-method.md)|<span data-ttu-id="5f781-109">设置 [COR_PRF_CODEGEN_FLAGS](cor-prf-codegen-flags-enumeration.md) 枚举中的一个或多个标志，以控制实时 (JIT) 重新编译函数的代码生成。</span><span class="sxs-lookup"><span data-stu-id="5f781-109">Sets one or more flags from the [COR_PRF_CODEGEN_FLAGS](cor-prf-codegen-flags-enumeration.md) enumeration to control code generation for a just-in-time (JIT) recompiled function.</span></span>|  
|[<span data-ttu-id="5f781-110">SetILFunctionBody 方法</span><span class="sxs-lookup"><span data-stu-id="5f781-110">SetILFunctionBody Method</span></span>](icorprofilerfunctioncontrol-setilfunctionbody-method.md)|<span data-ttu-id="5f781-111">替换方法的公共中间语言 (CIL) 主体。</span><span class="sxs-lookup"><span data-stu-id="5f781-111">Replaces the Common Intermediate Language (CIL) body of the method.</span></span>|  
|[<span data-ttu-id="5f781-112">SetILInstrumentedCodeMap 方法</span><span class="sxs-lookup"><span data-stu-id="5f781-112">SetILInstrumentedCodeMap Method</span></span>](icorprofilerfunctioncontrol-setilinstrumentedcodemap-method.md)|<span data-ttu-id="5f781-113">使用指定的公共中间语言 (CIL) 映射项为指定的函数设置代码图。</span><span class="sxs-lookup"><span data-stu-id="5f781-113">Sets a code map for the specified function by using the specified Common Intermediate Language (CIL) map entries.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5f781-114">备注</span><span class="sxs-lookup"><span data-stu-id="5f781-114">Remarks</span></span>  

 <span data-ttu-id="5f781-115">`ICorProfilerFunctionControl` 接口提供了用于控制单个重新编译函数的代码生成的方法。</span><span class="sxs-lookup"><span data-stu-id="5f781-115">The `ICorProfilerFunctionControl` interface provides methods for controlling code generation for a single recompiled function.</span></span> <span data-ttu-id="5f781-116">探查器通过 [ICorProfilerCallback4：： GetReJITParameters](icorprofilercallback4-getrejitparameters-method.md) 回调获取此接口的实例。</span><span class="sxs-lookup"><span data-stu-id="5f781-116">The profiler obtains an instance of this interface through the [ICorProfilerCallback4::GetReJITParameters](icorprofilercallback4-getrejitparameters-method.md) callback.</span></span> <span data-ttu-id="5f781-117">`ICorProfilerFunctionControl` 的每个实例都可控制一个函数的所有实例。</span><span class="sxs-lookup"><span data-stu-id="5f781-117">Each instance of `ICorProfilerFunctionControl` controls all instances of one function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f781-118">要求</span><span class="sxs-lookup"><span data-stu-id="5f781-118">Requirements</span></span>  

 <span data-ttu-id="5f781-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f781-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f781-120">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5f781-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5f781-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5f781-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5f781-122">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f781-122">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f781-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f781-123">See also</span></span>

- [<span data-ttu-id="5f781-124">ICorProfilerInfo4 接口</span><span class="sxs-lookup"><span data-stu-id="5f781-124">ICorProfilerInfo4 Interface</span></span>](icorprofilerinfo4-interface.md)
- [<span data-ttu-id="5f781-125">分析接口</span><span class="sxs-lookup"><span data-stu-id="5f781-125">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="5f781-126">EnumJITedFunctions2 方法</span><span class="sxs-lookup"><span data-stu-id="5f781-126">EnumJITedFunctions2 Method</span></span>](icorprofilerinfo4-enumjitedfunctions2-method.md)
