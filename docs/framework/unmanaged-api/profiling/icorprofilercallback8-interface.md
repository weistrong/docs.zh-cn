---
description: 了解详细信息： ICorProfilerCallback8 接口
title: ICorProfilerCallback8 接口
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback8
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.openlocfilehash: 8dd9b8eea82f38b7598d578bd718743af826070d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781670"
---
# <a name="icorprofilercallback8-interface"></a><span data-ttu-id="c6db1-103">ICorProfilerCallback8 接口</span><span class="sxs-lookup"><span data-stu-id="c6db1-103">ICorProfilerCallback8 Interface</span></span>

<span data-ttu-id="c6db1-104">[.NET Framework 4.7 及更高版本中支持]</span><span class="sxs-lookup"><span data-stu-id="c6db1-104">[Supported in the .NET Framework 4.7 and later versions]</span></span>  

 <span data-ttu-id="c6db1-105">提供回调方法的 [ICorProfilerCallback7](icorprofilercallback7-interface.md) 的子类，公共语言运行时使用该方法通知探查器动态方法的 JIT 编译已开始和完成。</span><span class="sxs-lookup"><span data-stu-id="c6db1-105">A subclass of [ICorProfilerCallback7](icorprofilercallback7-interface.md) that provides callback methods used by the common language runtime to notify the profiler that JIT compilation of a dynamic method has started and finished.</span></span>
  
## <a name="methods"></a><span data-ttu-id="c6db1-106">方法</span><span class="sxs-lookup"><span data-stu-id="c6db1-106">Methods</span></span>  
  
|<span data-ttu-id="c6db1-107">方法</span><span class="sxs-lookup"><span data-stu-id="c6db1-107">Method</span></span>|<span data-ttu-id="c6db1-108">说明</span><span class="sxs-lookup"><span data-stu-id="c6db1-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c6db1-109">DynamicMethodJITCompilationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="c6db1-109">DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)|<span data-ttu-id="c6db1-110">通知探查器已经开始对动态方法进行 JIT 编译。</span><span class="sxs-lookup"><span data-stu-id="c6db1-110">Notifies the profiler that JIT compilation of a dynamic method has started.</span></span>|  
|[<span data-ttu-id="c6db1-111">DynamicMethodJITCompilationFinished 方法</span><span class="sxs-lookup"><span data-stu-id="c6db1-111">DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)|<span data-ttu-id="c6db1-112">通知探查器已完成动态方法的 JIT 编译。</span><span class="sxs-lookup"><span data-stu-id="c6db1-112">Notifies the profiler that JIT compilation of a dynamic method has finished.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c6db1-113">要求</span><span class="sxs-lookup"><span data-stu-id="c6db1-113">Requirements</span></span>  

 <span data-ttu-id="c6db1-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c6db1-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c6db1-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c6db1-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
<span data-ttu-id="c6db1-116">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="c6db1-116">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="c6db1-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="c6db1-117">See also</span></span>

- [<span data-ttu-id="c6db1-118">分析接口</span><span class="sxs-lookup"><span data-stu-id="c6db1-118">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="c6db1-119">ICorProfilerCallback9 接口</span><span class="sxs-lookup"><span data-stu-id="c6db1-119">ICorProfilerCallback9 Interface</span></span>](icorprofilercallback9-interface.md)
