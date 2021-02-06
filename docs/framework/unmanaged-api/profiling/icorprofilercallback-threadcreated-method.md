---
description: 了解详细信息： ICorProfilerCallback：： ThreadCreated 方法
title: ICorProfilerCallback::ThreadCreated 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ThreadCreated
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ThreadCreated
helpviewer_keywords:
- ICorProfilerCallback::ThreadCreated method [.NET Framework profiling]
- ThreadCreated method [.NET Framework profiling]
ms.assetid: cca0f799-09b8-4689-a33c-6d6537943a9b
topic_type:
- apiref
ms.openlocfilehash: 8b6208856b78298f643161cd6bb78773ac86bc3b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657195"
---
# <a name="icorprofilercallbackthreadcreated-method"></a><span data-ttu-id="75bcc-103">ICorProfilerCallback::ThreadCreated 方法</span><span class="sxs-lookup"><span data-stu-id="75bcc-103">ICorProfilerCallback::ThreadCreated Method</span></span>

<span data-ttu-id="75bcc-104">通知探查器已创建一个线程。</span><span class="sxs-lookup"><span data-stu-id="75bcc-104">Notifies the profiler that a thread has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="75bcc-105">语法</span><span class="sxs-lookup"><span data-stu-id="75bcc-105">Syntax</span></span>  
  
```cpp  
HRESULT ThreadCreated(  
    [in] ThreadID threadId);
```  
  
## <a name="parameters"></a><span data-ttu-id="75bcc-106">参数</span><span class="sxs-lookup"><span data-stu-id="75bcc-106">Parameters</span></span>  

 `threadId`  
 <span data-ttu-id="75bcc-107">中已创建的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="75bcc-107">[in] The ID of the thread that has been created.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="75bcc-108">备注</span><span class="sxs-lookup"><span data-stu-id="75bcc-108">Remarks</span></span>  

 <span data-ttu-id="75bcc-109">`threadId`值立即有效。</span><span class="sxs-lookup"><span data-stu-id="75bcc-109">The `threadId` value is immediately valid.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="75bcc-110">要求</span><span class="sxs-lookup"><span data-stu-id="75bcc-110">Requirements</span></span>  

 <span data-ttu-id="75bcc-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="75bcc-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="75bcc-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="75bcc-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="75bcc-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="75bcc-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="75bcc-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="75bcc-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75bcc-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="75bcc-115">See also</span></span>

- [<span data-ttu-id="75bcc-116">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="75bcc-116">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="75bcc-117">ThreadDestroyed 方法</span><span class="sxs-lookup"><span data-stu-id="75bcc-117">ThreadDestroyed Method</span></span>](icorprofilercallback-threaddestroyed-method.md)
