---
description: 了解详细信息： ICorProfilerCallback：： AssemblyLoadStarted 方法
title: ICorProfilerCallback::AssemblyLoadStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AssemblyLoadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AssemblyLoadStarted
helpviewer_keywords:
- ICorProfilerCallback::AssemblyLoadStarted method [.NET Framework profiling]
- AssemblyLoadStarted method [.NET Framework profiling]
ms.assetid: 67e8209d-a0ca-4118-a6e6-c1ee0abc2221
topic_type:
- apiref
ms.openlocfilehash: f771008b9aed9322f0c5fd279fa9dfb3086755e5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647999"
---
# <a name="icorprofilercallbackassemblyloadstarted-method"></a><span data-ttu-id="c6906-103">ICorProfilerCallback::AssemblyLoadStarted 方法</span><span class="sxs-lookup"><span data-stu-id="c6906-103">ICorProfilerCallback::AssemblyLoadStarted Method</span></span>

<span data-ttu-id="c6906-104">通知探查器正在加载程序集。</span><span class="sxs-lookup"><span data-stu-id="c6906-104">Notifies the profiler that an assembly is being loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c6906-105">语法</span><span class="sxs-lookup"><span data-stu-id="c6906-105">Syntax</span></span>  
  
```cpp  
HRESULT AssemblyLoadStarted(  
    [in] AssemblyID assemblyId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c6906-106">参数</span><span class="sxs-lookup"><span data-stu-id="c6906-106">Parameters</span></span>

- `assemblyId`

  <span data-ttu-id="c6906-107">\[in] 标识要加载的程序集。</span><span class="sxs-lookup"><span data-stu-id="c6906-107">\[in] Identifies the assembly that is being loaded.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6906-108">备注</span><span class="sxs-lookup"><span data-stu-id="c6906-108">Remarks</span></span>  

 <span data-ttu-id="c6906-109">在 `assemblyId` 调用 [ICorProfilerCallback：： AssemblyLoadFinished](icorprofilercallback-assemblyloadfinished-method.md) 方法之前，的值对信息请求无效。</span><span class="sxs-lookup"><span data-stu-id="c6906-109">The value of `assemblyId` is not valid for an information request until the [ICorProfilerCallback::AssemblyLoadFinished](icorprofilercallback-assemblyloadfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c6906-110">要求</span><span class="sxs-lookup"><span data-stu-id="c6906-110">Requirements</span></span>  

 <span data-ttu-id="c6906-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c6906-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c6906-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c6906-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c6906-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c6906-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c6906-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c6906-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6906-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="c6906-115">See also</span></span>

- [<span data-ttu-id="c6906-116">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="c6906-116">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
