---
description: 了解详细信息： ICorDebugGCReferenceEnum 接口
title: ICorDebugGCReferenceEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugGCReferenceEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGCReferenceEnum
helpviewer_keywords:
- ICorDebugGCReferenceEnum interface [.NET Framework debugging]
ms.assetid: 5f3c91c9-c035-454f-96cc-011cab1ea06b
topic_type:
- apiref
ms.openlocfilehash: ad4a61cdc2b30fb4c8e2be500eae878327c6b449
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801288"
---
# <a name="icordebuggcreferenceenum-interface"></a><span data-ttu-id="7cace-103">ICorDebugGCReferenceEnum 接口</span><span class="sxs-lookup"><span data-stu-id="7cace-103">ICorDebugGCReferenceEnum Interface</span></span>

<span data-ttu-id="7cace-104">提供针对将进行垃圾回收的对象的枚举器。</span><span class="sxs-lookup"><span data-stu-id="7cace-104">Provides an enumerator for objects that will be garbage-collected.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7cace-105">方法</span><span class="sxs-lookup"><span data-stu-id="7cace-105">Methods</span></span>  
  
|<span data-ttu-id="7cace-106">方法</span><span class="sxs-lookup"><span data-stu-id="7cace-106">Method</span></span>|<span data-ttu-id="7cace-107">说明</span><span class="sxs-lookup"><span data-stu-id="7cace-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7cace-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="7cace-108">Next Method</span></span>](icordebuggcreferenceenum-next-method.md)|<span data-ttu-id="7cace-109">获取指定数量的 [COR_GC_REFERENCE](cor-gc-reference-structure.md) 实例，这些实例包含有关将进行垃圾回收的对象的信息。</span><span class="sxs-lookup"><span data-stu-id="7cace-109">Gets the specified number of [COR_GC_REFERENCE](cor-gc-reference-structure.md) instances that contain information about objects that will be garbage-collected.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7cace-110">备注</span><span class="sxs-lookup"><span data-stu-id="7cace-110">Remarks</span></span>  

 <span data-ttu-id="7cace-111">`ICorDebugGCReferenceEnum`接口实现 "ICorDebugEnum" 接口。</span><span class="sxs-lookup"><span data-stu-id="7cace-111">The `ICorDebugGCReferenceEnum` interface implements the "ICorDebugEnum" interface.</span></span>  
  
 <span data-ttu-id="7cace-112">`ICorDebugGCReferenceEnum`实例通过调用[ICorDebugProcess5：： EnumerateGCReferences](icordebugprocess5-enumerategcreferences-method.md)方法填充[COR_GC_REFERENCE](cor-gc-reference-structure.md)的实例。</span><span class="sxs-lookup"><span data-stu-id="7cace-112">An `ICorDebugGCReferenceEnum` instance is populated with [COR_GC_REFERENCE](cor-gc-reference-structure.md) instances by calling the [ICorDebugProcess5::EnumerateGCReferences](icordebugprocess5-enumerategcreferences-method.md) method.</span></span> <span data-ttu-id="7cace-113">可以通过调用[ICorDebugGCReference：： Next](icordebuggcreferenceenum-next-method.md)方法来枚举[COR_GC_REFERENCE](cor-gc-reference-structure.md)的对象。</span><span class="sxs-lookup"><span data-stu-id="7cace-113">[COR_GC_REFERENCE](cor-gc-reference-structure.md) objects can be enumerated by calling the [ICorDebugGCReference::Next](icordebuggcreferenceenum-next-method.md) method.</span></span>  
  
 <span data-ttu-id="7cace-114">此方法填充的集合中的 [COR_GC_REFERENCE](cor-gc-reference-structure.md) 对象表示三种对象：</span><span class="sxs-lookup"><span data-stu-id="7cace-114">The [COR_GC_REFERENCE](cor-gc-reference-structure.md) objects in the collection populated by this method represent three kinds of objects:</span></span>  
  
- <span data-ttu-id="7cace-115">所有托管堆栈中的对象。</span><span class="sxs-lookup"><span data-stu-id="7cace-115">Objects from all managed stacks.</span></span> <span data-ttu-id="7cace-116">这包括托管代码中的实时引用以及由公共语言运行时创建的对象。</span><span class="sxs-lookup"><span data-stu-id="7cace-116">This includes live references in managed code as well as objects created by the common language runtime.</span></span>  
  
- <span data-ttu-id="7cace-117">句柄表中的对象。</span><span class="sxs-lookup"><span data-stu-id="7cace-117">Objects from the handle table.</span></span> <span data-ttu-id="7cace-118">这包括 `HNDTYPE_STRONG` 模块中 (和 `HNDTYPE_REFCOUNT`) 和静态变量的强引用。</span><span class="sxs-lookup"><span data-stu-id="7cace-118">This includes strong references (`HNDTYPE_STRONG` and `HNDTYPE_REFCOUNT`) and static variables in a module.</span></span>  
  
- <span data-ttu-id="7cace-119">终结器队列中的对象。</span><span class="sxs-lookup"><span data-stu-id="7cace-119">Objects from the finalizer queue.</span></span> <span data-ttu-id="7cace-120">终结器队列根对象，直到终结器运行。</span><span class="sxs-lookup"><span data-stu-id="7cace-120">The finalizer queue roots objects until the finalizer has run.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7cace-121">要求</span><span class="sxs-lookup"><span data-stu-id="7cace-121">Requirements</span></span>  

 <span data-ttu-id="7cace-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7cace-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7cace-123">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7cace-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7cace-124">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7cace-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7cace-125">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7cace-125">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7cace-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="7cace-126">See also</span></span>

- [<span data-ttu-id="7cace-127">调试接口</span><span class="sxs-lookup"><span data-stu-id="7cace-127">Debugging Interfaces</span></span>](debugging-interfaces.md)
