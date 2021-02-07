---
description: 了解详细信息： ICorDebugGenericValue 接口
title: ICorDebugGenericValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugGenericValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGenericValue
helpviewer_keywords:
- ICorDebugGenericValue interface [.NET Framework debugging]
ms.assetid: bc14f408-b359-4c8c-ade2-888ccdf7261b
topic_type:
- apiref
ms.openlocfilehash: 7c81855849d7b72bc509d20072b96bb64f5d395a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692025"
---
# <a name="icordebuggenericvalue-interface"></a><span data-ttu-id="4331c-103">ICorDebugGenericValue 接口</span><span class="sxs-lookup"><span data-stu-id="4331c-103">ICorDebugGenericValue Interface</span></span>

<span data-ttu-id="4331c-104">"ICorDebugValue" 的子类，适用于所有值。</span><span class="sxs-lookup"><span data-stu-id="4331c-104">A subclass of "ICorDebugValue" that applies to all values.</span></span> <span data-ttu-id="4331c-105">此接口可为值提供 Get 和 Set 方法。</span><span class="sxs-lookup"><span data-stu-id="4331c-105">This interface provides Get and Set methods for the value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4331c-106">方法</span><span class="sxs-lookup"><span data-stu-id="4331c-106">Methods</span></span>  
  
|<span data-ttu-id="4331c-107">方法</span><span class="sxs-lookup"><span data-stu-id="4331c-107">Method</span></span>|<span data-ttu-id="4331c-108">说明</span><span class="sxs-lookup"><span data-stu-id="4331c-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4331c-109">GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="4331c-109">GetValue Method</span></span>](icordebuggenericvalue-getvalue-method.md)|<span data-ttu-id="4331c-110">将值复制到指定的缓冲区中。</span><span class="sxs-lookup"><span data-stu-id="4331c-110">Copies the value into the specified buffer.</span></span>|  
|[<span data-ttu-id="4331c-111">SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="4331c-111">SetValue Method</span></span>](icordebuggenericvalue-setvalue-method.md)|<span data-ttu-id="4331c-112">从指定的缓冲区复制新值。</span><span class="sxs-lookup"><span data-stu-id="4331c-112">Copies a new value from the specified buffer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4331c-113">备注</span><span class="sxs-lookup"><span data-stu-id="4331c-113">Remarks</span></span>  

 <span data-ttu-id="4331c-114">`ICorDebugGenericValue` 是子接口，因为它是不可远程处理的。</span><span class="sxs-lookup"><span data-stu-id="4331c-114">`ICorDebugGenericValue` is a sub-interface because it is non-remotable.</span></span>  
  
 <span data-ttu-id="4331c-115">对于引用类型，该值是引用而不是引用的内容。</span><span class="sxs-lookup"><span data-stu-id="4331c-115">For reference types, the value is the reference rather than the contents of the reference.</span></span>  
  
 <span data-ttu-id="4331c-116">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="4331c-116">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="4331c-117">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="4331c-117">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4331c-118">要求</span><span class="sxs-lookup"><span data-stu-id="4331c-118">Requirements</span></span>  

 <span data-ttu-id="4331c-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4331c-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4331c-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4331c-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4331c-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4331c-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4331c-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4331c-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4331c-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="4331c-123">See also</span></span>

- [<span data-ttu-id="4331c-124">调试接口</span><span class="sxs-lookup"><span data-stu-id="4331c-124">Debugging Interfaces</span></span>](debugging-interfaces.md)
