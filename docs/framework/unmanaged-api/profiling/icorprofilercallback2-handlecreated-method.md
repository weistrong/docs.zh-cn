---
description: 了解详细信息： ICorProfilerCallback2：： HandleCreated 方法
title: ICorProfilerCallback2::HandleCreated 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.HandleCreated
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::HandleCreated
helpviewer_keywords:
- HandleCreated method [.NET Framework profiling]
- ICorProfilerCallback2::HandleCreated method [.NET Framework profiling]
ms.assetid: 6bbb7786-7c38-490f-9834-91aa2795c355
topic_type:
- apiref
ms.openlocfilehash: 17f4ed83646907a229dcc6a30dcce1b52fa608d5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657081"
---
# <a name="icorprofilercallback2handlecreated-method"></a><span data-ttu-id="3c410-103">ICorProfilerCallback2::HandleCreated 方法</span><span class="sxs-lookup"><span data-stu-id="3c410-103">ICorProfilerCallback2::HandleCreated Method</span></span>

<span data-ttu-id="3c410-104">通知代码探查器已创建垃圾回收句柄。</span><span class="sxs-lookup"><span data-stu-id="3c410-104">Notifies the code profiler that a garbage collection handle has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c410-105">语法</span><span class="sxs-lookup"><span data-stu-id="3c410-105">Syntax</span></span>  
  
```cpp  
HRESULT HandleCreated(  
    [in] GCHandleID handleId,  
    [in] ObjectID initialObjectId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3c410-106">参数</span><span class="sxs-lookup"><span data-stu-id="3c410-106">Parameters</span></span>  

 `handleId`  
 <span data-ttu-id="3c410-107">中垃圾回收的句柄的 ID。</span><span class="sxs-lookup"><span data-stu-id="3c410-107">[in] The ID of the handle for the garbage collection.</span></span>  
  
 `initialObjectId`  
 <span data-ttu-id="3c410-108">中为其创建垃圾回收句柄的对象的 ID。</span><span class="sxs-lookup"><span data-stu-id="3c410-108">[in] The ID of the object for which the garbage collection handle was created.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c410-109">要求</span><span class="sxs-lookup"><span data-stu-id="3c410-109">Requirements</span></span>  

 <span data-ttu-id="3c410-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3c410-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c410-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3c410-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3c410-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3c410-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3c410-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c410-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c410-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="3c410-114">See also</span></span>

- [<span data-ttu-id="3c410-115">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="3c410-115">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="3c410-116">ICorProfilerCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="3c410-116">ICorProfilerCallback2 Interface</span></span>](icorprofilercallback2-interface.md)
