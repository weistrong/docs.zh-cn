---
description: 了解详细信息： ICorDebugReferenceValue 接口
title: ICorDebugReferenceValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue
helpviewer_keywords:
- ICorDebugReferenceValue interface [.NET Framework debugging]
ms.assetid: 2040e2be-119a-4cfb-ae52-b0b6f052665c
topic_type:
- apiref
ms.openlocfilehash: e516b1178b4f4268472dedd37d6443e673e16af6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690959"
---
# <a name="icordebugreferencevalue-interface"></a><span data-ttu-id="6703c-103">ICorDebugReferenceValue 接口</span><span class="sxs-lookup"><span data-stu-id="6703c-103">ICorDebugReferenceValue Interface</span></span>

<span data-ttu-id="6703c-104">提供管理作为对对象的引用的值的方法。</span><span class="sxs-lookup"><span data-stu-id="6703c-104">Provides methods that manage a value that is a reference to an object.</span></span> <span data-ttu-id="6703c-105"> (即，此接口提供管理指针的方法。 ) 此接口实现 "ICorDebugValue"。</span><span class="sxs-lookup"><span data-stu-id="6703c-105">(That is, this interface provides methods that manage a pointer.) This interface implements "ICorDebugValue".</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6703c-106">方法</span><span class="sxs-lookup"><span data-stu-id="6703c-106">Methods</span></span>  
  
|<span data-ttu-id="6703c-107">方法</span><span class="sxs-lookup"><span data-stu-id="6703c-107">Method</span></span>|<span data-ttu-id="6703c-108">说明</span><span class="sxs-lookup"><span data-stu-id="6703c-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6703c-109">Dereference 方法</span><span class="sxs-lookup"><span data-stu-id="6703c-109">Dereference Method</span></span>](icordebugreferencevalue-dereference-method.md)|<span data-ttu-id="6703c-110">获取所引用的对象。</span><span class="sxs-lookup"><span data-stu-id="6703c-110">Gets the object that is referenced.</span></span>|  
|[<span data-ttu-id="6703c-111">DereferenceStrong 方法</span><span class="sxs-lookup"><span data-stu-id="6703c-111">DereferenceStrong Method</span></span>](icordebugreferencevalue-dereferencestrong-method.md)|<span data-ttu-id="6703c-112">未实现。</span><span class="sxs-lookup"><span data-stu-id="6703c-112">Not implemented.</span></span> <span data-ttu-id="6703c-113">请勿调用此方法。</span><span class="sxs-lookup"><span data-stu-id="6703c-113">Do not call this method.</span></span>|  
|[<span data-ttu-id="6703c-114">GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="6703c-114">GetValue Method</span></span>](icordebugreferencevalue-getvalue-method.md)|<span data-ttu-id="6703c-115">获取所引用对象的当前内存地址。</span><span class="sxs-lookup"><span data-stu-id="6703c-115">Gets the current memory address of the referenced object.</span></span>|  
|[<span data-ttu-id="6703c-116">IsNull 方法</span><span class="sxs-lookup"><span data-stu-id="6703c-116">IsNull Method</span></span>](icordebugreferencevalue-isnull-method.md)|<span data-ttu-id="6703c-117">获取一个值，该值指示此 `ICorDebugReferenceValue` 值是否为 null 值，在这种情况下，不 `ICorDebugReferenceValue` 指向对象。</span><span class="sxs-lookup"><span data-stu-id="6703c-117">Gets a value that indicates whether this `ICorDebugReferenceValue` is a null value, in which case the `ICorDebugReferenceValue` does not point to an object.</span></span>|  
|[<span data-ttu-id="6703c-118">SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="6703c-118">SetValue Method</span></span>](icordebugreferencevalue-setvalue-method.md)|<span data-ttu-id="6703c-119">设置当前内存地址。</span><span class="sxs-lookup"><span data-stu-id="6703c-119">Sets the current memory address.</span></span> <span data-ttu-id="6703c-120">也就是说，此方法会将此设置 `ICorDebugReferenceValue` 为指向对象。</span><span class="sxs-lookup"><span data-stu-id="6703c-120">That is, this method sets this `ICorDebugReferenceValue` to point to an object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6703c-121">备注</span><span class="sxs-lookup"><span data-stu-id="6703c-121">Remarks</span></span>  

 <span data-ttu-id="6703c-122">在继续调试进程时，公共语言运行时 (CLR) 可以对对象进行垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="6703c-122">The common language runtime (CLR) may do a garbage collection on objects when the debugged process is continued.</span></span> <span data-ttu-id="6703c-123">垃圾回收可能会在内存中移动对象。</span><span class="sxs-lookup"><span data-stu-id="6703c-123">The garbage collection may move objects around in memory.</span></span> <span data-ttu-id="6703c-124">`ICorDebugReferenceValue`将与垃圾回收一起合作，以便在垃圾回收后更新其信息，或者在垃圾回收之前隐式地将其无效。</span><span class="sxs-lookup"><span data-stu-id="6703c-124">An `ICorDebugReferenceValue` will either cooperate with the garbage collection so that its information is updated after the garbage collection, or it will be invalidated implicitly before the garbage collection.</span></span>  
  
 <span data-ttu-id="6703c-125">`ICorDebugReferenceValue`继续调试的进程后，对象可能会隐式失效。</span><span class="sxs-lookup"><span data-stu-id="6703c-125">The `ICorDebugReferenceValue` object may be implicitly invalidated after the debugged process has been continued.</span></span> <span data-ttu-id="6703c-126">派生的 "ICorDebugHandleValue" 在显式发布或公开之前不会失效。</span><span class="sxs-lookup"><span data-stu-id="6703c-126">The derived "ICorDebugHandleValue" is not invalidated until it is explicitly released or exposed.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="6703c-127">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="6703c-127">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6703c-128">要求</span><span class="sxs-lookup"><span data-stu-id="6703c-128">Requirements</span></span>  

 <span data-ttu-id="6703c-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6703c-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6703c-130">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6703c-130">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6703c-131">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6703c-131">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6703c-132">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6703c-132">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6703c-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="6703c-133">See also</span></span>

- [<span data-ttu-id="6703c-134">调试接口</span><span class="sxs-lookup"><span data-stu-id="6703c-134">Debugging Interfaces</span></span>](debugging-interfaces.md)
