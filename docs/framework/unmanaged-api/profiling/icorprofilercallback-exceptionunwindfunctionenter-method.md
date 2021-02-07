---
description: 了解详细信息： ICorProfilerCallback：： ExceptionUnwindFunctionEnter 方法
title: ICorProfilerCallback::ExceptionUnwindFunctionEnter 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionUnwindFunctionEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionUnwindFunctionEnter
helpviewer_keywords:
- ICorProfilerCallback::ExceptionUnwindFunctionEnter method [.NET Framework profiling]
- ExceptionUnwindFunctionEnter method [.NET Framework profiling]
ms.assetid: ea3dc625-5650-4bf4-8e67-01e42be065b1
topic_type:
- apiref
ms.openlocfilehash: 3f0376e01263290596aa722b37f6a796ab919139
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706014"
---
# <a name="icorprofilercallbackexceptionunwindfunctionenter-method"></a><span data-ttu-id="4bb80-103">ICorProfilerCallback::ExceptionUnwindFunctionEnter 方法</span><span class="sxs-lookup"><span data-stu-id="4bb80-103">ICorProfilerCallback::ExceptionUnwindFunctionEnter Method</span></span>

<span data-ttu-id="4bb80-104">通知探查器异常处理的展开阶段已开始展开某个函数。</span><span class="sxs-lookup"><span data-stu-id="4bb80-104">Notifies the profiler that the unwind phase of exception handling has begun to unwind a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4bb80-105">语法</span><span class="sxs-lookup"><span data-stu-id="4bb80-105">Syntax</span></span>  
  
```cpp  
HRESULT ExceptionUnwindFunctionEnter(  
    [in] FunctionID functionId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4bb80-106">参数</span><span class="sxs-lookup"><span data-stu-id="4bb80-106">Parameters</span></span>

- `functionId`

  <span data-ttu-id="4bb80-107">\[in] 要展开的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="4bb80-107">\[in] The ID of the function that is being unwound.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bb80-108">备注</span><span class="sxs-lookup"><span data-stu-id="4bb80-108">Remarks</span></span>  

 <span data-ttu-id="4bb80-109">探查器不应在此方法的实现中被阻止，因为堆栈可能不处于允许垃圾回收的状态，因此无法启用抢先垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="4bb80-109">The profiler should not block in its implementation of this method because the stack may not be in a state that allows garbage collection, and therefore preemptive garbage collection cannot be enabled.</span></span> <span data-ttu-id="4bb80-110">如果探查器在此处阻止并且试图进行垃圾回收，则运行时将被阻止，直到此回调返回。</span><span class="sxs-lookup"><span data-stu-id="4bb80-110">If the profiler blocks here and garbage collection is attempted, the runtime will block until this callback returns.</span></span>  
  
 <span data-ttu-id="4bb80-111">探查器的此方法的实现不应调入托管代码或以任何方式导致托管内存分配。</span><span class="sxs-lookup"><span data-stu-id="4bb80-111">The profiler's implementation of this method should not call into managed code or in any way cause a managed-memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4bb80-112">要求</span><span class="sxs-lookup"><span data-stu-id="4bb80-112">Requirements</span></span>  

 <span data-ttu-id="4bb80-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4bb80-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4bb80-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="4bb80-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="4bb80-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4bb80-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4bb80-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4bb80-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4bb80-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="4bb80-117">See also</span></span>

- [<span data-ttu-id="4bb80-118">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="4bb80-118">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="4bb80-119">ExceptionUnwindFunctionLeave 方法</span><span class="sxs-lookup"><span data-stu-id="4bb80-119">ExceptionUnwindFunctionLeave Method</span></span>](icorprofilercallback-exceptionunwindfunctionleave-method.md)
