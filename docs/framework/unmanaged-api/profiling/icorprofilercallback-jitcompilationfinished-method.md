---
description: 了解详细信息： ICorProfilerCallback：： JITCompilationFinished 方法
title: ICorProfilerCallback::JITCompilationFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.JITCompilationFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::JITCompilationFinished
helpviewer_keywords:
- JITCompilationFinished method [.NET Framework profiling]
- ICorProfilerCallback::JITCompilationFinished method [.NET Framework profiling]
ms.assetid: 8dcd7537-d0c6-498c-8a56-2c060310ef65
topic_type:
- apiref
ms.openlocfilehash: f0308bfb5f81d7305ab36acbb9144142232ef8c4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99705780"
---
# <a name="icorprofilercallbackjitcompilationfinished-method"></a><span data-ttu-id="bcf72-103">ICorProfilerCallback::JITCompilationFinished 方法</span><span class="sxs-lookup"><span data-stu-id="bcf72-103">ICorProfilerCallback::JITCompilationFinished Method</span></span>

<span data-ttu-id="bcf72-104">通知探查器实时 (JIT) 编译器已经完成了对函数的编译。</span><span class="sxs-lookup"><span data-stu-id="bcf72-104">Notifies the profiler that the just-in-time (JIT) compiler has finished compiling a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bcf72-105">语法</span><span class="sxs-lookup"><span data-stu-id="bcf72-105">Syntax</span></span>  
  
```cpp  
HRESULT JITCompilationFinished(  
    [in] FunctionID functionId,  
    [in] HRESULT    hrStatus,  
    [in] BOOL       fIsSafeToBlock);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bcf72-106">参数</span><span class="sxs-lookup"><span data-stu-id="bcf72-106">Parameters</span></span>

- `functionId`

  <span data-ttu-id="bcf72-107">\[in] 编译的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="bcf72-107">\[in] The ID of the function that was compiled.</span></span>

- `hrStatus`

  <span data-ttu-id="bcf72-108">\[in] 一个值，该值指示编译是否成功。</span><span class="sxs-lookup"><span data-stu-id="bcf72-108">\[in] A value indicating whether compilation was successful.</span></span>

- `fIsSafeToBlock`

  <span data-ttu-id="bcf72-109">\[in] 一个值，该值指示探查器是否会影响运行时的操作。</span><span class="sxs-lookup"><span data-stu-id="bcf72-109">\[in] A value indicating to the profiler whether blocking will affect the operation of the runtime.</span></span> <span data-ttu-id="bcf72-110">`true`如果阻止可能会导致运行时等待调用线程从此回调返回，则该值为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="bcf72-110">The value is `true` if blocking may cause the runtime to wait for the calling thread to return from this callback; otherwise, `false`.</span></span>

  <span data-ttu-id="bcf72-111">尽管的值 `true` 不会损害运行时，但它可能会使分析结果变形。</span><span class="sxs-lookup"><span data-stu-id="bcf72-111">Although a value of `true` will not harm the runtime, it can skew the profiling results.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf72-112">要求</span><span class="sxs-lookup"><span data-stu-id="bcf72-112">Requirements</span></span>  

 <span data-ttu-id="bcf72-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bcf72-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bcf72-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="bcf72-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="bcf72-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bcf72-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bcf72-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bcf72-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bcf72-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="bcf72-117">See also</span></span>

- [<span data-ttu-id="bcf72-118">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="bcf72-118">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="bcf72-119">JITCompilationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="bcf72-119">JITCompilationStarted Method</span></span>](icorprofilercallback-jitcompilationstarted-method.md)
