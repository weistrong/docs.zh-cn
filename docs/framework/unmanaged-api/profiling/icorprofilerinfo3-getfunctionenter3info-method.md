---
description: 了解详细信息： ICorProfilerInfo3：： GetFunctionEnter3Info 方法
title: ICorProfilerInfo3::GetFunctionEnter3Info 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.GetFunctionEnter3Info Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::GetFunctionEnter3Info
helpviewer_keywords:
- GetFunctionEnter3Info method [.NET Framework profiling]
- ICorProfilerInfo3::GetFunctionEnter3Info method [.NET Framework profiling]
ms.assetid: 542c7c65-dd56-4651-b76f-5db2465e4a15
topic_type:
- apiref
ms.openlocfilehash: 3e6c0cfbf2518301e62ed5c57e956190066504ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646811"
---
# <a name="icorprofilerinfo3getfunctionenter3info-method"></a><span data-ttu-id="ad50d-103">ICorProfilerInfo3::GetFunctionEnter3Info 方法</span><span class="sxs-lookup"><span data-stu-id="ad50d-103">ICorProfilerInfo3::GetFunctionEnter3Info Method</span></span>

<span data-ttu-id="ad50d-104">提供由 [FunctionEnter3WithInfo](functionenter3withinfo-function.md) 函数向探查器报告的函数的堆栈帧和参数信息。</span><span class="sxs-lookup"><span data-stu-id="ad50d-104">Provides the stack frame and argument information of the function that is being reported to the profiler by the [FunctionEnter3WithInfo](functionenter3withinfo-function.md) function.</span></span> <span data-ttu-id="ad50d-105">仅在 `FunctionEnter3WithInfo` 回调时可调用此方法。</span><span class="sxs-lookup"><span data-stu-id="ad50d-105">This method can be called only during the `FunctionEnter3WithInfo` callback.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad50d-106">语法</span><span class="sxs-lookup"><span data-stu-id="ad50d-106">Syntax</span></span>  
  
```cpp  
HRESULT GetFunctionEnter3Info(  
            [in]  FunctionID functionId,
            [in]  COR_PRF_ELT_INFO eltInfo,  
            [out] COR_PRF_FRAME_INFO *pFrameInfo,  
            [in, out] ULONG *pcbArgumentInfo,  
            [out, size_is(*pcbArgumentInfo)]  
                  COR_PRF_FUNCTION_ARGUMENT_INFO *pArgumentInfo);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ad50d-107">参数</span><span class="sxs-lookup"><span data-stu-id="ad50d-107">Parameters</span></span>  

 `functionId`  
 <span data-ttu-id="ad50d-108">[in] 正在输入的函数的 `FunctionID`。</span><span class="sxs-lookup"><span data-stu-id="ad50d-108">[in] The `FunctionID` of the function that is being entered.</span></span>  
  
 `eltInfo`  
 <span data-ttu-id="ad50d-109">[in] 表示有关给定堆栈帧的信息的不透明的句柄。</span><span class="sxs-lookup"><span data-stu-id="ad50d-109">[in] An opaque handle that represents information about a given stack frame.</span></span> <span data-ttu-id="ad50d-110">探查器应提供与 `eltInfo` [FunctionEnter3WithInfo](functionenter3withinfo-function.md) 函数给定的相同的。</span><span class="sxs-lookup"><span data-stu-id="ad50d-110">The profiler should provide the same `eltInfo` that it was given by the [FunctionEnter3WithInfo](functionenter3withinfo-function.md) function.</span></span>  
  
 `pFrameInfo`  
 <span data-ttu-id="ad50d-111">[out] 表示有关给定堆栈帧的泛型信息的不透明的句柄。</span><span class="sxs-lookup"><span data-stu-id="ad50d-111">[out] An opaque handle that represents generics information about a given stack frame.</span></span> <span data-ttu-id="ad50d-112">此句柄仅在探查器调用 `GetFunctionEnter3Info` 方法的 `FunctionEnter3WithInfo` 回调时有效。</span><span class="sxs-lookup"><span data-stu-id="ad50d-112">This handle is valid only during the `FunctionEnter3WithInfo` callback in which the profiler called the `GetFunctionEnter3Info` method.</span></span>  
  
 `pcbArgumentInfo`  
 <span data-ttu-id="ad50d-113">[in，out]一个指针，指向 [COR_PRF_FUNCTION_ARGUMENT_INFO](cor-prf-function-argument-info-structure.md) 结构的总大小（以字节为单位） (加上) 指向的参数范围的任何附加 [COR_PRF_FUNCTION_ARGUMENT_RANGE](cor-prf-function-argument-range-structure.md) 结构 `pArgumentInfo` 。</span><span class="sxs-lookup"><span data-stu-id="ad50d-113">[in, out] A pointer to the total size, in bytes, of the [COR_PRF_FUNCTION_ARGUMENT_INFO](cor-prf-function-argument-info-structure.md) structure (plus any additional [COR_PRF_FUNCTION_ARGUMENT_RANGE](cor-prf-function-argument-range-structure.md) structures for the argument ranges pointed to by `pArgumentInfo`).</span></span> <span data-ttu-id="ad50d-114">如果指定的大小不足，将返回 ERROR_INSUFFICIENT_BUFFER，并将预期大小存储在 `pcbArgumentInfo` 中。</span><span class="sxs-lookup"><span data-stu-id="ad50d-114">If the specified size is not enough, ERROR_INSUFFICIENT_BUFFER is returned and the expected size is stored in `pcbArgumentInfo`.</span></span> <span data-ttu-id="ad50d-115">若仅为检索 `*pcbArgumentInfo` 的预期值而调用 `GetFunctionEnter3Info`，请设置 `*pcbArgumentInfo`=0 和 `pArgumentInfo`=NULL。</span><span class="sxs-lookup"><span data-stu-id="ad50d-115">To call `GetFunctionEnter3Info` just to retrieve the expected value for `*pcbArgumentInfo`, set `*pcbArgumentInfo`=0 and `pArgumentInfo`=NULL.</span></span>  
  
 `pArgumentInfo`  
 <span data-ttu-id="ad50d-116">弄指向 [COR_PRF_FUNCTION_ARGUMENT_INFO](cor-prf-function-argument-info-structure.md) 结构的指针，该结构以从左到右的顺序描述函数参数在内存中的位置。</span><span class="sxs-lookup"><span data-stu-id="ad50d-116">[out] A pointer to a [COR_PRF_FUNCTION_ARGUMENT_INFO](cor-prf-function-argument-info-structure.md) structure that describes the locations of the function's arguments in memory, in left-to-right order.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ad50d-117">备注</span><span class="sxs-lookup"><span data-stu-id="ad50d-117">Remarks</span></span>  

 <span data-ttu-id="ad50d-118">探查器必须为将进行检查的函数的 `COR_PRF_FUNCTION_ARGUMENT_INFO` 结构分配足够的空间，并且必须指示 `pcbArgumentInfo` 参数中的大小。</span><span class="sxs-lookup"><span data-stu-id="ad50d-118">The profiler must allocate sufficient space for the `COR_PRF_FUNCTION_ARGUMENT_INFO` structure of the function that is being inspected, and must indicate the size in the `pcbArgumentInfo` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ad50d-119">要求</span><span class="sxs-lookup"><span data-stu-id="ad50d-119">Requirements</span></span>  

 <span data-ttu-id="ad50d-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ad50d-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ad50d-121">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ad50d-121">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ad50d-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ad50d-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ad50d-123">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ad50d-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad50d-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="ad50d-124">See also</span></span>

- [<span data-ttu-id="ad50d-125">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="ad50d-125">FunctionEnter3WithInfo</span></span>](functionenter3withinfo-function.md)
- [<span data-ttu-id="ad50d-126">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="ad50d-126">FunctionLeave3WithInfo</span></span>](functionleave3withinfo-function.md)
- [<span data-ttu-id="ad50d-127">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="ad50d-127">FunctionTailcall3WithInfo</span></span>](functiontailcall3withinfo-function.md)
- [<span data-ttu-id="ad50d-128">ICorProfilerInfo3 接口</span><span class="sxs-lookup"><span data-stu-id="ad50d-128">ICorProfilerInfo3 Interface</span></span>](icorprofilerinfo3-interface.md)
- [<span data-ttu-id="ad50d-129">分析接口</span><span class="sxs-lookup"><span data-stu-id="ad50d-129">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="ad50d-130">分析</span><span class="sxs-lookup"><span data-stu-id="ad50d-130">Profiling</span></span>](index.md)
