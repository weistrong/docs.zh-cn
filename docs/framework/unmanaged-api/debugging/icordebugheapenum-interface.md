---
description: 了解详细信息： ICorDebugHeapEnum 接口
title: ICorDebugHeapEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugHeapEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapEnum
helpviewer_keywords:
- ICorDebugHeapEnum interface [.NET Framework debugging]
ms.assetid: 99cbc1eb-d539-4f76-a0d8-b93348112f14
topic_type:
- apiref
ms.openlocfilehash: c8a2f46bf412e2c4b2fe43d3eb50169191f40445
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660890"
---
# <a name="icordebugheapenum-interface"></a><span data-ttu-id="bbeb2-103">ICorDebugHeapEnum 接口</span><span class="sxs-lookup"><span data-stu-id="bbeb2-103">ICorDebugHeapEnum Interface</span></span>

<span data-ttu-id="bbeb2-104">提供针对托管堆上的对象的枚举器。</span><span class="sxs-lookup"><span data-stu-id="bbeb2-104">Provides an enumerator for objects on the managed heap.</span></span> <span data-ttu-id="bbeb2-105">此接口是 ICorDebugEnum 接口的子类。</span><span class="sxs-lookup"><span data-stu-id="bbeb2-105">This interface is a subclass of the ICorDebugEnum interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bbeb2-106">方法</span><span class="sxs-lookup"><span data-stu-id="bbeb2-106">Methods</span></span>  
  
|<span data-ttu-id="bbeb2-107">方法</span><span class="sxs-lookup"><span data-stu-id="bbeb2-107">Method</span></span>|<span data-ttu-id="bbeb2-108">说明</span><span class="sxs-lookup"><span data-stu-id="bbeb2-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bbeb2-109">下一方法</span><span class="sxs-lookup"><span data-stu-id="bbeb2-109">Next Method</span></span>](icordebugheapenum-next-method.md)|<span data-ttu-id="bbeb2-110">获取指定数量的 [COR_HEAPOBJECT](cor-heapobject-structure.md) 实例，这些实例包含有关托管堆上的对象的信息。</span><span class="sxs-lookup"><span data-stu-id="bbeb2-110">Gets the specified number of [COR_HEAPOBJECT](cor-heapobject-structure.md) instances that contain information about objects on the managed heap.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bbeb2-111">备注</span><span class="sxs-lookup"><span data-stu-id="bbeb2-111">Remarks</span></span>  

 <span data-ttu-id="bbeb2-112">`ICorDebugHeapEnum`接口实现 ICorDebugEnum 接口。</span><span class="sxs-lookup"><span data-stu-id="bbeb2-112">The `ICorDebugHeapEnum` interface implements the ICorDebugEnum interface.</span></span>  
  
 <span data-ttu-id="bbeb2-113">`ICorDebugHeapEnum`实例通过调用[ICorDebugProcess5：： EnumerateHeap](icordebugprocess5-enumerateheap-method.md)方法填充[COR_HEAPOBJECT](cor-heapobject-structure.md)的实例。</span><span class="sxs-lookup"><span data-stu-id="bbeb2-113">An `ICorDebugHeapEnum` instance is populated with [COR_HEAPOBJECT](cor-heapobject-structure.md) instances by calling the [ICorDebugProcess5::EnumerateHeap](icordebugprocess5-enumerateheap-method.md) method.</span></span> <span data-ttu-id="bbeb2-114">集合中的每个 [COR_HEAPOBJECT](cor-heapobject-structure.md) 实例都表示堆上的一个活动对象，或表示一个对象，该对象不是任何对象的根路径，但尚未由垃圾回收器收集。</span><span class="sxs-lookup"><span data-stu-id="bbeb2-114">Each [COR_HEAPOBJECT](cor-heapobject-structure.md) instance in the collection represents either a live object on the heap or an object that is not rooted by any object but has not yet been collected by the garbage collector.</span></span> <span data-ttu-id="bbeb2-115">可以通过调用[ICorDebugHeapEnum：： Next](icordebugheapenum-next-method.md)方法枚举集合中的[COR_HEAPOBJECT](cor-heapobject-structure.md)对象。</span><span class="sxs-lookup"><span data-stu-id="bbeb2-115">The [COR_HEAPOBJECT](cor-heapobject-structure.md) objects in the collection can be enumerated by calling the [ICorDebugHeapEnum::Next](icordebugheapenum-next-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bbeb2-116">要求</span><span class="sxs-lookup"><span data-stu-id="bbeb2-116">Requirements</span></span>  

 <span data-ttu-id="bbeb2-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bbeb2-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bbeb2-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bbeb2-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bbeb2-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bbeb2-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bbeb2-120">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bbeb2-120">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bbeb2-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="bbeb2-121">See also</span></span>

- [<span data-ttu-id="bbeb2-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="bbeb2-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
