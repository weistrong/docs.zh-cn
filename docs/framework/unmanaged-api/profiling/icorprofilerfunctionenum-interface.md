---
description: 了解详细信息： ICorProfilerFunctionEnum 接口
title: ICorProfilerFunctionEnum 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionEnum
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionEnum
helpviewer_keywords:
- ICorProfilerFunctionEnum interface [.NET Framework profiling]
ms.assetid: 0a1d4a38-cd0b-4231-91df-13646218ae72
topic_type:
- apiref
ms.openlocfilehash: 0a9437ee1f5c481c2c2d1fd46361da6e938dd179
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737592"
---
# <a name="icorprofilerfunctionenum-interface"></a><span data-ttu-id="67db4-103">ICorProfilerFunctionEnum 接口</span><span class="sxs-lookup"><span data-stu-id="67db4-103">ICorProfilerFunctionEnum Interface</span></span>

<span data-ttu-id="67db4-104">提供按顺序循环访问公共语言运行时中的函数集合的方法。</span><span class="sxs-lookup"><span data-stu-id="67db4-104">Provides methods to sequentially iterate through a collection of functions in the common language runtime.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="67db4-105">方法</span><span class="sxs-lookup"><span data-stu-id="67db4-105">Methods</span></span>  
  
|<span data-ttu-id="67db4-106">方法</span><span class="sxs-lookup"><span data-stu-id="67db4-106">Method</span></span>|<span data-ttu-id="67db4-107">说明</span><span class="sxs-lookup"><span data-stu-id="67db4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="67db4-108">Clone 方法</span><span class="sxs-lookup"><span data-stu-id="67db4-108">Clone Method</span></span>](icorprofilerfunctionenum-clone-method.md)|<span data-ttu-id="67db4-109">获取指向此 `ICorProfilerFunctionEnum` 接口副本的接口指针。</span><span class="sxs-lookup"><span data-stu-id="67db4-109">Gets an interface pointer to a copy of this `ICorProfilerFunctionEnum` interface.</span></span>|  
|[<span data-ttu-id="67db4-110">GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="67db4-110">GetCount Method</span></span>](icorprofilerfunctionenum-getcount-method.md)|<span data-ttu-id="67db4-111">获取应用程序加载的函数数量或探查器强制加载的函数数量。</span><span class="sxs-lookup"><span data-stu-id="67db4-111">Gets the number of functions that were loaded by the application or forcibly loaded by the profiler.</span></span>|  
|[<span data-ttu-id="67db4-112">下一方法</span><span class="sxs-lookup"><span data-stu-id="67db4-112">Next Method</span></span>](icorprofilerfunctionenum-next-method.md)|<span data-ttu-id="67db4-113">从一个函数的顺序集合中获取指定数量的连续函数（从枚举器在序列中的当前位置开始）。</span><span class="sxs-lookup"><span data-stu-id="67db4-113">Gets the specified number of contiguous functions from a sequential collection of functions, starting at the enumerator's current position in the sequence.</span></span>|  
|[<span data-ttu-id="67db4-114">Reset 方法</span><span class="sxs-lookup"><span data-stu-id="67db4-114">Reset Method</span></span>](icorprofilerfunctionenum-reset-method.md)|<span data-ttu-id="67db4-115">将枚举器的光标移动到序列的起始位置。</span><span class="sxs-lookup"><span data-stu-id="67db4-115">Moves the enumerator's cursor to the starting position of the sequence.</span></span>|  
|[<span data-ttu-id="67db4-116">Skip 方法</span><span class="sxs-lookup"><span data-stu-id="67db4-116">Skip Method</span></span>](icorprofilerfunctionenum-skip-method.md)|<span data-ttu-id="67db4-117">将枚举器的游标从其当前位置前移，以便跳过指定数量的元素。</span><span class="sxs-lookup"><span data-stu-id="67db4-117">Advances the enumerator's cursor from its current position so that the specified number of elements are skipped.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="67db4-118">备注</span><span class="sxs-lookup"><span data-stu-id="67db4-118">Remarks</span></span>  

 <span data-ttu-id="67db4-119">`ICorProfilerFunctionEnum` 接口是一个枚举器。</span><span class="sxs-lookup"><span data-stu-id="67db4-119">The `ICorProfilerFunctionEnum` interface is an enumerator.</span></span> <span data-ttu-id="67db4-120">它可以让数组接收器以其合适的速率从发送器拉取元素。</span><span class="sxs-lookup"><span data-stu-id="67db4-120">It allows the receiver of an array to pull elements from the sender at a rate that is appropriate for the receiver.</span></span> <span data-ttu-id="67db4-121">换而言之，接收器可以显式控制数组元素流，从而避免将大型数组作为方法形参传递方面的相关问题。</span><span class="sxs-lookup"><span data-stu-id="67db4-121">In other words, the receiver is able to explicitly control the flow of array elements, thereby avoiding the problems associated with passing large arrays as method parameters.</span></span>  
  
 <span data-ttu-id="67db4-122">`ICorProfilerFunctionEnum` 枚举已经过 JIT 编译的函数，但不包括从使用 Ngen.exe 生成的本机映像加载的函数。</span><span class="sxs-lookup"><span data-stu-id="67db4-122">`ICorProfilerFunctionEnum` enumerates over functions that have already been JIT-compiled, but does not include functions that are loaded from native images generated with Ngen.exe.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="67db4-123">要求</span><span class="sxs-lookup"><span data-stu-id="67db4-123">Requirements</span></span>  

 <span data-ttu-id="67db4-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="67db4-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="67db4-125">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="67db4-125">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="67db4-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="67db4-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="67db4-127">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="67db4-127">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67db4-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="67db4-128">See also</span></span>

- [<span data-ttu-id="67db4-129">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="67db4-129">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="67db4-130">分析接口</span><span class="sxs-lookup"><span data-stu-id="67db4-130">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="67db4-131">EnumJITedFunctions 方法</span><span class="sxs-lookup"><span data-stu-id="67db4-131">EnumJITedFunctions Method</span></span>](icorprofilerinfo3-enumjitedfunctions-method.md)
