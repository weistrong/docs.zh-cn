---
description: 了解详细信息： ICorProfilerCallback：： ExceptionSearchCatcherFound 方法
title: ICorProfilerCallback::ExceptionSearchCatcherFound 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionSearchCatcherFound
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionSearchCatcherFound
helpviewer_keywords:
- ExceptionSearchCatcherFound method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionSearchCatcherFound method [.NET Framework profiling]
ms.assetid: 190f424d-5e37-4163-a191-0895686e9476
topic_type:
- apiref
ms.openlocfilehash: b222e629cbfce2fde27c2d266b3a343466a1419c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706313"
---
# <a name="icorprofilercallbackexceptionsearchcatcherfound-method"></a><span data-ttu-id="58083-103">ICorProfilerCallback::ExceptionSearchCatcherFound 方法</span><span class="sxs-lookup"><span data-stu-id="58083-103">ICorProfilerCallback::ExceptionSearchCatcherFound Method</span></span>

<span data-ttu-id="58083-104">通知探查器，异常处理的搜索阶段已找到引发的异常的处理程序。</span><span class="sxs-lookup"><span data-stu-id="58083-104">Notifies the profiler that the search phase of exception handling has located a handler for the exception that was thrown.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58083-105">语法</span><span class="sxs-lookup"><span data-stu-id="58083-105">Syntax</span></span>  
  
```cpp  
RESULT ExceptionSearchCatcherFound(  
    [in] FunctionID functionId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="58083-106">参数</span><span class="sxs-lookup"><span data-stu-id="58083-106">Parameters</span></span>

- `functionId`

  <span data-ttu-id="58083-107">\[in] 包含异常处理程序的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="58083-107">\[in] The ID of the function that contains the exception handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="58083-108">要求</span><span class="sxs-lookup"><span data-stu-id="58083-108">Requirements</span></span>  

 <span data-ttu-id="58083-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="58083-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58083-110">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="58083-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="58083-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="58083-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="58083-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58083-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58083-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="58083-113">See also</span></span>

- [<span data-ttu-id="58083-114">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="58083-114">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
