---
description: 了解详细信息： ICorProfilerInfo3：： GetFunctionTailcall3Info 方法
title: ICorProfilerInfo3::GetFunctionTailcall3Info 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.GetFunctionTailcall3Info Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::GetFunctionTailcall3Info
helpviewer_keywords:
- ICorProfilerInfo3::GetFunctionTailcall3Info method [.NET Framework profiling]
- GetFunctionTailcall3Info method [.NET Framework profiling]
ms.assetid: afdb5ac9-5bf5-4b91-b7cb-f81db23d7da3
topic_type:
- apiref
ms.openlocfilehash: a8976a11cf7a2c556afa62a559e3a294d81b9a1d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646791"
---
# <a name="icorprofilerinfo3getfunctiontailcall3info-method"></a><span data-ttu-id="8905c-103">ICorProfilerInfo3::GetFunctionTailcall3Info 方法</span><span class="sxs-lookup"><span data-stu-id="8905c-103">ICorProfilerInfo3::GetFunctionTailcall3Info Method</span></span>

<span data-ttu-id="8905c-104">提供由 [FunctionTailcall3WithInfo](functiontailcall3withinfo-function.md) 函数向探查器报告的函数的堆栈帧。</span><span class="sxs-lookup"><span data-stu-id="8905c-104">Provides the stack frame of the function that is being reported to the profiler by the [FunctionTailcall3WithInfo](functiontailcall3withinfo-function.md) function.</span></span> <span data-ttu-id="8905c-105">仅在 `FunctionTailcall3WithInfo` 回调时可调用此方法。</span><span class="sxs-lookup"><span data-stu-id="8905c-105">This method can be called only during the `FunctionTailcall3WithInfo` callback.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8905c-106">语法</span><span class="sxs-lookup"><span data-stu-id="8905c-106">Syntax</span></span>  
  
```cpp  
HRESULT GetFunctionTailcall3Info(
            [in]  FunctionID functionId,
            [in]  COR_PRF_ELT_INFO eltInfo,  
            [out] COR_PRF_FRAME_INFO *pFrameInfo);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8905c-107">参数</span><span class="sxs-lookup"><span data-stu-id="8905c-107">Parameters</span></span>  

 `functionId`  
 <span data-ttu-id="8905c-108">中 `FunctionID` 正在返回的函数的。</span><span class="sxs-lookup"><span data-stu-id="8905c-108">[in] The `FunctionID` of the function that is returning.</span></span>  
  
 `eltInfo`  
 <span data-ttu-id="8905c-109">[in] 表示有关给定堆栈帧的信息的不透明的句柄。</span><span class="sxs-lookup"><span data-stu-id="8905c-109">[in] An opaque handle that represents information about a given stack frame.</span></span> <span data-ttu-id="8905c-110">探查器应提供 `eltInfo` 由函数为探查器提供的相同的 `FunctionTailcall3WithInfo` 。</span><span class="sxs-lookup"><span data-stu-id="8905c-110">The profiler should provide the same `eltInfo` that was given to the profiler by the `FunctionTailcall3WithInfo` function.</span></span>  
  
 `pFrameInfo`  
 <span data-ttu-id="8905c-111">[out] 表示有关给定堆栈帧的泛型信息的不透明的句柄。</span><span class="sxs-lookup"><span data-stu-id="8905c-111">[out] An opaque handle that represents generics information about a given stack frame.</span></span> <span data-ttu-id="8905c-112">此句柄仅在探查器调用 `GetFunctionTailcall3Info` 方法的 `FunctionTailcall3WithInfo` 回调时有效。</span><span class="sxs-lookup"><span data-stu-id="8905c-112">This handle is valid only during the `FunctionTailcall3WithInfo` callback in which the profiler called the `GetFunctionTailcall3Info` method.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8905c-113">备注</span><span class="sxs-lookup"><span data-stu-id="8905c-113">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8905c-114">要求</span><span class="sxs-lookup"><span data-stu-id="8905c-114">Requirements</span></span>  

 <span data-ttu-id="8905c-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8905c-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8905c-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8905c-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8905c-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8905c-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8905c-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8905c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8905c-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="8905c-119">See also</span></span>

- [<span data-ttu-id="8905c-120">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="8905c-120">FunctionEnter3WithInfo</span></span>](functionenter3withinfo-function.md)
- [<span data-ttu-id="8905c-121">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="8905c-121">FunctionLeave3WithInfo</span></span>](functionleave3withinfo-function.md)
- [<span data-ttu-id="8905c-122">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="8905c-122">FunctionTailcall3WithInfo</span></span>](functiontailcall3withinfo-function.md)
- [<span data-ttu-id="8905c-123">ICorProfilerInfo3 接口</span><span class="sxs-lookup"><span data-stu-id="8905c-123">ICorProfilerInfo3 Interface</span></span>](icorprofilerinfo3-interface.md)
- [<span data-ttu-id="8905c-124">分析接口</span><span class="sxs-lookup"><span data-stu-id="8905c-124">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="8905c-125">分析</span><span class="sxs-lookup"><span data-stu-id="8905c-125">Profiling</span></span>](index.md)
