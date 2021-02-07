---
description: 了解详细信息： ICorProfilerCallback：： ExceptionSearchFunctionLeave 方法
title: ICorProfilerCallback::ExceptionSearchFunctionLeave 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionSearchFunctionLeave
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionSearchFunctionLeave
helpviewer_keywords:
- ExceptionSearchFunctionLeave method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionSearchFunctionLeave method [.NET Framework profiling]
ms.assetid: 01de7ac6-0aad-42ef-bf93-50737667b0a4
topic_type:
- apiref
ms.openlocfilehash: 1a30d7ef979f751596cdd723b76eefee3cc1db5a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706144"
---
# <a name="icorprofilercallbackexceptionsearchfunctionleave-method"></a><span data-ttu-id="d976f-103">ICorProfilerCallback::ExceptionSearchFunctionLeave 方法</span><span class="sxs-lookup"><span data-stu-id="d976f-103">ICorProfilerCallback::ExceptionSearchFunctionLeave Method</span></span>

<span data-ttu-id="d976f-104">通知探查器异常处理的搜索阶段已经完成了对函数的搜索。</span><span class="sxs-lookup"><span data-stu-id="d976f-104">Notifies the profiler that the search phase of exception handling has finished searching a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d976f-105">语法</span><span class="sxs-lookup"><span data-stu-id="d976f-105">Syntax</span></span>  
  
```cpp  
HRESULT ExceptionSearchFunctionLeave();  
```  
  
## <a name="requirements"></a><span data-ttu-id="d976f-106">要求</span><span class="sxs-lookup"><span data-stu-id="d976f-106">Requirements</span></span>  

 <span data-ttu-id="d976f-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d976f-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d976f-108">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d976f-108">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d976f-109">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d976f-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d976f-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d976f-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d976f-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="d976f-111">See also</span></span>

- [<span data-ttu-id="d976f-112">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="d976f-112">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="d976f-113">ExceptionSearchFunctionEnter 方法</span><span class="sxs-lookup"><span data-stu-id="d976f-113">ExceptionSearchFunctionEnter Method</span></span>](icorprofilercallback-exceptionsearchfunctionenter-method.md)
