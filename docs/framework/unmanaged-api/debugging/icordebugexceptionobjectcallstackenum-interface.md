---
description: 了解详细信息： ICorDebugExceptionObjectCallStackEnum 接口
title: ICorDebugExceptionObjectCallStackEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugExceptionObjectCallStackEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugExceptionObjectCallStackEnum
helpviewer_keywords:
- ICorDebugExceptionObjectCallStackEnum interface [.NET Framework debugging]
ms.assetid: 39dffa18-c71b-48c4-b11d-e814631ab1e9
topic_type:
- apiref
ms.openlocfilehash: c72f4299bf3ebc5de2d2ed196801d93ff5fe4356
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693351"
---
# <a name="icordebugexceptionobjectcallstackenum-interface"></a><span data-ttu-id="b5934-103">ICorDebugExceptionObjectCallStackEnum 接口</span><span class="sxs-lookup"><span data-stu-id="b5934-103">ICorDebugExceptionObjectCallStackEnum Interface</span></span>

<span data-ttu-id="b5934-104">为嵌入在异常对象中的调用堆栈信息提供枚举器。</span><span class="sxs-lookup"><span data-stu-id="b5934-104">Provides an enumerator for call stack information that is embedded in an exception object.</span></span> <span data-ttu-id="b5934-105">此接口是 ICorDebugEnum 接口的子类。</span><span class="sxs-lookup"><span data-stu-id="b5934-105">This interface is a subclass of the ICorDebugEnum interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b5934-106">方法</span><span class="sxs-lookup"><span data-stu-id="b5934-106">Methods</span></span>  
  
|<span data-ttu-id="b5934-107">方法</span><span class="sxs-lookup"><span data-stu-id="b5934-107">Method</span></span>|<span data-ttu-id="b5934-108">说明</span><span class="sxs-lookup"><span data-stu-id="b5934-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b5934-109">ICorDebugExceptionObjectCallStackEnum：： Next</span><span class="sxs-lookup"><span data-stu-id="b5934-109">ICorDebugExceptionObjectCallStackEnum::Next</span></span>](icordebugexceptionobjectcallstackenum-next-method.md)|<span data-ttu-id="b5934-110">获取指定数量的 [CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md) 对象，这些对象包含有关异常对象的调用堆栈的信息。</span><span class="sxs-lookup"><span data-stu-id="b5934-110">Gets a specified number of [CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md) objects that contain information about an exception object's call stack.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b5934-111">备注</span><span class="sxs-lookup"><span data-stu-id="b5934-111">Remarks</span></span>  

 <span data-ttu-id="b5934-112">`ICorDebugExceptionObjectCallStackEnum`接口实现 ICorDebugEnum 接口。</span><span class="sxs-lookup"><span data-stu-id="b5934-112">The `ICorDebugExceptionObjectCallStackEnum` interface implements the ICorDebugEnum interface.</span></span>  
  
 <span data-ttu-id="b5934-113">`ICorDebugExceptionObjectCallStackEnum`实例通过调用[ICorDebugExceptionObjectValue：： EnumerateExceptionCallStack](icordebugexceptionobjectvalue-enumerateexceptioncallstack-method.md)方法填充[CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md)对象。</span><span class="sxs-lookup"><span data-stu-id="b5934-113">An `ICorDebugExceptionObjectCallStackEnum` instance is populated with [CorDebugExceptionObjectStackFrame](cordebugexceptionobjectstackframe-structure.md) objects by calling the [ICorDebugExceptionObjectValue::EnumerateExceptionCallStack](icordebugexceptionobjectvalue-enumerateexceptioncallstack-method.md) method.</span></span> <span data-ttu-id="b5934-114">可以通过调用 [ICorDebugExceptionObjectCallStackEnum：： Next](icordebugexceptionobjectcallstackenum-next-method.md) 方法枚举集合中的调用堆栈项</span><span class="sxs-lookup"><span data-stu-id="b5934-114">The call stack items in the collection can be enumerated by calling the [ICorDebugExceptionObjectCallStackEnum::Next](icordebugexceptionobjectcallstackenum-next-method.md) method</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b5934-115">要求</span><span class="sxs-lookup"><span data-stu-id="b5934-115">Requirements</span></span>  

 <span data-ttu-id="b5934-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b5934-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b5934-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b5934-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b5934-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b5934-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b5934-119">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b5934-119">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5934-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="b5934-120">See also</span></span>

- [<span data-ttu-id="b5934-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="b5934-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="b5934-122">调试</span><span class="sxs-lookup"><span data-stu-id="b5934-122">Debugging</span></span>](index.md)
