---
description: 了解详细信息： ICorProfilerCallback：： Initialize 方法
title: ICorProfilerCallback::Initialize 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.Initialize
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::Initialize
helpviewer_keywords:
- Initialize method, ICorProfilerCallback interface [.NET Framework profiling]
- ICorProfilerCallback::Initialize method [.NET Framework profiling]
ms.assetid: dc5fab2a-4b45-4b12-8727-b89c9915f23e
topic_type:
- apiref
ms.openlocfilehash: b3ff579dee384b331450aa54aace39890febfe30
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99705936"
---
# <a name="icorprofilercallbackinitialize-method"></a><span data-ttu-id="0e6ca-103">ICorProfilerCallback::Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="0e6ca-103">ICorProfilerCallback::Initialize Method</span></span>

<span data-ttu-id="0e6ca-104">调用以在新的公共语言运行时 (CLR) 应用程序启动时初始化代码探查器。</span><span class="sxs-lookup"><span data-stu-id="0e6ca-104">Called to initialize the code profiler whenever a new common language runtime (CLR) application is started.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e6ca-105">语法</span><span class="sxs-lookup"><span data-stu-id="0e6ca-105">Syntax</span></span>  
  
```cpp  
HRESULT Initialize(  
    [in] IUnknown     *pICorProfilerInfoUnk);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0e6ca-106">参数</span><span class="sxs-lookup"><span data-stu-id="0e6ca-106">Parameters</span></span>

- `pICorProfilerInfoUnk`

  <span data-ttu-id="0e6ca-107">\[in] 指向 [IUnknown](/cpp/atl/iunknown) 接口的指针，探查器必须查询 [ICorProfilerInfo](icorprofilerinfo-interface.md) 接口指针。</span><span class="sxs-lookup"><span data-stu-id="0e6ca-107">\[in] Pointer to an [IUnknown](/cpp/atl/iunknown) interface that the profiler must query for an [ICorProfilerInfo](icorprofilerinfo-interface.md) interface pointer.</span></span>  

## <a name="remarks"></a><span data-ttu-id="0e6ca-108">备注</span><span class="sxs-lookup"><span data-stu-id="0e6ca-108">Remarks</span></span>  

 <span data-ttu-id="0e6ca-109">`Initialize`调用是启用 (或禁用不可变的) 回调的唯一机会。</span><span class="sxs-lookup"><span data-stu-id="0e6ca-109">The `Initialize` call is the only opportunity to enable (or disable) callbacks that are immutable.</span></span> <span data-ttu-id="0e6ca-110">一旦调用启用了回调 `Initialize` ，以后就不能再使用 [ICorProfilerInfo：： SetEventMask](icorprofilerinfo-seteventmask-method.md)来禁用它。</span><span class="sxs-lookup"><span data-stu-id="0e6ca-110">Once a callback is enabled by the `Initialize` call, it cannot be disabled later using [ICorProfilerInfo::SetEventMask](icorprofilerinfo-seteventmask-method.md).</span></span> <span data-ttu-id="0e6ca-111">[COR_PRF_MONITOR](cor-prf-monitor-enumeration.md)枚举的 COR_PRF_MONITOR_IMMUTABLE 值指示哪些事件是不可变的。</span><span class="sxs-lookup"><span data-stu-id="0e6ca-111">The COR_PRF_MONITOR_IMMUTABLE value of the [COR_PRF_MONITOR](cor-prf-monitor-enumeration.md) enumeration indicates which events are immutable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0e6ca-112">要求</span><span class="sxs-lookup"><span data-stu-id="0e6ca-112">Requirements</span></span>  

 <span data-ttu-id="0e6ca-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0e6ca-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0e6ca-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="0e6ca-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="0e6ca-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0e6ca-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0e6ca-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0e6ca-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e6ca-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="0e6ca-117">See also</span></span>

- [<span data-ttu-id="0e6ca-118">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="0e6ca-118">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="0e6ca-119">Shutdown 方法</span><span class="sxs-lookup"><span data-stu-id="0e6ca-119">Shutdown Method</span></span>](icorprofilercallback-shutdown-method.md)
