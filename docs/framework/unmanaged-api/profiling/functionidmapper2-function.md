---
description: 了解详细信息： FunctionIDMapper2 函数
title: FunctionIDMapper2 函数
ms.date: 03/30/2017
api_name:
- FunctionIDMapper2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionIDMapper2
helpviewer_keywords:
- FunctionIDMapper2 function [.NET Framework profiling]
ms.assetid: 466ad51b-8f0c-41d9-81f7-371aac3374cb
topic_type:
- apiref
ms.openlocfilehash: 1fd6680ffaa7b28e679dc3eaeb9840981ead5c45
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648566"
---
# <a name="functionidmapper2-function"></a><span data-ttu-id="b0a57-103">FunctionIDMapper2 函数</span><span class="sxs-lookup"><span data-stu-id="b0a57-103">FunctionIDMapper2 Function</span></span>

<span data-ttu-id="b0a57-104">通知探查器可能会将函数的给定标识符重新映射到备用 ID，该 ID 将在 [FunctionEnter3](functionenter3-function.md)、 [FunctionLeave3](functionleave3-function.md)和 [FunctionTailcall3](functiontailcall3-function.md)中使用，或者为该函数的[FunctionEnter3WithInfo](functionenter3withinfo-function.md)、 [FunctionLeave3WithInfo](functionleave3withinfo-function.md)和 [FunctionTailcall3WithInfo](functiontailcall3withinfo-function.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="b0a57-104">Notifies the profiler that the given identifier of a function may be remapped to an alternative ID to be used in the [FunctionEnter3](functionenter3-function.md), [FunctionLeave3](functionleave3-function.md), and [FunctionTailcall3](functiontailcall3-function.md), or[FunctionEnter3WithInfo](functionenter3withinfo-function.md), [FunctionLeave3WithInfo](functionleave3withinfo-function.md), and [FunctionTailcall3WithInfo](functiontailcall3withinfo-function.md) callbacks for that function.</span></span> <span data-ttu-id="b0a57-105">`FunctionIDMapper2` 此外还要使探查器指示它是否想要接收该函数的回调。</span><span class="sxs-lookup"><span data-stu-id="b0a57-105">`FunctionIDMapper2` also enables the profiler to indicate whether it wants to receive callbacks for that function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0a57-106">语法</span><span class="sxs-lookup"><span data-stu-id="b0a57-106">Syntax</span></span>  
  
```cpp  
UINT_PTR __stdcall FunctionIDMapper2 (  
    [in]  FunctionID  funcId,  
    [in]  void * clientData,  
    [out] BOOL       *pbHookFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b0a57-107">参数</span><span class="sxs-lookup"><span data-stu-id="b0a57-107">Parameters</span></span>

- `funcId`

  <span data-ttu-id="b0a57-108">\[in] 要重新映射的函数标识符。</span><span class="sxs-lookup"><span data-stu-id="b0a57-108">\[in] The function identifier to be remapped.</span></span>

- `clientData`

  <span data-ttu-id="b0a57-109">\[in] 一个指向用于消除运行时之间的歧义的数据的指针。</span><span class="sxs-lookup"><span data-stu-id="b0a57-109">\[in] A pointer to data that is used to disambiguate among runtimes.</span></span>

- `pbHookFunction`

  <span data-ttu-id="b0a57-110">\[out] 指向一个值的指针，探查器将其设置为 `true` （如果它要接收 `FunctionEnter3` 、 `FunctionLeave3` 、和）、、 `FunctionTailcall3` `FunctionEnter3WithInfo` `FunctionLeave3WithInfo` 和 `FunctionTailcall3WithInfo` 回调; 否则，它会将此值设置为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="b0a57-110">\[out] A pointer to a value that the profiler sets to `true` if it wants to receive `FunctionEnter3`, `FunctionLeave3`, and `FunctionTailcall3`, or `FunctionEnter3WithInfo`, `FunctionLeave3WithInfo`, and `FunctionTailcall3WithInfo` callbacks; otherwise, it sets this value to `false`.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0a57-111">返回值</span><span class="sxs-lookup"><span data-stu-id="b0a57-111">Return Value</span></span>  

 <span data-ttu-id="b0a57-112">探查器返回一个执行引擎用作替代函数标识符的值。</span><span class="sxs-lookup"><span data-stu-id="b0a57-112">The profiler returns a value that the execution engine uses as an alternative function identifier.</span></span> <span data-ttu-id="b0a57-113">返回值不能为 null，除非在 `pbHookFunction` 中返回 `false`。</span><span class="sxs-lookup"><span data-stu-id="b0a57-113">The return value cannot be null unless `false` is returned in `pbHookFunction`.</span></span> <span data-ttu-id="b0a57-114">否则为 null 的返回值将产生不可预知的结果，包括可能停止该过程。</span><span class="sxs-lookup"><span data-stu-id="b0a57-114">Otherwise, a null return value produces unpredictable results, including possibly halting the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b0a57-115">备注</span><span class="sxs-lookup"><span data-stu-id="b0a57-115">Remarks</span></span>  

 <span data-ttu-id="b0a57-116">此方法使用用于传递客户端数据的附加参数对 [FunctionIDMapper](functionidmapper-function.md) 函数进行扩展。</span><span class="sxs-lookup"><span data-stu-id="b0a57-116">This method extends the [FunctionIDMapper](functionidmapper-function.md) function with an additional parameter that is used to pass client data.</span></span> <span data-ttu-id="b0a57-117">客户端数据用于消除运行时之间的歧义。</span><span class="sxs-lookup"><span data-stu-id="b0a57-117">The client data is used to disambiguate among runtimes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b0a57-118">要求</span><span class="sxs-lookup"><span data-stu-id="b0a57-118">Requirements</span></span>  

 <span data-ttu-id="b0a57-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b0a57-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b0a57-120">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="b0a57-120">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="b0a57-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b0a57-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b0a57-122">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b0a57-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0a57-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="b0a57-123">See also</span></span>

- [<span data-ttu-id="b0a57-124">ICorProfilerInfo::SetFunctionIDMapper</span><span class="sxs-lookup"><span data-stu-id="b0a57-124">ICorProfilerInfo::SetFunctionIDMapper</span></span>](icorprofilerinfo-setfunctionidmapper-method.md)
- [<span data-ttu-id="b0a57-125">ICorProfilerInfo3::SetFunctionIDMapper2</span><span class="sxs-lookup"><span data-stu-id="b0a57-125">ICorProfilerInfo3::SetFunctionIDMapper2</span></span>](icorprofilerinfo3-setfunctionidmapper2-method.md)
- [<span data-ttu-id="b0a57-126">FunctionEnter3</span><span class="sxs-lookup"><span data-stu-id="b0a57-126">FunctionEnter3</span></span>](functionenter3-function.md)
- [<span data-ttu-id="b0a57-127">FunctionLeave3</span><span class="sxs-lookup"><span data-stu-id="b0a57-127">FunctionLeave3</span></span>](functionleave3-function.md)
- [<span data-ttu-id="b0a57-128">FunctionTailcall3</span><span class="sxs-lookup"><span data-stu-id="b0a57-128">FunctionTailcall3</span></span>](functiontailcall3-function.md)
- [<span data-ttu-id="b0a57-129">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="b0a57-129">FunctionEnter3WithInfo</span></span>](functionenter3withinfo-function.md)
- [<span data-ttu-id="b0a57-130">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="b0a57-130">FunctionLeave3WithInfo</span></span>](functionleave3withinfo-function.md)
- [<span data-ttu-id="b0a57-131">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="b0a57-131">FunctionTailcall3WithInfo</span></span>](functiontailcall3withinfo-function.md)
- [<span data-ttu-id="b0a57-132">分析全局静态函数</span><span class="sxs-lookup"><span data-stu-id="b0a57-132">Profiling Global Static Functions</span></span>](profiling-global-static-functions.md)
