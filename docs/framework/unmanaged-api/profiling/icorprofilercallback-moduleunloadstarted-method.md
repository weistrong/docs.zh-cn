---
description: 了解详细信息： ICorProfilerCallback：： ModuleUnloadStarted 方法
title: ICorProfilerCallback::ModuleUnloadStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleUnloadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleUnloadStarted
helpviewer_keywords:
- ModuleUnloadStarted method [.NET Framework profiling]
- ICorProfilerCallback::ModuleUnloadStarted method [.NET Framework profiling]
ms.assetid: 2debcaab-6005-4245-afdb-4268bb7e74bd
topic_type:
- apiref
ms.openlocfilehash: 3d10654e23481fe6f8956129a0aef7ed4206bba9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745211"
---
# <a name="icorprofilercallbackmoduleunloadstarted-method"></a><span data-ttu-id="3fc34-103">ICorProfilerCallback::ModuleUnloadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="3fc34-103">ICorProfilerCallback::ModuleUnloadStarted Method</span></span>

<span data-ttu-id="3fc34-104">通知探查器正在卸载模块。</span><span class="sxs-lookup"><span data-stu-id="3fc34-104">Notifies the profiler that a module is being unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3fc34-105">语法</span><span class="sxs-lookup"><span data-stu-id="3fc34-105">Syntax</span></span>  
  
```cpp  
HRESULT ModuleUnloadStarted(  
    [in] ModuleID moduleId);
```  
  
## <a name="parameters"></a><span data-ttu-id="3fc34-106">参数</span><span class="sxs-lookup"><span data-stu-id="3fc34-106">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="3fc34-107">中正在卸载的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="3fc34-107">[in] The ID of the module that is being unloaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3fc34-108">备注</span><span class="sxs-lookup"><span data-stu-id="3fc34-108">Remarks</span></span>  

 <span data-ttu-id="3fc34-109">在 `moduleId` 方法返回后，的值对信息请求无效 `ModuleUnloadStarted` -这是探查器获取有关此模块的信息的最后机会。</span><span class="sxs-lookup"><span data-stu-id="3fc34-109">The value of `moduleId` is not valid for an information request after the `ModuleUnloadStarted` method returns — this is the profiler's last chance to get information about this module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3fc34-110">要求</span><span class="sxs-lookup"><span data-stu-id="3fc34-110">Requirements</span></span>  

 <span data-ttu-id="3fc34-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3fc34-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3fc34-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3fc34-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3fc34-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3fc34-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3fc34-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3fc34-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3fc34-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="3fc34-115">See also</span></span>

- [<span data-ttu-id="3fc34-116">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="3fc34-116">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="3fc34-117">ModuleUnloadFinished 方法</span><span class="sxs-lookup"><span data-stu-id="3fc34-117">ModuleUnloadFinished Method</span></span>](icorprofilercallback-moduleunloadfinished-method.md)
