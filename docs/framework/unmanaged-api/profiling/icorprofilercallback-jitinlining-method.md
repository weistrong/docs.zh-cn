---
description: 了解详细信息： ICorProfilerCallback：： JITInlining 方法
title: ICorProfilerCallback::JITInlining 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.JITInlining
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::JITInlining
helpviewer_keywords:
- JITInlining method [.NET Framework profiling]
- ICorProfilerCallback::JITInlining method [.NET Framework profiling]
ms.assetid: c2f45801-dd38-4b78-b6b7-64397dc73f83
topic_type:
- apiref
ms.openlocfilehash: 2bd6c48180b9484ef90b6afb505c8171aff57aa4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99705624"
---
# <a name="icorprofilercallbackjitinlining-method"></a><span data-ttu-id="b8741-103">ICorProfilerCallback::JITInlining 方法</span><span class="sxs-lookup"><span data-stu-id="b8741-103">ICorProfilerCallback::JITInlining Method</span></span>

<span data-ttu-id="b8741-104">通知探查器，实时 (JIT) 编译器将与另一个函数插入一个函数。</span><span class="sxs-lookup"><span data-stu-id="b8741-104">Notifies the profiler that the just-in-time (JIT) compiler is about to insert a function in line with another function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8741-105">语法</span><span class="sxs-lookup"><span data-stu-id="b8741-105">Syntax</span></span>  
  
```cpp  
HRESULT JITInlining(  
    [in]  FunctionID callerId,  
    [in]  FunctionID calleeId,  
    [out] BOOL      *pfShouldInline);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b8741-106">参数</span><span class="sxs-lookup"><span data-stu-id="b8741-106">Parameters</span></span>  

 `callerId`  
 <span data-ttu-id="b8741-107">中将向其中插入函数的函数的 ID `calleeId` 。</span><span class="sxs-lookup"><span data-stu-id="b8741-107">[in] The ID of the function into which the `calleeId` function will be inserted.</span></span>  
  
 `calleeId`  
 <span data-ttu-id="b8741-108">中要插入的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="b8741-108">[in] The ID of the function to be inserted.</span></span>  
  
 `pfShouldInline`  
 <span data-ttu-id="b8741-109">[out] `true` 如果允许执行插入，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="b8741-109">[out] `true` to allow the insertion to occur; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b8741-110">备注</span><span class="sxs-lookup"><span data-stu-id="b8741-110">Remarks</span></span>  

 <span data-ttu-id="b8741-111">探查器可以将设置 `pfShouldInline` 为 `false` ，以防止将 `calleeId` 函数插入 `callerId` 函数。</span><span class="sxs-lookup"><span data-stu-id="b8741-111">The profiler can set `pfShouldInline` to `false` to prevent the `calleeId` function from being inserted into the `callerId` function.</span></span> <span data-ttu-id="b8741-112">此外，探查器可以通过使用 [COR_PRF_MONITOR](cor-prf-monitor-enumeration.md) 枚举的 COR_PRF_DISABLE_INLINING 值全局禁用内联插入。</span><span class="sxs-lookup"><span data-stu-id="b8741-112">Also, the profiler can globally disable inline insertion by using the COR_PRF_DISABLE_INLINING value of the [COR_PRF_MONITOR](cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
 <span data-ttu-id="b8741-113">以内联方式插入的函数不会引发用于进入或离开的事件。</span><span class="sxs-lookup"><span data-stu-id="b8741-113">Functions inserted inline do not raise events for entering or leaving.</span></span> <span data-ttu-id="b8741-114">因此，探查器必须设置 `pfShouldInline` 为才能 `false` 生成准确的调用图。</span><span class="sxs-lookup"><span data-stu-id="b8741-114">Therefore, the profiler must set `pfShouldInline` to `false` in order to produce an accurate callgraph.</span></span> <span data-ttu-id="b8741-115">设置 `pfShouldInline` 为 `false` 会影响性能，因为内联插入通常会提高速度，并减少插入方法的单独 JIT 编译事件数。</span><span class="sxs-lookup"><span data-stu-id="b8741-115">Setting `pfShouldInline` to `false` will affect performance, because inline insertion typically increases speed and reduces the number of separate JIT compilation events for the inserted method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b8741-116">要求</span><span class="sxs-lookup"><span data-stu-id="b8741-116">Requirements</span></span>  

 <span data-ttu-id="b8741-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b8741-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b8741-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b8741-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b8741-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b8741-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b8741-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b8741-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8741-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="b8741-121">See also</span></span>

- [<span data-ttu-id="b8741-122">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="b8741-122">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
