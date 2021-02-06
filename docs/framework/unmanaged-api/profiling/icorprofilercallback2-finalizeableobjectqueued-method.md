---
description: 了解详细信息： ICorProfilerCallback2：： FinalizeableObjectQueued 方法
title: ICorProfilerCallback2::FinalizeableObjectQueued 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.FinalizeableObjectQueued
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::FinalizeableObjectQueued
helpviewer_keywords:
- FinalizeableObjectQueued method [.NET Framework profiling]
- ICorProfilerCallback2::FinalizeableObjectQueued method [.NET Framework profiling]
ms.assetid: 92d76893-683c-475d-9996-5bff03cdb10f
topic_type:
- apiref
ms.openlocfilehash: 62424ea60f72cee2328a143e4e50acd7af33e221
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647903"
---
# <a name="icorprofilercallback2finalizeableobjectqueued-method"></a><span data-ttu-id="8f305-103">ICorProfilerCallback2::FinalizeableObjectQueued 方法</span><span class="sxs-lookup"><span data-stu-id="8f305-103">ICorProfilerCallback2::FinalizeableObjectQueued Method</span></span>

<span data-ttu-id="8f305-104">通知代码探查器，具有终结器的对象已排入终结器线程，以执行其 `Finalize` 方法。</span><span class="sxs-lookup"><span data-stu-id="8f305-104">Notifies the code profiler that an object with a finalizer has been queued to the finalizer thread for execution of its `Finalize` method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f305-105">语法</span><span class="sxs-lookup"><span data-stu-id="8f305-105">Syntax</span></span>  
  
```cpp  
HRESULT FinalizeableObjectQueued(  
    [in] DWORD finalizerFlags,  
    [in] ObjectID objectID);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8f305-106">参数</span><span class="sxs-lookup"><span data-stu-id="8f305-106">Parameters</span></span>  

 `finalizerFlags`  
 <span data-ttu-id="8f305-107">中一个 [COR_PRF_FINALIZER_FLAGS](cor-prf-finalizer-flags-enumeration.md) 枚举的值，该值描述终结器的各个方面。</span><span class="sxs-lookup"><span data-stu-id="8f305-107">[in] A value of the [COR_PRF_FINALIZER_FLAGS](cor-prf-finalizer-flags-enumeration.md) enumeration that describes aspects of the finalizer.</span></span>  
  
 `objectID`  
 <span data-ttu-id="8f305-108">中已排队的对象的 ID。</span><span class="sxs-lookup"><span data-stu-id="8f305-108">[in] The ID of the object that has been queued.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8f305-109">要求</span><span class="sxs-lookup"><span data-stu-id="8f305-109">Requirements</span></span>  

 <span data-ttu-id="8f305-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8f305-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8f305-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8f305-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8f305-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8f305-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8f305-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8f305-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f305-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="8f305-114">See also</span></span>

- [<span data-ttu-id="8f305-115">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="8f305-115">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="8f305-116">ICorProfilerCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="8f305-116">ICorProfilerCallback2 Interface</span></span>](icorprofilercallback2-interface.md)
