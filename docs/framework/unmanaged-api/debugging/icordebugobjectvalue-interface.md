---
description: 了解详细信息： ICorDebugObjectValue 接口
title: ICorDebugObjectValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugObjectValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectValue
helpviewer_keywords:
- ICorDebugObjectValue interface [.NET Framework debugging]
ms.assetid: 937de6a0-6fbf-4ddc-80ea-a6217b73e62b
topic_type:
- apiref
ms.openlocfilehash: a2af438bbb4c2f56eb1a72151e339b6b0a978eec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794762"
---
# <a name="icordebugobjectvalue-interface"></a><span data-ttu-id="43479-103">ICorDebugObjectValue 接口</span><span class="sxs-lookup"><span data-stu-id="43479-103">ICorDebugObjectValue Interface</span></span>

<span data-ttu-id="43479-104">"ICorDebugValue" 的子类，表示包含对象的值。</span><span class="sxs-lookup"><span data-stu-id="43479-104">A subclass of "ICorDebugValue" that represents a value that contains an object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="43479-105">方法</span><span class="sxs-lookup"><span data-stu-id="43479-105">Methods</span></span>  
  
|<span data-ttu-id="43479-106">方法</span><span class="sxs-lookup"><span data-stu-id="43479-106">Method</span></span>|<span data-ttu-id="43479-107">说明</span><span class="sxs-lookup"><span data-stu-id="43479-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="43479-108">GetClass 方法</span><span class="sxs-lookup"><span data-stu-id="43479-108">GetClass Method</span></span>](icordebugobjectvalue-getclass-method.md)|<span data-ttu-id="43479-109">获取指向公共语言运行时的接口指针，该指针指向此引用的对象 (CLR) <xref:System.Type> `ICorDebugObjectValue` 。</span><span class="sxs-lookup"><span data-stu-id="43479-109">Gets an interface pointer to the common language runtime (CLR) <xref:System.Type> of the object that this `ICorDebugObjectValue` references.</span></span>|  
|[<span data-ttu-id="43479-110">GetContext 方法</span><span class="sxs-lookup"><span data-stu-id="43479-110">GetContext Method</span></span>](icordebugobjectvalue-getcontext-method.md)|<span data-ttu-id="43479-111">未实现。</span><span class="sxs-lookup"><span data-stu-id="43479-111">Not implemented.</span></span>|  
|[<span data-ttu-id="43479-112">GetFieldValue 方法</span><span class="sxs-lookup"><span data-stu-id="43479-112">GetFieldValue Method</span></span>](icordebugobjectvalue-getfieldvalue-method.md)|<span data-ttu-id="43479-113">获取一个指向 [ICorDebugValue](icordebugvalue-interface.md) 的接口指针，该指针表示指定类的指定字段的值。</span><span class="sxs-lookup"><span data-stu-id="43479-113">Gets an interface pointer to an [ICorDebugValue](icordebugvalue-interface.md) that represents the value of the specified field of the specified class.</span></span>|  
|[<span data-ttu-id="43479-114">GetManagedCopy 方法</span><span class="sxs-lookup"><span data-stu-id="43479-114">GetManagedCopy Method</span></span>](icordebugobjectvalue-getmanagedcopy-method.md)|<span data-ttu-id="43479-115">已过时。</span><span class="sxs-lookup"><span data-stu-id="43479-115">Obsolete.</span></span> <span data-ttu-id="43479-116">请勿调用此方法。</span><span class="sxs-lookup"><span data-stu-id="43479-116">Do not call this method.</span></span>|  
|[<span data-ttu-id="43479-117">GetVirtualMethod 方法</span><span class="sxs-lookup"><span data-stu-id="43479-117">GetVirtualMethod Method</span></span>](icordebugobjectvalue-getvirtualmethod-method.md)|<span data-ttu-id="43479-118">未实现。</span><span class="sxs-lookup"><span data-stu-id="43479-118">Not implemented.</span></span>|  
|[<span data-ttu-id="43479-119">IsValueClass 方法</span><span class="sxs-lookup"><span data-stu-id="43479-119">IsValueClass Method</span></span>](icordebugobjectvalue-isvalueclass-method.md)|<span data-ttu-id="43479-120">获取一个值，该值指示由此引用的对象是否 `ICorDebugObjectValue` 为值类型。</span><span class="sxs-lookup"><span data-stu-id="43479-120">Gets a value that indicates whether the object referenced by this `ICorDebugObjectValue` is a value type.</span></span>|  
|[<span data-ttu-id="43479-121">SetFromManagedCopy 方法</span><span class="sxs-lookup"><span data-stu-id="43479-121">SetFromManagedCopy Method</span></span>](icordebugobjectvalue-setfrommanagedcopy-method.md)|<span data-ttu-id="43479-122">已过时。</span><span class="sxs-lookup"><span data-stu-id="43479-122">Obsolete.</span></span> <span data-ttu-id="43479-123">请勿调用此方法。</span><span class="sxs-lookup"><span data-stu-id="43479-123">Do not call this method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="43479-124">备注</span><span class="sxs-lookup"><span data-stu-id="43479-124">Remarks</span></span>  

 <span data-ttu-id="43479-125">在 `ICorDebugObjectValue` 继续进行调试之前，将一直有效。</span><span class="sxs-lookup"><span data-stu-id="43479-125">An `ICorDebugObjectValue` remains valid until the process being debugged is continued.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="43479-126">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="43479-126">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="43479-127">要求</span><span class="sxs-lookup"><span data-stu-id="43479-127">Requirements</span></span>  

 <span data-ttu-id="43479-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="43479-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="43479-129">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="43479-129">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="43479-130">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="43479-130">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="43479-131">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="43479-131">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="43479-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="43479-132">See also</span></span>

- [<span data-ttu-id="43479-133">调试接口</span><span class="sxs-lookup"><span data-stu-id="43479-133">Debugging Interfaces</span></span>](debugging-interfaces.md)
