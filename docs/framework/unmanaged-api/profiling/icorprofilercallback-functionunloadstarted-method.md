---
description: 了解详细信息： ICorProfilerCallback：： FunctionUnloadStarted 方法
title: ICorProfilerCallback::FunctionUnloadStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.FunctionUnloadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::FunctionUnloadStarted
helpviewer_keywords:
- FunctionUnloadStarted method [.NET Framework profiling]
- ICorProfilerCallback::FunctionUnloadStarted method [.NET Framework profiling]
ms.assetid: d6a5fa8b-09c6-47a5-b60e-6cf2e355df30
topic_type:
- apiref
ms.openlocfilehash: 3dd5d46a224c0c51dfee251cf5d0c6ae9320b630
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99705949"
---
# <a name="icorprofilercallbackfunctionunloadstarted-method"></a><span data-ttu-id="28e09-103">ICorProfilerCallback::FunctionUnloadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="28e09-103">ICorProfilerCallback::FunctionUnloadStarted Method</span></span>

<span data-ttu-id="28e09-104">通知探查器运行时已开始卸载某个函数。</span><span class="sxs-lookup"><span data-stu-id="28e09-104">Notifies the profiler that the runtime has started to unload a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28e09-105">语法</span><span class="sxs-lookup"><span data-stu-id="28e09-105">Syntax</span></span>  
  
```cpp  
HRESULT FunctionUnloadStarted(  
    [in] FunctionID functionId);
```  
  
## <a name="parameters"></a><span data-ttu-id="28e09-106">参数</span><span class="sxs-lookup"><span data-stu-id="28e09-106">Parameters</span></span>

- `functionId`

  <span data-ttu-id="28e09-107">\[in] 正在卸载的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="28e09-107">\[in] The ID of the function that is being unloaded.</span></span>

## <a name="remarks"></a><span data-ttu-id="28e09-108">备注</span><span class="sxs-lookup"><span data-stu-id="28e09-108">Remarks</span></span>  

 <span data-ttu-id="28e09-109">`functionId`此方法返回到调用方后，该参数的值不再有效。</span><span class="sxs-lookup"><span data-stu-id="28e09-109">The value of the `functionId` parameter is no longer valid after this method returns to the caller.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="28e09-110">要求</span><span class="sxs-lookup"><span data-stu-id="28e09-110">Requirements</span></span>  

 <span data-ttu-id="28e09-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="28e09-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="28e09-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="28e09-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="28e09-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="28e09-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="28e09-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="28e09-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28e09-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="28e09-115">See also</span></span>

- [<span data-ttu-id="28e09-116">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="28e09-116">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
