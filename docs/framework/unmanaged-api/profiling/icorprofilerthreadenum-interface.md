---
description: 了解详细信息： ICorProfilerThreadEnum 接口
title: ICorProfilerThreadEnum 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum
helpviewer_keywords:
- ICorProfilerThreadEnum interface [.NET Framework profiling]
ms.assetid: 1e35031b-e095-4c14-9644-8deeb3081e0b
topic_type:
- apiref
ms.openlocfilehash: 035296412aabf20503588a558c8e8ccc1338210e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636385"
---
# <a name="icorprofilerthreadenum-interface"></a><span data-ttu-id="d8d81-103">ICorProfilerThreadEnum 接口</span><span class="sxs-lookup"><span data-stu-id="d8d81-103">ICorProfilerThreadEnum Interface</span></span>

<span data-ttu-id="d8d81-104">提供方法以按顺序循环访问公共语言运行时中的线程集合。</span><span class="sxs-lookup"><span data-stu-id="d8d81-104">Provides methods to sequentially iterate through a collection of threads in the common language runtime.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d8d81-105">方法</span><span class="sxs-lookup"><span data-stu-id="d8d81-105">Methods</span></span>  
  
|<span data-ttu-id="d8d81-106">方法</span><span class="sxs-lookup"><span data-stu-id="d8d81-106">Method</span></span>|<span data-ttu-id="d8d81-107">说明</span><span class="sxs-lookup"><span data-stu-id="d8d81-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d8d81-108">Clone 方法</span><span class="sxs-lookup"><span data-stu-id="d8d81-108">Clone Method</span></span>](icorprofilerthreadenum-clone-method.md)|<span data-ttu-id="d8d81-109">获取指向此 `ICorProfilerThreadEnum` 接口副本的接口指针。</span><span class="sxs-lookup"><span data-stu-id="d8d81-109">Gets an interface pointer to a copy of this `ICorProfilerThreadEnum` interface.</span></span>|  
|[<span data-ttu-id="d8d81-110">GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="d8d81-110">GetCount Method</span></span>](icorprofilerthreadenum-getcount-method.md)|<span data-ttu-id="d8d81-111">获取应用程序使用的线程数。</span><span class="sxs-lookup"><span data-stu-id="d8d81-111">Gets the number of threads that are used by the application.</span></span>|  
|[<span data-ttu-id="d8d81-112">下一方法</span><span class="sxs-lookup"><span data-stu-id="d8d81-112">Next Method</span></span>](icorprofilerthreadenum-next-method.md)|<span data-ttu-id="d8d81-113">从线程的序列集合获取指定的连续线程数，从序列中枚举器的当前位置开始。</span><span class="sxs-lookup"><span data-stu-id="d8d81-113">Gets the specified number of contiguous threads from a sequential collection of threads, starting at the enumerator's current position in the sequence.</span></span>|  
|[<span data-ttu-id="d8d81-114">Reset 方法</span><span class="sxs-lookup"><span data-stu-id="d8d81-114">Reset Method</span></span>](icorprofilerthreadenum-reset-method.md)|<span data-ttu-id="d8d81-115">将枚举器的光标移动到序列的起始位置。</span><span class="sxs-lookup"><span data-stu-id="d8d81-115">Moves the enumerator's cursor to the starting position of the sequence.</span></span>|  
|[<span data-ttu-id="d8d81-116">Skip 方法</span><span class="sxs-lookup"><span data-stu-id="d8d81-116">Skip Method</span></span>](icorprofilerthreadenum-skip-method.md)|<span data-ttu-id="d8d81-117">从当前位置前移枚举器的光标，以便跳过指定的元素数量。</span><span class="sxs-lookup"><span data-stu-id="d8d81-117">Advances the enumerator's cursor from its current position to skip the specified number of elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d8d81-118">备注</span><span class="sxs-lookup"><span data-stu-id="d8d81-118">Remarks</span></span>  

 <span data-ttu-id="d8d81-119">`ICorProfilerThreadEnum` 接口是一个枚举器。</span><span class="sxs-lookup"><span data-stu-id="d8d81-119">The `ICorProfilerThreadEnum` interface is an enumerator.</span></span> <span data-ttu-id="d8d81-120">它可以让数组接收器以其合适的速率从发送器拉取元素。</span><span class="sxs-lookup"><span data-stu-id="d8d81-120">It allows the receiver of an array to pull elements from the sender at a rate that is appropriate for the receiver.</span></span> <span data-ttu-id="d8d81-121">换而言之，接收器可以显式控制数组元素流，从而避免将大型数组作为方法形参传递方面的相关问题。</span><span class="sxs-lookup"><span data-stu-id="d8d81-121">In other words, the receiver is able to explicitly control the flow of array elements, thereby avoiding the problems associated with passing large arrays as method parameters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8d81-122">要求</span><span class="sxs-lookup"><span data-stu-id="d8d81-122">Requirements</span></span>  

 <span data-ttu-id="d8d81-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d8d81-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8d81-124">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d8d81-124">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d8d81-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d8d81-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d8d81-126">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8d81-126">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8d81-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="d8d81-127">See also</span></span>

- [<span data-ttu-id="d8d81-128">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="d8d81-128">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="d8d81-129">分析接口</span><span class="sxs-lookup"><span data-stu-id="d8d81-129">Profiling Interfaces</span></span>](profiling-interfaces.md)
