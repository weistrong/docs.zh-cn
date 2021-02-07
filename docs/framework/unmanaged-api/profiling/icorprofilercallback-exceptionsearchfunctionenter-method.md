---
description: 了解详细信息： ICorProfilerCallback：： ExceptionSearchFunctionEnter 方法
title: ICorProfilerCallback::ExceptionSearchFunctionEnter 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionSearchFunctionEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionSearchFunctionEnter
helpviewer_keywords:
- ExceptionSearchFunctionEnter method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionSearchFunctionEnter method [.NET Framework profiling]
ms.assetid: bfd54573-b7e6-4bd1-a184-7f08a8b39fae
topic_type:
- apiref
ms.openlocfilehash: 6e77ab5dc8c15a1d0785fb83310183c0a4693225
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706183"
---
# <a name="icorprofilercallbackexceptionsearchfunctionenter-method"></a><span data-ttu-id="2d854-103">ICorProfilerCallback::ExceptionSearchFunctionEnter 方法</span><span class="sxs-lookup"><span data-stu-id="2d854-103">ICorProfilerCallback::ExceptionSearchFunctionEnter Method</span></span>

<span data-ttu-id="2d854-104">通知探查器，异常处理的搜索阶段已开始搜索函数以查找当前异常的处理程序。</span><span class="sxs-lookup"><span data-stu-id="2d854-104">Notifies the profiler that the search phase of exception handling has begun searching a function to find a handler for the current exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d854-105">语法</span><span class="sxs-lookup"><span data-stu-id="2d854-105">Syntax</span></span>  
  
```cpp  
HRESULT ExceptionSearchFunctionEnter(  
    [in] FunctionID functionId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2d854-106">参数</span><span class="sxs-lookup"><span data-stu-id="2d854-106">Parameters</span></span>

- `functionId`

  <span data-ttu-id="2d854-107">\[in] 已输入的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="2d854-107">\[in] The ID of the function that has been entered.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="2d854-108">要求</span><span class="sxs-lookup"><span data-stu-id="2d854-108">Requirements</span></span>  

 <span data-ttu-id="2d854-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2d854-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d854-110">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2d854-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2d854-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2d854-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2d854-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d854-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d854-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="2d854-113">See also</span></span>

- [<span data-ttu-id="2d854-114">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="2d854-114">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="2d854-115">ExceptionSearchFunctionLeave 方法</span><span class="sxs-lookup"><span data-stu-id="2d854-115">ExceptionSearchFunctionLeave Method</span></span>](icorprofilercallback-exceptionsearchfunctionleave-method.md)
