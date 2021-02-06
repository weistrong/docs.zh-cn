---
description: 了解详细信息： ICorProfilerCallback：： ThreadDestroyed 方法
title: ICorProfilerCallback::ThreadDestroyed 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ThreadDestroyed
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ThreadDestroyed
helpviewer_keywords:
- ThreadDestroyed method [.NET Framework profiling]
- ICorProfilerCallback::ThreadDestroyed method [.NET Framework profiling]
ms.assetid: 4c2b66fd-0595-40a3-8931-f9c4fff97ac8
topic_type:
- apiref
ms.openlocfilehash: 63c8c4c523cb398bd7c766fc41bc669a2d74045e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657159"
---
# <a name="icorprofilercallbackthreaddestroyed-method"></a><span data-ttu-id="05707-103">ICorProfilerCallback::ThreadDestroyed 方法</span><span class="sxs-lookup"><span data-stu-id="05707-103">ICorProfilerCallback::ThreadDestroyed Method</span></span>

<span data-ttu-id="05707-104">通知探查器线程已销毁。</span><span class="sxs-lookup"><span data-stu-id="05707-104">Notifies the profiler that a thread has been destroyed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05707-105">语法</span><span class="sxs-lookup"><span data-stu-id="05707-105">Syntax</span></span>  
  
```cpp  
HRESULT ThreadDestroyed(  
    [in] ThreadID threadId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="05707-106">参数</span><span class="sxs-lookup"><span data-stu-id="05707-106">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="05707-107">中已销毁的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="05707-107">[in] The ID of the thread that has been destroyed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="05707-108">备注</span><span class="sxs-lookup"><span data-stu-id="05707-108">Remarks</span></span>  

 <span data-ttu-id="05707-109">`threadId`此调用时，该值不再有效。</span><span class="sxs-lookup"><span data-stu-id="05707-109">The `threadId` value is no longer valid at the time of this call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05707-110">要求</span><span class="sxs-lookup"><span data-stu-id="05707-110">Requirements</span></span>  

 <span data-ttu-id="05707-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="05707-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="05707-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="05707-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="05707-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="05707-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="05707-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="05707-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05707-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="05707-115">See also</span></span>

- [<span data-ttu-id="05707-116">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="05707-116">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="05707-117">ThreadCreated 方法</span><span class="sxs-lookup"><span data-stu-id="05707-117">ThreadCreated Method</span></span>](icorprofilercallback-threadcreated-method.md)
