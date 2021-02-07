---
description: 了解详细信息： ICorProfilerCallback2：： HandleDestroyed 方法
title: ICorProfilerCallback2::HandleDestroyed 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.HandleDestroyed
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::HandleDestroyed
helpviewer_keywords:
- ICorProfilerCallback2::HandleDestroyed method [.NET Framework profiling]
- HandleDestroyed method [.NET Framework profiling]
ms.assetid: ab4f4bbd-40c7-4667-bfde-60cd73803110
topic_type:
- apiref
ms.openlocfilehash: d583a2170efbb4ebe72d7eacdd60af1a089a518f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99705563"
---
# <a name="icorprofilercallback2handledestroyed-method"></a><span data-ttu-id="5b7f4-103">ICorProfilerCallback2::HandleDestroyed 方法</span><span class="sxs-lookup"><span data-stu-id="5b7f4-103">ICorProfilerCallback2::HandleDestroyed Method</span></span>

<span data-ttu-id="5b7f4-104">通知代码探查器垃圾回收句柄已销毁。</span><span class="sxs-lookup"><span data-stu-id="5b7f4-104">Notifies the code profiler that a garbage collection handle has been destroyed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5b7f4-105">语法</span><span class="sxs-lookup"><span data-stu-id="5b7f4-105">Syntax</span></span>  
  
```cpp  
HRESULT HandleDestroyed(  
    [in] GCHandleID handleId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5b7f4-106">参数</span><span class="sxs-lookup"><span data-stu-id="5b7f4-106">Parameters</span></span>  

 `handleId`  
 <span data-ttu-id="5b7f4-107">中垃圾回收的句柄的 ID。</span><span class="sxs-lookup"><span data-stu-id="5b7f4-107">[in] The ID of the handle for the garbage collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5b7f4-108">要求</span><span class="sxs-lookup"><span data-stu-id="5b7f4-108">Requirements</span></span>  

 <span data-ttu-id="5b7f4-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5b7f4-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5b7f4-110">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5b7f4-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5b7f4-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5b7f4-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5b7f4-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5b7f4-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5b7f4-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="5b7f4-113">See also</span></span>

- [<span data-ttu-id="5b7f4-114">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="5b7f4-114">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="5b7f4-115">ICorProfilerCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="5b7f4-115">ICorProfilerCallback2 Interface</span></span>](icorprofilercallback2-interface.md)
