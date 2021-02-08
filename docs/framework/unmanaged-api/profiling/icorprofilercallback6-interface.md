---
description: 了解详细信息： ICorProfilerCallback6 接口
title: ICorProfilerCallback6 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback6
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.assetid: edc420b7-96d1-4dec-ace0-36d907f644bc
topic_type:
- apiref
ms.openlocfilehash: 12eaafff8bd9ab8d4d58eac8f2d62415531bc898
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781748"
---
# <a name="icorprofilercallback6-interface"></a><span data-ttu-id="52dcd-103">ICorProfilerCallback6 接口</span><span class="sxs-lookup"><span data-stu-id="52dcd-103">ICorProfilerCallback6 Interface</span></span>

<span data-ttu-id="52dcd-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="52dcd-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="52dcd-105">提供回调方法的 [ICorProfilerCallback5](icorprofilercallback5-interface.md) 的子类，公共语言运行时使用该方法通知探查器正在加载程序集。</span><span class="sxs-lookup"><span data-stu-id="52dcd-105">A subclass of [ICorProfilerCallback5](icorprofilercallback5-interface.md) that provides a callback method that the common language runtime uses to notify a profiler that an assembly is loading.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="52dcd-106">方法</span><span class="sxs-lookup"><span data-stu-id="52dcd-106">Methods</span></span>  
  
|<span data-ttu-id="52dcd-107">方法</span><span class="sxs-lookup"><span data-stu-id="52dcd-107">Method</span></span>|<span data-ttu-id="52dcd-108">说明</span><span class="sxs-lookup"><span data-stu-id="52dcd-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="52dcd-109">GetAssemblyReferences 方法</span><span class="sxs-lookup"><span data-stu-id="52dcd-109">GetAssemblyReferences Method</span></span>](icorprofilercallback6-getassemblyreferences-method.md)|<span data-ttu-id="52dcd-110">当公共语言运行时执行程序集引用闭包审核时，通知探查器程序集正处于非常早期的加载阶段。</span><span class="sxs-lookup"><span data-stu-id="52dcd-110">Notifies the profiler that an assembly is in a very early loading stage, when the common language runtime performs an assembly reference closure walk.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="52dcd-111">备注</span><span class="sxs-lookup"><span data-stu-id="52dcd-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="52dcd-112">要求</span><span class="sxs-lookup"><span data-stu-id="52dcd-112">Requirements</span></span>  

 <span data-ttu-id="52dcd-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="52dcd-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="52dcd-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="52dcd-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="52dcd-115">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="52dcd-115">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="52dcd-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="52dcd-116">See also</span></span>

- [<span data-ttu-id="52dcd-117">分析接口</span><span class="sxs-lookup"><span data-stu-id="52dcd-117">Profiling Interfaces</span></span>](profiling-interfaces.md)
