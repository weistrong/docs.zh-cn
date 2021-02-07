---
description: 了解详细信息： ICorProfilerCallback：： ClassLoadStarted 方法
title: ICorProfilerCallback::ClassLoadStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ClassLoadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ClassLoadStarted
helpviewer_keywords:
- ICorProfilerCallback::ClassLoadStarted method [.NET Framework profiling]
- ClassLoadStarted method [.NET Framework profiling]
ms.assetid: 9f728de8-45c2-45a5-ac4a-45660bd36ecf
topic_type:
- apiref
ms.openlocfilehash: 2474f8041b0858cbcb81d3f4042f1748cb99df3e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706429"
---
# <a name="icorprofilercallbackclassloadstarted-method"></a><span data-ttu-id="7842b-103">ICorProfilerCallback::ClassLoadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="7842b-103">ICorProfilerCallback::ClassLoadStarted Method</span></span>

<span data-ttu-id="7842b-104">通知探查器正在加载某个类。</span><span class="sxs-lookup"><span data-stu-id="7842b-104">Notifies the profiler that a class is being loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7842b-105">语法</span><span class="sxs-lookup"><span data-stu-id="7842b-105">Syntax</span></span>  
  
```cpp  
HRESULT ClassLoadStarted(  
    [in] ClassID classId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7842b-106">参数</span><span class="sxs-lookup"><span data-stu-id="7842b-106">Parameters</span></span>

- `classId`

  <span data-ttu-id="7842b-107">\[in] 标识正在加载的类。</span><span class="sxs-lookup"><span data-stu-id="7842b-107">\[in] Identifies the class that is being loaded.</span></span>

## <a name="remarks"></a><span data-ttu-id="7842b-108">备注</span><span class="sxs-lookup"><span data-stu-id="7842b-108">Remarks</span></span>  

 <span data-ttu-id="7842b-109">在 `classId` 调用 [ICorProfilerCallback：： ClassLoadFinished](icorprofilercallback-classloadfinished-method.md) 方法之前，的值对信息请求无效。</span><span class="sxs-lookup"><span data-stu-id="7842b-109">The value of `classId` is not valid for an information request until the [ICorProfilerCallback::ClassLoadFinished](icorprofilercallback-classloadfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7842b-110">要求</span><span class="sxs-lookup"><span data-stu-id="7842b-110">Requirements</span></span>  

 <span data-ttu-id="7842b-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7842b-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7842b-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7842b-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7842b-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7842b-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7842b-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7842b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7842b-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="7842b-115">See also</span></span>

- [<span data-ttu-id="7842b-116">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="7842b-116">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
