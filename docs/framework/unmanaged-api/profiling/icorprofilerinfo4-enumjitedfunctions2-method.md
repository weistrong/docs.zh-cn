---
description: 了解详细信息： ICorProfilerInfo4：： EnumJITedFunctions2 方法
title: ICorProfilerInfo4::EnumJITedFunctions2 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.EnumJITedFunctions2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::EnumJITedFunctions2
helpviewer_keywords:
- EnumJITedFunctions2 method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::EnumJITedFunctions2 method [.NET Framework profiling]
ms.assetid: 40e9a1be-9bd2-4fad-9921-34a84b61c1e3
topic_type:
- apiref
ms.openlocfilehash: 3740236cfe2bc7ecc6cd3bbeb3345c7510dd159f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99686942"
---
# <a name="icorprofilerinfo4enumjitedfunctions2-method"></a><span data-ttu-id="2135b-103">ICorProfilerInfo4::EnumJITedFunctions2 方法</span><span class="sxs-lookup"><span data-stu-id="2135b-103">ICorProfilerInfo4::EnumJITedFunctions2 Method</span></span>

<span data-ttu-id="2135b-104">返回之前 JIT 编译和 JIT 重新编译的所有函数的枚举器。</span><span class="sxs-lookup"><span data-stu-id="2135b-104">Returns an enumerator for all functions that were previously JIT-compiled and JIT-recompiled.</span></span> <span data-ttu-id="2135b-105">此方法将替换 [ICorProfilerInfo3：： EnumJITedFunctions](icorprofilerinfo3-enumjitedfunctions-method.md) 方法，该方法不枚举 JIT 重新编译的 id。</span><span class="sxs-lookup"><span data-stu-id="2135b-105">This method replaces the [ICorProfilerInfo3::EnumJITedFunctions](icorprofilerinfo3-enumjitedfunctions-method.md) method, which does not enumerate JIT-recompiled IDs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2135b-106">语法</span><span class="sxs-lookup"><span data-stu-id="2135b-106">Syntax</span></span>  
  
```cpp  
HRESULT EnumJITedFunctions([out] ICorProfilerFunctionEnum** ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2135b-107">参数</span><span class="sxs-lookup"><span data-stu-id="2135b-107">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="2135b-108">弄指向 [ICorProfilerFunctionEnum](icorprofilerfunctionenum-interface.md) 枚举器的指针。</span><span class="sxs-lookup"><span data-stu-id="2135b-108">[out] A pointer to the [ICorProfilerFunctionEnum](icorprofilerfunctionenum-interface.md) enumerator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2135b-109">备注</span><span class="sxs-lookup"><span data-stu-id="2135b-109">Remarks</span></span>  

 <span data-ttu-id="2135b-110">此方法可能与 `JITCompilation` 回调（如 [ICorProfilerCallback：： JITCompilationStarted](icorprofilercallback-jitcompilationstarted-method.md) 方法）重叠。</span><span class="sxs-lookup"><span data-stu-id="2135b-110">This method may overlap with `JITCompilation` callbacks such as the [ICorProfilerCallback::JITCompilationStarted](icorprofilercallback-jitcompilationstarted-method.md) method.</span></span> <span data-ttu-id="2135b-111">返回的枚举包含字段的值 `COR_PRF_FUNCTION::reJitId` 。</span><span class="sxs-lookup"><span data-stu-id="2135b-111">The returned enumeration includes values for the `COR_PRF_FUNCTION::reJitId` field.</span></span> <span data-ttu-id="2135b-112">此方法替换的 [ICorProfilerInfo3：： EnumJITedFunctions](icorprofilerinfo3-enumjitedfunctions-method.md) 方法不枚举 JIT 重新编译的 id，因为 `COR_PRF_FUNCTION::reJitId` 字段始终设置为0。</span><span class="sxs-lookup"><span data-stu-id="2135b-112">The [ICorProfilerInfo3::EnumJITedFunctions](icorprofilerinfo3-enumjitedfunctions-method.md) method, which this method replaces, does not enumerate JIT-recompiled IDs, because the `COR_PRF_FUNCTION::reJitId` field is always set to 0.</span></span> <span data-ttu-id="2135b-113">`ICorProfilerInfo4::EnumJITedFunctions`方法会枚举 JIT 重新编译的 id，因为 `COR_PRF_FUNCTION::reJitId` 字段设置正确。</span><span class="sxs-lookup"><span data-stu-id="2135b-113">The `ICorProfilerInfo4::EnumJITedFunctions` method does enumerate JIT-recompiled IDs, because the `COR_PRF_FUNCTION::reJitId` field is set properly.</span></span> <span data-ttu-id="2135b-114">请注意， [ICorProfilerInfo4：： EnumJITedFunctions2](icorprofilerinfo4-enumjitedfunctions2-method.md) 方法可以触发垃圾回收，而 [ICorProfilerInfo3：： EnumJITedFunctions 方法](icorprofilerinfo3-enumjitedfunctions-method.md) 将不会触发垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="2135b-114">Note that the [ICorProfilerInfo4::EnumJITedFunctions2](icorprofilerinfo4-enumjitedfunctions2-method.md) method can trigger a garbage collection, whereas [ICorProfilerInfo3::EnumJITedFunctions method](icorprofilerinfo3-enumjitedfunctions-method.md) will not.</span></span>  <span data-ttu-id="2135b-115">有关详细信息，请参阅 [CORPROF_E_UNSUPPORTED_CALL_SEQUENCE HRESULT](corprof-e-unsupported-call-sequence-hresult.md)。</span><span class="sxs-lookup"><span data-stu-id="2135b-115">For more information, see [CORPROF_E_UNSUPPORTED_CALL_SEQUENCE HRESULT](corprof-e-unsupported-call-sequence-hresult.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2135b-116">要求</span><span class="sxs-lookup"><span data-stu-id="2135b-116">Requirements</span></span>  

 <span data-ttu-id="2135b-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2135b-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2135b-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2135b-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2135b-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2135b-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2135b-120">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2135b-120">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2135b-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="2135b-121">See also</span></span>

- [<span data-ttu-id="2135b-122">EnumJITedFunctions 方法</span><span class="sxs-lookup"><span data-stu-id="2135b-122">EnumJITedFunctions Method</span></span>](icorprofilerinfo3-enumjitedfunctions-method.md)
- [<span data-ttu-id="2135b-123">ICorProfilerInfo4 接口</span><span class="sxs-lookup"><span data-stu-id="2135b-123">ICorProfilerInfo4 Interface</span></span>](icorprofilerinfo4-interface.md)
- [<span data-ttu-id="2135b-124">分析接口</span><span class="sxs-lookup"><span data-stu-id="2135b-124">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="2135b-125">分析</span><span class="sxs-lookup"><span data-stu-id="2135b-125">Profiling</span></span>](index.md)
