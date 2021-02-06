---
description: 了解详细信息： ICorProfilerInfo3：： GetFunctionLeave3Info 方法
title: ICorProfilerInfo3::GetFunctionLeave3Info 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.GetFunctionLeave3Info Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::GetFunctionLeave3Info
helpviewer_keywords:
- GetFunctionLeave3Info method [.NET Framework profiling]
- ICorProfilerInfo3::GetFunctionLeave3Info method [.NET Framework profiling]
ms.assetid: df7083d2-fd43-44c7-9ce5-912c25cef0ff
topic_type:
- apiref
ms.openlocfilehash: 3031190a3603bedb3f58e7a86747542831c72291
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646785"
---
# <a name="icorprofilerinfo3getfunctionleave3info-method"></a><span data-ttu-id="fcea2-103">ICorProfilerInfo3::GetFunctionLeave3Info 方法</span><span class="sxs-lookup"><span data-stu-id="fcea2-103">ICorProfilerInfo3::GetFunctionLeave3Info Method</span></span>

<span data-ttu-id="fcea2-104">提供由 [FunctionLeave3WithInfo 函数](functionleave3withinfo-function.md) 函数向探查器报告的函数的堆栈帧和返回值。</span><span class="sxs-lookup"><span data-stu-id="fcea2-104">Provides the stack frame and return value of the function that is being reported to the profiler by the [FunctionLeave3WithInfo function](functionleave3withinfo-function.md) function.</span></span> <span data-ttu-id="fcea2-105">仅在 `FunctionLeave3WithInfo` 回调时可调用此方法。</span><span class="sxs-lookup"><span data-stu-id="fcea2-105">This method can be called only during the `FunctionLeave3WithInfo` callback.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fcea2-106">语法</span><span class="sxs-lookup"><span data-stu-id="fcea2-106">Syntax</span></span>  
  
```cpp  
HRESULT GetFunctionLeave3Info(  
            [in]  FunctionID functionId,  
            [in]  COR_PRF_ELT_INFO eltInfo,  
            [out] COR_PRF_FRAME_INFO *pFrameInfo,  
            [out] COR_PRF_FUNCTION_ARGUMENT_RANGE *pRetvalRange);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fcea2-107">参数</span><span class="sxs-lookup"><span data-stu-id="fcea2-107">Parameters</span></span>  

 `functionId`  
 <span data-ttu-id="fcea2-108">中 `FunctionID` 正在返回的函数的。</span><span class="sxs-lookup"><span data-stu-id="fcea2-108">[in] The `FunctionID` of the function that is returning.</span></span>  
  
 `eltInfo`  
 <span data-ttu-id="fcea2-109">[in] 表示有关给定堆栈帧的信息的不透明的句柄。</span><span class="sxs-lookup"><span data-stu-id="fcea2-109">[in] An opaque handle that represents information about a given stack frame.</span></span> <span data-ttu-id="fcea2-110">探查器应提供 `eltInfo` [FunctionLeave3WithInfo](functionleave3withinfo-function.md) 函数为探查器提供的相同的。</span><span class="sxs-lookup"><span data-stu-id="fcea2-110">The profiler should provide the same `eltInfo` that was given to the profiler by the [FunctionLeave3WithInfo](functionleave3withinfo-function.md) function.</span></span>  
  
 `pFrameInfo`  
 <span data-ttu-id="fcea2-111">[out] 表示有关给定堆栈帧的泛型信息的不透明的句柄。</span><span class="sxs-lookup"><span data-stu-id="fcea2-111">[out] An opaque handle that represents generics information about a given stack frame.</span></span> <span data-ttu-id="fcea2-112">此句柄仅在探查器调用 `GetFunctionLeave3Info` 方法的 `FunctionLeave3WithInfo` 回调时有效。</span><span class="sxs-lookup"><span data-stu-id="fcea2-112">This handle is valid only during the `FunctionLeave3WithInfo` callback in which the profiler called the `GetFunctionLeave3Info` method.</span></span>  
  
 `pRetvalRange`  
 <span data-ttu-id="fcea2-113">弄指向 [COR_PRF_FUNCTION_ARGUMENT_RANGE](cor-prf-function-argument-range-structure.md) 结构的指针，该结构包含从函数返回的值。</span><span class="sxs-lookup"><span data-stu-id="fcea2-113">[out] A pointer to a [COR_PRF_FUNCTION_ARGUMENT_RANGE](cor-prf-function-argument-range-structure.md) structure that contains the value that is returned from the function.</span></span> <span data-ttu-id="fcea2-114">若要访问返回值信息， `COR_PRF_ENABLE_FUNCTION_RETVAL` 必须设置标志。</span><span class="sxs-lookup"><span data-stu-id="fcea2-114">To access return value information, the `COR_PRF_ENABLE_FUNCTION_RETVAL` flag must be set.</span></span> <span data-ttu-id="fcea2-115">探查器可以使用 [ICorProfilerInfo：： SetEventMask 方法](icorprofilerinfo-seteventmask-method.md) 来设置事件标志。</span><span class="sxs-lookup"><span data-stu-id="fcea2-115">The profiler can use the [ICorProfilerInfo::SetEventMask method](icorprofilerinfo-seteventmask-method.md) to set the event flags.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fcea2-116">备注</span><span class="sxs-lookup"><span data-stu-id="fcea2-116">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fcea2-117">要求</span><span class="sxs-lookup"><span data-stu-id="fcea2-117">Requirements</span></span>  

 <span data-ttu-id="fcea2-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fcea2-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fcea2-119">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fcea2-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fcea2-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fcea2-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fcea2-121">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fcea2-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fcea2-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="fcea2-122">See also</span></span>

- [<span data-ttu-id="fcea2-123">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="fcea2-123">FunctionEnter3WithInfo</span></span>](functionenter3withinfo-function.md)
- [<span data-ttu-id="fcea2-124">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="fcea2-124">FunctionLeave3WithInfo</span></span>](functionleave3withinfo-function.md)
- [<span data-ttu-id="fcea2-125">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="fcea2-125">FunctionTailcall3WithInfo</span></span>](functiontailcall3withinfo-function.md)
- [<span data-ttu-id="fcea2-126">ICorProfilerInfo3 接口</span><span class="sxs-lookup"><span data-stu-id="fcea2-126">ICorProfilerInfo3 Interface</span></span>](icorprofilerinfo3-interface.md)
- [<span data-ttu-id="fcea2-127">分析接口</span><span class="sxs-lookup"><span data-stu-id="fcea2-127">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="fcea2-128">分析</span><span class="sxs-lookup"><span data-stu-id="fcea2-128">Profiling</span></span>](index.md)
