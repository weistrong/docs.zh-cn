---
description: 了解详细信息： ICorProfilerInfo10 接口
title: ICorProfilerInfo10 接口
ms.date: 08/06/2019
author: davmason
ms.author: davmason
ms.openlocfilehash: f2fa0115f6894ac737696b63c1f0f00a0cb028ec
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102106899"
---
# <a name="icorprofilerinfo10-interface"></a><span data-ttu-id="a728e-103">ICorProfilerInfo10 接口</span><span class="sxs-lookup"><span data-stu-id="a728e-103">ICorProfilerInfo10 Interface</span></span>

<span data-ttu-id="a728e-104">[ICorProfilerInfo9](icorprofilerinfo9-interface.md)的子类，提供用于修改函数 IL、从运行时查询信息以及挂起和恢复运行时的方法。</span><span class="sxs-lookup"><span data-stu-id="a728e-104">A subclass of [ICorProfilerInfo9](icorprofilerinfo9-interface.md) that provides methods to modify function IL, query information from the runtime, and suspend and resume the runtime.</span></span>

## <a name="methods"></a><span data-ttu-id="a728e-105">方法</span><span class="sxs-lookup"><span data-stu-id="a728e-105">Methods</span></span>  

| <span data-ttu-id="a728e-106">方法</span><span class="sxs-lookup"><span data-stu-id="a728e-106">Method</span></span>|<span data-ttu-id="a728e-107">说明</span><span class="sxs-lookup"><span data-stu-id="a728e-107">Description</span></span>|  
| ------------|-----------------|  
|[<span data-ttu-id="a728e-108">EnumerateObjectReferences 方法</span><span class="sxs-lookup"><span data-stu-id="a728e-108">EnumerateObjectReferences Method</span></span>](icorprofilerinfo10-enumerateobjectreferences-method.md)|<span data-ttu-id="a728e-109">给定 ObjectID、callback 和 clientData，如果有任何) ，则枚举 (的每个对象引用。</span><span class="sxs-lookup"><span data-stu-id="a728e-109">Given an ObjectID, callback and clientData, enumerates each object reference (if any).</span></span> |
|[<span data-ttu-id="a728e-110">IsFrozenObject 方法</span><span class="sxs-lookup"><span data-stu-id="a728e-110">IsFrozenObject Method</span></span>](icorprofilerinfo10-isfrozenobject-method.md)|<span data-ttu-id="a728e-111">给定 ObjectID，确定对象是否位于只读段。</span><span class="sxs-lookup"><span data-stu-id="a728e-111">Given an ObjectID, determines whether the object is in a read-only segment.</span></span> |
|[<span data-ttu-id="a728e-112">GetLOHObjectSizeThreshold 方法</span><span class="sxs-lookup"><span data-stu-id="a728e-112">GetLOHObjectSizeThreshold Method</span></span>](icorprofilerinfo10-getlohobjectsizethreshold-method.md)|<span data-ttu-id="a728e-113">获取配置的 LOH 阈值的值。</span><span class="sxs-lookup"><span data-stu-id="a728e-113">Gets the value of the configured LOH threshold.</span></span> |
|[<span data-ttu-id="a728e-114">RequestReJITWithInliners 方法</span><span class="sxs-lookup"><span data-stu-id="a728e-114">RequestReJITWithInliners Method</span></span>](icorprofilerinfo10-requestrejitwithinliners-method.md)| <span data-ttu-id="a728e-115">ReJITs 请求的方法，以及所请求的方法的任何 inliners。</span><span class="sxs-lookup"><span data-stu-id="a728e-115">ReJITs the methods requested, as well as any inliners of the methods requested.</span></span>  |
|[<span data-ttu-id="a728e-116">SuspendRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="a728e-116">SuspendRuntime Method</span></span>](icorprofilerinfo10-suspendruntime-method.md)| <span data-ttu-id="a728e-117">挂起运行时，而不执行 GC。</span><span class="sxs-lookup"><span data-stu-id="a728e-117">Suspends the runtime without performing a GC.</span></span> |
|[<span data-ttu-id="a728e-118">ResumeRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="a728e-118">ResumeRuntime Method</span></span>](icorprofilerinfo10-resumeruntime-method.md)| <span data-ttu-id="a728e-119">恢复运行时，而不执行 GC。</span><span class="sxs-lookup"><span data-stu-id="a728e-119">Resumes the runtime without performing a GC.</span></span> |

## <a name="requirements"></a><span data-ttu-id="a728e-120">要求</span><span class="sxs-lookup"><span data-stu-id="a728e-120">Requirements</span></span>  

<span data-ttu-id="a728e-121">**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。</span><span class="sxs-lookup"><span data-stu-id="a728e-121">**Platforms:** See [.NET Core supported operating systems](../../../core/install/windows.md?pivots=os-windows).</span></span>  
<span data-ttu-id="a728e-122">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a728e-122">**Header:** CorProf.idl, CorProf.h</span></span>  
<span data-ttu-id="a728e-123">**.Net 版本：**[!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a728e-123">**.NET Versions:** [!INCLUDE[net_core_30](../../../../includes/net-core-30-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="a728e-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a728e-124">See also</span></span>

- [<span data-ttu-id="a728e-125">分析接口</span><span class="sxs-lookup"><span data-stu-id="a728e-125">Profiling Interfaces</span></span>](profiling-interfaces.md)
