---
description: 了解详细信息： ICorProfilerCallback9 接口
title: ICorProfilerCallback9 接口
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback9
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.openlocfilehash: 4bfcaf6f8985909ef9142ef4d08535a19facd7e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781644"
---
# <a name="icorprofilercallback9-interface"></a><span data-ttu-id="e570a-103">ICorProfilerCallback9 接口</span><span class="sxs-lookup"><span data-stu-id="e570a-103">ICorProfilerCallback9 Interface</span></span>

<span data-ttu-id="e570a-104">[.NET Framework 4.7.2 和更高版本中支持]</span><span class="sxs-lookup"><span data-stu-id="e570a-104">[Supported in the .NET Framework 4.7.2 and later versions]</span></span>  

 <span data-ttu-id="e570a-105">提供回调方法的 [ICorProfilerCallback8](icorprofilercallback8-interface.md) 的子类，公共语言运行时使用该方法通知探查器动态方法已被垃圾回收并随后卸载。</span><span class="sxs-lookup"><span data-stu-id="e570a-105">A subclass of [ICorProfilerCallback8](icorprofilercallback8-interface.md) that provides a callback method used by the common language runtime to notify the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e570a-106">方法</span><span class="sxs-lookup"><span data-stu-id="e570a-106">Methods</span></span>  
  
|<span data-ttu-id="e570a-107">方法</span><span class="sxs-lookup"><span data-stu-id="e570a-107">Method</span></span>|<span data-ttu-id="e570a-108">说明</span><span class="sxs-lookup"><span data-stu-id="e570a-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e570a-109">DynamicMethodUnloaded 方法</span><span class="sxs-lookup"><span data-stu-id="e570a-109">DynamicMethodUnloaded Method</span></span>](ICorProfilerCallback9-dynamicmethodunloaded-method.md)|<span data-ttu-id="e570a-110">通知探查器已对动态方法进行了垃圾回收并随后将其卸载。</span><span class="sxs-lookup"><span data-stu-id="e570a-110">Notifies the profiler that a dynamic method has been garbage collected and subsequently unloaded.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e570a-111">要求</span><span class="sxs-lookup"><span data-stu-id="e570a-111">Requirements</span></span>  

 <span data-ttu-id="e570a-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e570a-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e570a-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e570a-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="e570a-114">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="e570a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="e570a-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="e570a-115">See also</span></span>

- [<span data-ttu-id="e570a-116">分析接口</span><span class="sxs-lookup"><span data-stu-id="e570a-116">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="e570a-117">ICorProfilerCallback8 接口</span><span class="sxs-lookup"><span data-stu-id="e570a-117">ICorProfilerCallback8 Interface</span></span>](icorprofilercallback9-interface.md)
- [<span data-ttu-id="e570a-118">ICorProfilerCallback8. DynamicMethodJITCompilationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="e570a-118">ICorProfilerCallback8.DynamicMethodJITCompilationStarted method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [<span data-ttu-id="e570a-119">ICorProfilerCallback8. DynamicMethodJITCompilationFinished 方法</span><span class="sxs-lookup"><span data-stu-id="e570a-119">ICorProfilerCallback8.DynamicMethodJITCompilationFinished method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
