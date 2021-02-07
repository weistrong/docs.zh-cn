---
description: 了解详细信息： ICorProfilerCallback9：:D ynamicMethodUnloaded 方法
title: ICorProfilerCallback9：:D ynamicMethodUnloaded 方法
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback9.DynamicMethodUnloaded
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.openlocfilehash: 243660d3159e3c8c1d052c08e9c7499e7065d301
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753323"
---
# <a name="icorprofilercallback9dynamicmethodunloaded-method"></a><span data-ttu-id="4c959-103">ICorProfilerCallback9：:D ynamicMethodUnloaded 方法</span><span class="sxs-lookup"><span data-stu-id="4c959-103">ICorProfilerCallback9::DynamicMethodUnloaded Method</span></span>

<span data-ttu-id="4c959-104">[.NET Framework 4.7.2 和更高版本中支持]</span><span class="sxs-lookup"><span data-stu-id="4c959-104">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  
  
<span data-ttu-id="4c959-105">每当对动态方法进行垃圾回收并随后卸载时，通知探查器。</span><span class="sxs-lookup"><span data-stu-id="4c959-105">Notifies the profiler whenever a dynamic method is garbage collected and subsequently unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c959-106">语法</span><span class="sxs-lookup"><span data-stu-id="4c959-106">Syntax</span></span>  
  
```cpp  
HRESULT DynamicMethodUnloaded(  
     [in]  FunctionID  functionId
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4c959-107">参数</span><span class="sxs-lookup"><span data-stu-id="4c959-107">Parameters</span></span>  

<span data-ttu-id="4c959-108">[in] `functionId`</span><span class="sxs-lookup"><span data-stu-id="4c959-108">[in] `functionId`</span></span>  
<span data-ttu-id="4c959-109">已被垃圾回收和卸载的内存中函数的标识符。</span><span class="sxs-lookup"><span data-stu-id="4c959-109">The identifier of the in-memory function that has been garbage collected and unloaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c959-110">要求</span><span class="sxs-lookup"><span data-stu-id="4c959-110">Requirements</span></span>  

 <span data-ttu-id="4c959-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4c959-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4c959-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="4c959-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="4c959-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4c959-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4c959-114">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="4c959-114">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c959-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="4c959-115">See also</span></span>

- [<span data-ttu-id="4c959-116">ICorProfilerCallback8. DynamicMethodJITCompilationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="4c959-116">ICorProfilerCallback8.DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [<span data-ttu-id="4c959-117">ICorProfilerCallback8. DynamicMethodJITCompilationFinished 方法</span><span class="sxs-lookup"><span data-stu-id="4c959-117">ICorProfilerCallback8.DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
- [<span data-ttu-id="4c959-118">ICorProfilerCallback9 接口</span><span class="sxs-lookup"><span data-stu-id="4c959-118">ICorProfilerCallback9 Interface</span></span>](icorprofilercallback9-interface.md)
- [<span data-ttu-id="4c959-119">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span><span class="sxs-lookup"><span data-stu-id="4c959-119">COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS</span></span>](cor-prf-high-monitor-enumeration.md)
