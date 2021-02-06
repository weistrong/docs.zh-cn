---
description: 了解详细信息： ICorProfilerCallback：： AssemblyLoadFinished 方法
title: ICorProfilerCallback::AssemblyLoadFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AssemblyLoadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AssemblyLoadFinished
helpviewer_keywords:
- ICorProfilerCallback::AssemblyLoadFinished method [.NET Framework profiling]
- AssemblyLoadFinished method [.NET Framework profiling]
ms.assetid: 86d98f39-52e6-4c61-a625-9760f695ff12
topic_type:
- apiref
ms.openlocfilehash: 19c0871808455e64ad8a4eb002806a87030f7882
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648033"
---
# <a name="icorprofilercallbackassemblyloadfinished-method"></a><span data-ttu-id="31447-103">ICorProfilerCallback::AssemblyLoadFinished 方法</span><span class="sxs-lookup"><span data-stu-id="31447-103">ICorProfilerCallback::AssemblyLoadFinished Method</span></span>

<span data-ttu-id="31447-104">通知探查器程序集已完成加载。</span><span class="sxs-lookup"><span data-stu-id="31447-104">Notifies the profiler that an assembly has finished loading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="31447-105">语法</span><span class="sxs-lookup"><span data-stu-id="31447-105">Syntax</span></span>  
  
```cpp  
HRESULT AssemblyLoadFinished(  
    [in] AssemblyID assemblyId,  
    [in] HRESULT    hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="31447-106">参数</span><span class="sxs-lookup"><span data-stu-id="31447-106">Parameters</span></span>

- `assemblyId`

  <span data-ttu-id="31447-107">\[in] 标识已加载的程序集。</span><span class="sxs-lookup"><span data-stu-id="31447-107">\[in] Identifies the assembly that was loaded.</span></span>

- `hrStatus`

  <span data-ttu-id="31447-108">\[in] 一个 HRESULT，指示程序集是否已成功加载。</span><span class="sxs-lookup"><span data-stu-id="31447-108">\[in] An HRESULT that indicates whether the assembly finished loading successfully.</span></span>

## <a name="remarks"></a><span data-ttu-id="31447-109">备注</span><span class="sxs-lookup"><span data-stu-id="31447-109">Remarks</span></span>  

 <span data-ttu-id="31447-110">在 `assemblyId` 调用方法之前，的值对信息请求无效 `AssemblyLoadFinished` 。</span><span class="sxs-lookup"><span data-stu-id="31447-110">The value of `assemblyId` is not valid for an information request until the `AssemblyLoadFinished` method is called.</span></span>  
  
 <span data-ttu-id="31447-111">在回调后，加载程序集的某些部分可能会继续 `AssemblyLoadFinished` 。</span><span class="sxs-lookup"><span data-stu-id="31447-111">Some parts of loading the assembly might continue after the `AssemblyLoadFinished` callback.</span></span> <span data-ttu-id="31447-112">中的 HRESULT 失败 `hrStatus` 表示失败。</span><span class="sxs-lookup"><span data-stu-id="31447-112">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="31447-113">但是，中的成功 HRESULT `hrStatus` 仅指示加载程序集的第一部分已成功完成。</span><span class="sxs-lookup"><span data-stu-id="31447-113">However, a success HRESULT in `hrStatus` indicates only that the first part of loading the assembly has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="31447-114">要求</span><span class="sxs-lookup"><span data-stu-id="31447-114">Requirements</span></span>  

 <span data-ttu-id="31447-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="31447-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="31447-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="31447-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="31447-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="31447-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="31447-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="31447-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="31447-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="31447-119">See also</span></span>

- [<span data-ttu-id="31447-120">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="31447-120">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
