---
description: 了解详细信息： ICorProfilerAssemblyReferenceProvider 接口
title: ICorProfilerAssemblyReferenceProvider 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerAssemblyReferenceProvider
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: 17205116-66e1-4acc-8f01-532fb3867028
topic_type:
- apiref
ms.openlocfilehash: 0f16bad95dba46452ce5cc8ad1bbe6ca1bfeb7c8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648345"
---
# <a name="icorprofilerassemblyreferenceprovider-interface"></a><span data-ttu-id="19e39-103">ICorProfilerAssemblyReferenceProvider 方法</span><span class="sxs-lookup"><span data-stu-id="19e39-103">ICorProfilerAssemblyReferenceProvider Interface</span></span>

<span data-ttu-id="19e39-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="19e39-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="19e39-105">使探查器能够向公共语言运行 (时通知) 探查器将在 [ICorProfilerCallback：： ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) 回调中添加的程序集引用的 CLR。</span><span class="sxs-lookup"><span data-stu-id="19e39-105">Enables the profiler to inform the common language runtime (CLR) of assembly references that the profiler will add in the [ICorProfilerCallback::ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) callback.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="19e39-106">方法</span><span class="sxs-lookup"><span data-stu-id="19e39-106">Methods</span></span>  
  
|<span data-ttu-id="19e39-107">方法</span><span class="sxs-lookup"><span data-stu-id="19e39-107">Method</span></span>|<span data-ttu-id="19e39-108">说明</span><span class="sxs-lookup"><span data-stu-id="19e39-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="19e39-109">AddAssemblyReference 方法</span><span class="sxs-lookup"><span data-stu-id="19e39-109">AddAssemblyReference Method</span></span>](icorprofilerassemblyreferenceprovider-addassemblyreference-method.md)|<span data-ttu-id="19e39-110">向 CLR 通知探查器计划在 [ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) 回调中添加的程序集引用。</span><span class="sxs-lookup"><span data-stu-id="19e39-110">Informs the CLR of an assembly reference that the profiler plans to add in the [ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md) callback.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="19e39-111">备注</span><span class="sxs-lookup"><span data-stu-id="19e39-111">Remarks</span></span>  

 <span data-ttu-id="19e39-112">CLR 将探查器的 `ICorProfilerAssemblyReferenceProvider` 接口对象传递给 [ICorProfilerCallback6：： GetAssemblyReferences](icorprofilercallback6-getassemblyreferences-method.md) 回调。</span><span class="sxs-lookup"><span data-stu-id="19e39-112">The CLR passes the profiler an `ICorProfilerAssemblyReferenceProvider` interface object in the [ICorProfilerCallback6::GetAssemblyReferences](icorprofilercallback6-getassemblyreferences-method.md) callback.</span></span> <span data-ttu-id="19e39-113">这使探查器能够通知程序集引用的 CLR，探查器计划稍后将其添加到 [ICorProfilerCallback：： ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md)中。</span><span class="sxs-lookup"><span data-stu-id="19e39-113">This enables the profiler to inform the CLR of assembly references that the profiler plans to add later in the [ICorProfilerCallback::ModuleLoadFinished](icorprofilercallback-moduleloadfinished-method.md).</span></span> <span data-ttu-id="19e39-114">回调中。</span><span class="sxs-lookup"><span data-stu-id="19e39-114">callback.</span></span> <span data-ttu-id="19e39-115">这提高了 CLR 的程序集引用闭包审核器，及其用于确定是否可以共享程序集的算法的准确性。</span><span class="sxs-lookup"><span data-stu-id="19e39-115">This improves the accuracy of the CLR's assembly reference closure walker and its algorithms for determining whether assemblies may be shared.</span></span>  
  
 <span data-ttu-id="19e39-116">此接口只能在将此接口对象传递给探查器的 [ICorProfilerCallback6：： GetAssemblyReferences](icorprofilercallback6-getassemblyreferences-method.md) 回调中使用。</span><span class="sxs-lookup"><span data-stu-id="19e39-116">This interface can be used only in the [ICorProfilerCallback6::GetAssemblyReferences](icorprofilercallback6-getassemblyreferences-method.md) callback that passes this interface object to the profiler.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="19e39-117">要求</span><span class="sxs-lookup"><span data-stu-id="19e39-117">Requirements</span></span>  

 <span data-ttu-id="19e39-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="19e39-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="19e39-119">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="19e39-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="19e39-120">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="19e39-120">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19e39-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="19e39-121">See also</span></span>

- [<span data-ttu-id="19e39-122">分析接口</span><span class="sxs-lookup"><span data-stu-id="19e39-122">Profiling Interfaces</span></span>](profiling-interfaces.md)
