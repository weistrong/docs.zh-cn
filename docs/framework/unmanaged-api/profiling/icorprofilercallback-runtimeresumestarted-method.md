---
description: 了解详细信息： ICorProfilerCallback：： RuntimeResumeStarted 方法
title: ICorProfilerCallback::RuntimeResumeStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RuntimeResumeStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeResumeStarted
helpviewer_keywords:
- ICorProfilerCallback::RuntimeResumeStarted method [.NET Framework profiling]
- RuntimeResumeStarted method [.NET Framework profiling]
ms.assetid: 5854bfb2-c568-4f19-904a-7c9d41e7b995
topic_type:
- apiref
ms.openlocfilehash: 74e87906b4c429d795aa3074b25f4ac7a9edfa37
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788834"
---
# <a name="icorprofilercallbackruntimeresumestarted-method"></a><span data-ttu-id="bb59c-103">ICorProfilerCallback::RuntimeResumeStarted 方法</span><span class="sxs-lookup"><span data-stu-id="bb59c-103">ICorProfilerCallback::RuntimeResumeStarted Method</span></span>

<span data-ttu-id="bb59c-104">通知探查器运行时正在恢复所有运行时线程。</span><span class="sxs-lookup"><span data-stu-id="bb59c-104">Notifies the profiler that the runtime is resuming all run-time threads.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb59c-105">语法</span><span class="sxs-lookup"><span data-stu-id="bb59c-105">Syntax</span></span>  
  
```cpp  
HRESULT RuntimeResumeStarted();  
```  
  
## <a name="requirements"></a><span data-ttu-id="bb59c-106">要求</span><span class="sxs-lookup"><span data-stu-id="bb59c-106">Requirements</span></span>  

 <span data-ttu-id="bb59c-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bb59c-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb59c-108">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="bb59c-108">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="bb59c-109">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bb59c-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bb59c-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bb59c-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb59c-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="bb59c-111">See also</span></span>

- [<span data-ttu-id="bb59c-112">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="bb59c-112">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="bb59c-113">RuntimeResumeFinished 方法</span><span class="sxs-lookup"><span data-stu-id="bb59c-113">RuntimeResumeFinished Method</span></span>](icorprofilercallback-runtimeresumefinished-method.md)
