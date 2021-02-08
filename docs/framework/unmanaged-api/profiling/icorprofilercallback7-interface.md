---
description: 了解详细信息： ICorProfilerCallback7 接口
title: ICorProfilerCallback7 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback7
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.assetid: a0be019e-aaa1-4036-990f-565f114d4b5c
ms.openlocfilehash: 3db402db221fca4487939f9817b20ec0c5207fc5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781735"
---
# <a name="icorprofilercallback7-interface"></a><span data-ttu-id="d0330-103">ICorProfilerCallback7 接口</span><span class="sxs-lookup"><span data-stu-id="d0330-103">ICorProfilerCallback7 Interface</span></span>

<span data-ttu-id="d0330-104">[仅在 .NET Framework 4.6.1 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="d0330-104">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="d0330-105">提供回调方法的 [ICorProfilerCallback6](icorprofilercallback6-interface.md) 的子类，公共语言运行时使用该方法通知探查器已更新与内存中模块关联的符号流。</span><span class="sxs-lookup"><span data-stu-id="d0330-105">A subclass of [ICorProfilerCallback6](icorprofilercallback6-interface.md) that provides a callback method that the common language runtime uses to notify the profiler that the symbol stream associated with an in-memory module is updated.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d0330-106">方法</span><span class="sxs-lookup"><span data-stu-id="d0330-106">Methods</span></span>  
  
|<span data-ttu-id="d0330-107">方法</span><span class="sxs-lookup"><span data-stu-id="d0330-107">Method</span></span>|<span data-ttu-id="d0330-108">说明</span><span class="sxs-lookup"><span data-stu-id="d0330-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d0330-109">ModuleInMemorySymbolsUpdated 方法</span><span class="sxs-lookup"><span data-stu-id="d0330-109">ModuleInMemorySymbolsUpdated Method</span></span>](icorprofilercallback7-moduleinmemorysymbolsupdated-method.md)|<span data-ttu-id="d0330-110">通知探查器已更新与内存中模块关联的符号流。</span><span class="sxs-lookup"><span data-stu-id="d0330-110">Notifies the profiler that the symbol stream associated with an in-memory module is updated.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d0330-111">要求</span><span class="sxs-lookup"><span data-stu-id="d0330-111">Requirements</span></span>  

 <span data-ttu-id="d0330-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d0330-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0330-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d0330-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d0330-114">**.NET Framework 版本：**[!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d0330-114">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0330-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="d0330-115">See also</span></span>

- [<span data-ttu-id="d0330-116">分析接口</span><span class="sxs-lookup"><span data-stu-id="d0330-116">Profiling Interfaces</span></span>](profiling-interfaces.md)
