---
description: 了解详细信息： ICorProfilerCallback：： ModuleLoadStarted 方法
title: ICorProfilerCallback::ModuleLoadStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleLoadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleLoadStarted
helpviewer_keywords:
- ModuleLoadStarted method [.NET Framework profiling]
- ICorProfilerCallback::ModuleLoadStarted method [.NET Framework profiling]
ms.assetid: 9cd2fe75-408a-400f-a6b1-9979624a2fe2
topic_type:
- apiref
ms.openlocfilehash: e8d15bece7baf82f69162663da00d331c7904837
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745260"
---
# <a name="icorprofilercallbackmoduleloadstarted-method"></a><span data-ttu-id="c509b-103">ICorProfilerCallback::ModuleLoadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="c509b-103">ICorProfilerCallback::ModuleLoadStarted Method</span></span>

<span data-ttu-id="c509b-104">通知探查器正在加载模块。</span><span class="sxs-lookup"><span data-stu-id="c509b-104">Notifies the profiler that a module is being loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c509b-105">语法</span><span class="sxs-lookup"><span data-stu-id="c509b-105">Syntax</span></span>  
  
```cpp  
HRESULT ModuleLoadStarted(  
    [in] ModuleID moduleId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c509b-106">参数</span><span class="sxs-lookup"><span data-stu-id="c509b-106">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="c509b-107">中正在加载的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="c509b-107">[in] The ID of the module that is being loaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c509b-108">备注</span><span class="sxs-lookup"><span data-stu-id="c509b-108">Remarks</span></span>  

 <span data-ttu-id="c509b-109">在 `moduleId` 调用 [ICorProfilerCallback：： ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) 方法之前，的值对信息请求无效。</span><span class="sxs-lookup"><span data-stu-id="c509b-109">The value of `moduleId` is not valid for an information request until the [ICorProfilerCallback::ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c509b-110">要求</span><span class="sxs-lookup"><span data-stu-id="c509b-110">Requirements</span></span>  

 <span data-ttu-id="c509b-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c509b-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c509b-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c509b-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c509b-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c509b-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c509b-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c509b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c509b-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="c509b-115">See also</span></span>

- [<span data-ttu-id="c509b-116">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="c509b-116">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
