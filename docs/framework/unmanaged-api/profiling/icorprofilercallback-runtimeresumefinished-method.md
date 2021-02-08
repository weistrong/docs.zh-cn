---
description: 了解详细信息： ICorProfilerCallback：： RuntimeResumeFinished 方法
title: ICorProfilerCallback::RuntimeResumeFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RuntimeResumeFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeResumeFinished
helpviewer_keywords:
- RuntimeResumeFinished method [.NET Framework profiling]
- ICorProfilerCallback::RuntimeResumeFinished method [.NET Framework profiling]
ms.assetid: 76de0494-dc49-426b-887d-bee98806a982
topic_type:
- apiref
ms.openlocfilehash: a8a38ff8372df9890239966c90175d72bda4b09d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788847"
---
# <a name="icorprofilercallbackruntimeresumefinished-method"></a><span data-ttu-id="fa1b2-103">ICorProfilerCallback::RuntimeResumeFinished 方法</span><span class="sxs-lookup"><span data-stu-id="fa1b2-103">ICorProfilerCallback::RuntimeResumeFinished Method</span></span>

<span data-ttu-id="fa1b2-104">通知探查器运行时已恢复所有运行时线程并返回到正常操作。</span><span class="sxs-lookup"><span data-stu-id="fa1b2-104">Notifies the profiler that the runtime has resumed all runtime threads and has returned to normal operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa1b2-105">语法</span><span class="sxs-lookup"><span data-stu-id="fa1b2-105">Syntax</span></span>  
  
```cpp  
HRESULT RuntimeResumeFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="fa1b2-106">备注</span><span class="sxs-lookup"><span data-stu-id="fa1b2-106">Remarks</span></span>  

 <span data-ttu-id="fa1b2-107">`RuntimeResumeFinished`不保证回调与[ICorProfilerCallback：： RuntimeSuspendStarted](icorprofilercallback-runtimesuspendstarted-method.md)回调在同一线程上发生。</span><span class="sxs-lookup"><span data-stu-id="fa1b2-107">The `RuntimeResumeFinished` callback is not guaranteed to occur on the same thread as the [ICorProfilerCallback::RuntimeSuspendStarted](icorprofilercallback-runtimesuspendstarted-method.md) callback.</span></span> <span data-ttu-id="fa1b2-108">但是，它可以保证在与 [ICorProfilerCallback：： RuntimeResumeStarted](icorprofilercallback-runtimeresumestarted-method.md) 回调相同的线程上发生。</span><span class="sxs-lookup"><span data-stu-id="fa1b2-108">However, it is guaranteed to occur on the same thread as the [ICorProfilerCallback::RuntimeResumeStarted](icorprofilercallback-runtimeresumestarted-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fa1b2-109">要求</span><span class="sxs-lookup"><span data-stu-id="fa1b2-109">Requirements</span></span>  

 <span data-ttu-id="fa1b2-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fa1b2-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa1b2-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fa1b2-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fa1b2-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fa1b2-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fa1b2-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa1b2-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa1b2-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="fa1b2-114">See also</span></span>

- [<span data-ttu-id="fa1b2-115">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="fa1b2-115">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
