---
description: 了解详细信息： ICorProfilerCallback：： ClassUnloadFinished 方法
title: ICorProfilerCallback::ClassUnloadFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ClassUnloadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ClassUnloadFinished
helpviewer_keywords:
- ICorProfilerCallback::ClassUnloadFinished method [.NET Framework profiling]
- ClassUnloadFinished method [.NET Framework profiling]
ms.assetid: 55674b68-678a-4747-ae06-4e91519c7305
topic_type:
- apiref
ms.openlocfilehash: ae1ef56a1eb3b9b45c2165ecceb0af826cc7a2ea
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657731"
---
# <a name="icorprofilercallbackclassunloadfinished-method"></a><span data-ttu-id="5a1d2-103">ICorProfilerCallback::ClassUnloadFinished 方法</span><span class="sxs-lookup"><span data-stu-id="5a1d2-103">ICorProfilerCallback::ClassUnloadFinished Method</span></span>

<span data-ttu-id="5a1d2-104">通知探查器类已经完成卸载。</span><span class="sxs-lookup"><span data-stu-id="5a1d2-104">Notifies the profiler that a class has finished unloading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5a1d2-105">语法</span><span class="sxs-lookup"><span data-stu-id="5a1d2-105">Syntax</span></span>  
  
```cpp  
HRESULT ClassUnloadFinished(  
    [in] ClassID classId,  
    [in] HRESULT hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5a1d2-106">参数</span><span class="sxs-lookup"><span data-stu-id="5a1d2-106">Parameters</span></span>

- `classId`

  <span data-ttu-id="5a1d2-107">\[in] 标识已卸载的类。</span><span class="sxs-lookup"><span data-stu-id="5a1d2-107">\[in] Identifies the class that was unloaded.</span></span>

- `hrStatus`

  <span data-ttu-id="5a1d2-108">\[在] 中指示是否已成功卸载类的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="5a1d2-108">\[in] An HRESULT that indicates whether the class was unloaded successfully.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a1d2-109">备注</span><span class="sxs-lookup"><span data-stu-id="5a1d2-109">Remarks</span></span>  

 <span data-ttu-id="5a1d2-110">卸载类的某些部分可能会在回调后继续 `ClassUnloadFinished` 。</span><span class="sxs-lookup"><span data-stu-id="5a1d2-110">Some parts of unloading the class might continue after the `ClassUnloadFinished` callback.</span></span> <span data-ttu-id="5a1d2-111">中的 HRESULT 失败 `hrStatus` 表示失败。</span><span class="sxs-lookup"><span data-stu-id="5a1d2-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="5a1d2-112">但是，中的成功 HRESULT `hrStatus` 仅指示卸载类的第一部分已成功。</span><span class="sxs-lookup"><span data-stu-id="5a1d2-112">However, a success HRESULT in `hrStatus` indicates only that the first part of unloading the class has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5a1d2-113">要求</span><span class="sxs-lookup"><span data-stu-id="5a1d2-113">Requirements</span></span>  

 <span data-ttu-id="5a1d2-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5a1d2-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5a1d2-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5a1d2-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5a1d2-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5a1d2-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5a1d2-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5a1d2-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5a1d2-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="5a1d2-118">See also</span></span>

- [<span data-ttu-id="5a1d2-119">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="5a1d2-119">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="5a1d2-120">ClassUnloadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="5a1d2-120">ClassUnloadStarted Method</span></span>](icorprofilercallback-classunloadstarted-method.md)
