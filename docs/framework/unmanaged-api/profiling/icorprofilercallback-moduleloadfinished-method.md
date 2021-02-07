---
description: 了解详细信息： ICorProfilerCallback：： ModuleLoadFinished 方法
title: ICorProfilerCallback::ModuleLoadFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleLoadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleLoadFinished
helpviewer_keywords:
- ModuleLoadFinished method [.NET Framework profiling]
- ICorProfilerCallback::ModuleLoadFinished method [.NET Framework profiling]
ms.assetid: 050649e5-ffc0-4458-a0a4-d9ee128a219e
topic_type:
- apiref
ms.openlocfilehash: 960eb9edd036055069ef3f9ab3a93602ce4ef9bf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745341"
---
# <a name="icorprofilercallbackmoduleloadfinished-method"></a><span data-ttu-id="63765-103">ICorProfilerCallback::ModuleLoadFinished 方法</span><span class="sxs-lookup"><span data-stu-id="63765-103">ICorProfilerCallback::ModuleLoadFinished Method</span></span>

<span data-ttu-id="63765-104">通知探查器模块已完成加载。</span><span class="sxs-lookup"><span data-stu-id="63765-104">Notifies the profiler that a module has finished loading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63765-105">语法</span><span class="sxs-lookup"><span data-stu-id="63765-105">Syntax</span></span>  
  
```cpp  
HRESULT ModuleLoadFinished(  
    [in] ModuleID moduleId,  
    [in] HRESULT  hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="63765-106">参数</span><span class="sxs-lookup"><span data-stu-id="63765-106">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="63765-107">中已完成加载的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="63765-107">[in] The ID of the module that has finished loading.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="63765-108">中一个 HRESULT，指示是否已成功加载该模块。</span><span class="sxs-lookup"><span data-stu-id="63765-108">[in] An HRESULT that indicates whether the module was loaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="63765-109">备注</span><span class="sxs-lookup"><span data-stu-id="63765-109">Remarks</span></span>  

 <span data-ttu-id="63765-110">在 `moduleId` 调用方法之前，的值对信息请求无效 `ModuleLoadFinished` 。</span><span class="sxs-lookup"><span data-stu-id="63765-110">The value of `moduleId` is not valid for an information request until the `ModuleLoadFinished` method is called.</span></span>  
  
 <span data-ttu-id="63765-111">在回调后，加载模块的某些部分可能会继续 `ModuleLoadFinished` 。</span><span class="sxs-lookup"><span data-stu-id="63765-111">Some parts of loading the module might continue after the `ModuleLoadFinished` callback.</span></span> <span data-ttu-id="63765-112">中的 HRESULT 失败 `hrStatus` 表示失败。</span><span class="sxs-lookup"><span data-stu-id="63765-112">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="63765-113">但是，中的成功 HRESULT `hrStatus` 仅指示加载模块的第一部分已成功。</span><span class="sxs-lookup"><span data-stu-id="63765-113">However, a success HRESULT in `hrStatus` indicates only that the first part of loading the module has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="63765-114">要求</span><span class="sxs-lookup"><span data-stu-id="63765-114">Requirements</span></span>  

 <span data-ttu-id="63765-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="63765-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="63765-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="63765-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="63765-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="63765-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="63765-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="63765-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63765-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="63765-119">See also</span></span>

- [<span data-ttu-id="63765-120">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="63765-120">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="63765-121">ModuleLoadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="63765-121">ModuleLoadStarted Method</span></span>](icorprofilercallback-moduleloadstarted-method.md)
