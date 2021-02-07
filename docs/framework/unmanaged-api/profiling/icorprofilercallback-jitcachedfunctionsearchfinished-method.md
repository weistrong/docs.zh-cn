---
description: 了解详细信息： ICorProfilerCallback：： JITCachedFunctionSearchFinished 方法
title: ICorProfilerCallback::JITCachedFunctionSearchFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.JITCachedFunctionSearchFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::JITCachedFunctionSearchFinished
helpviewer_keywords:
- JITCachedFunctionSearchFinished method [.NET Framework profiling]
- ICorProfilerCallback::JITCachedFunctionSearchFinished method [.NET Framework profiling]
ms.assetid: 3c325c82-cddd-4b00-b3da-e450c36abf62
topic_type:
- apiref
ms.openlocfilehash: b5025a7d33800047bb6244b82308ba2ab158cea7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99705845"
---
# <a name="icorprofilercallbackjitcachedfunctionsearchfinished-method"></a><span data-ttu-id="8dffa-103">ICorProfilerCallback::JITCachedFunctionSearchFinished 方法</span><span class="sxs-lookup"><span data-stu-id="8dffa-103">ICorProfilerCallback::JITCachedFunctionSearchFinished Method</span></span>

<span data-ttu-id="8dffa-104">通知探查器搜索已完成先前使用本机映像生成器编译的函数 ( # A0) 。</span><span class="sxs-lookup"><span data-stu-id="8dffa-104">Notifies the profiler that a search has finished for a function that was compiled previously using the Native Image Generator (NGen.exe).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8dffa-105">语法</span><span class="sxs-lookup"><span data-stu-id="8dffa-105">Syntax</span></span>  
  
```cpp  
HRESULT JITCachedFunctionSearchFinished(  
    [in] FunctionID        functionId,  
    [in] COR_PRF_JIT_CACHE result);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8dffa-106">参数</span><span class="sxs-lookup"><span data-stu-id="8dffa-106">Parameters</span></span>

- `functionId`

  <span data-ttu-id="8dffa-107">\[in] 执行搜索的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="8dffa-107">\[in] The ID of the function for which the search was performed.</span></span>

- `result`

  <span data-ttu-id="8dffa-108">\[in] 指示搜索结果的 [COR_PRF_JIT_CACHE](cor-prf-jit-cache-enumeration.md) 枚举的值。</span><span class="sxs-lookup"><span data-stu-id="8dffa-108">\[in] A value of the [COR_PRF_JIT_CACHE](cor-prf-jit-cache-enumeration.md) enumeration that indicates the result of the search.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dffa-109">备注</span><span class="sxs-lookup"><span data-stu-id="8dffa-109">Remarks</span></span>  

 <span data-ttu-id="8dffa-110">在 .NET Framework 版本2.0 中，将不会对常规 NGen 映像中的所有函数执行 [ICorProfilerCallback：： JITCachedFunctionSearchStarted](icorprofilercallback-jitcachedfunctionsearchstarted-method.md) 和 `JITCachedFunctionSearchFinished` 回调。</span><span class="sxs-lookup"><span data-stu-id="8dffa-110">In the .NET Framework version 2.0, the [ICorProfilerCallback::JITCachedFunctionSearchStarted](icorprofilercallback-jitcachedfunctionsearchstarted-method.md) and `JITCachedFunctionSearchFinished` callbacks will not be made for all functions in regular NGen images.</span></span> <span data-ttu-id="8dffa-111">只有针对探查器优化的 NGen 映像将为映像中的所有函数生成回调。</span><span class="sxs-lookup"><span data-stu-id="8dffa-111">Only NGen images optimized for a profiler will generate callbacks for all functions in the image.</span></span> <span data-ttu-id="8dffa-112">但是，由于额外的开销，如果探查器打算使用这些回调来强制将函数实时编译 (JIT) ，则它应请求探查器优化的 NGen 映像。</span><span class="sxs-lookup"><span data-stu-id="8dffa-112">However, due to the additional overhead, a profiler should request profiler-optimized NGen images only if it intends to use these callbacks to force a function to be compiled just-in-time (JIT).</span></span> <span data-ttu-id="8dffa-113">否则，探查器应使用延迟策略来收集函数信息。</span><span class="sxs-lookup"><span data-stu-id="8dffa-113">Otherwise, the profiler should use a lazy strategy for gathering function information.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8dffa-114">要求</span><span class="sxs-lookup"><span data-stu-id="8dffa-114">Requirements</span></span>  

 <span data-ttu-id="8dffa-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8dffa-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8dffa-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8dffa-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8dffa-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8dffa-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8dffa-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8dffa-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8dffa-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="8dffa-119">See also</span></span>

- [<span data-ttu-id="8dffa-120">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="8dffa-120">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
