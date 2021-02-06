---
description: 了解详细信息： ICorProfilerCallback：： RuntimeThreadResumed 方法
title: ICorProfilerCallback::RuntimeThreadResumed 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RuntimeThreadResumed
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeThreadResumed
helpviewer_keywords:
- ICorProfilerCallback::RuntimeThreadResumed method [.NET Framework profiling]
- RuntimeThreadResumed method [.NET Framework profiling]
ms.assetid: da984f89-4f53-4ab0-ae6f-3e2ee6085994
topic_type:
- apiref
ms.openlocfilehash: a01be057bb442c69890d3b1cb4ebe1f861d2518c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657341"
---
# <a name="icorprofilercallbackruntimethreadresumed-method"></a><span data-ttu-id="5b6b9-103">ICorProfilerCallback::RuntimeThreadResumed 方法</span><span class="sxs-lookup"><span data-stu-id="5b6b9-103">ICorProfilerCallback::RuntimeThreadResumed Method</span></span>

<span data-ttu-id="5b6b9-104">通知探查器指定的线程在挂起后已恢复。</span><span class="sxs-lookup"><span data-stu-id="5b6b9-104">Notifies the profiler that the specified thread has resumed after being suspended.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5b6b9-105">语法</span><span class="sxs-lookup"><span data-stu-id="5b6b9-105">Syntax</span></span>  
  
```cpp  
HRESULT RuntimeThreadResumed(  
    [in] ThreadID threadId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5b6b9-106">参数</span><span class="sxs-lookup"><span data-stu-id="5b6b9-106">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="5b6b9-107">中已恢复的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="5b6b9-107">[in] The ID of the thread that has been resumed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5b6b9-108">要求</span><span class="sxs-lookup"><span data-stu-id="5b6b9-108">Requirements</span></span>  

 <span data-ttu-id="5b6b9-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5b6b9-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5b6b9-110">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5b6b9-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5b6b9-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5b6b9-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5b6b9-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5b6b9-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5b6b9-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="5b6b9-113">See also</span></span>

- [<span data-ttu-id="5b6b9-114">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="5b6b9-114">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="5b6b9-115">RuntimeThreadSuspended 方法</span><span class="sxs-lookup"><span data-stu-id="5b6b9-115">RuntimeThreadSuspended Method</span></span>](icorprofilercallback-runtimethreadsuspended-method.md)
