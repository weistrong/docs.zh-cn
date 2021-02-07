---
description: 了解详细信息： ICorDebugExceptionDebugEvent：： GetStackPointer 方法
title: ICorDebugExceptionDebugEvent::GetStackPointer 方法
ms.date: 03/30/2017
ms.assetid: d8f66a1c-16be-4264-afc5-bc2dfbb4a682
ms.openlocfilehash: 5a62a5eb54fff1e94beebc222e3f18cc4655040f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693442"
---
# <a name="icordebugexceptiondebugeventgetstackpointer-method"></a><span data-ttu-id="f555a-103">ICorDebugExceptionDebugEvent::GetStackPointer 方法</span><span class="sxs-lookup"><span data-stu-id="f555a-103">ICorDebugExceptionDebugEvent::GetStackPointer Method</span></span>

<span data-ttu-id="f555a-104">获取此异常调试事件的堆栈指针。</span><span class="sxs-lookup"><span data-stu-id="f555a-104">Gets the stack pointer for this exception debug event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f555a-105">语法</span><span class="sxs-lookup"><span data-stu-id="f555a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStackPointer(  
   [out]CORDB_ADDRESS *pStackPointer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f555a-106">参数</span><span class="sxs-lookup"><span data-stu-id="f555a-106">Parameters</span></span>  

 `pStackPointer`  
 <span data-ttu-id="f555a-107">[out] 指向此异常调试事件的堆栈指针的地址的指针。</span><span class="sxs-lookup"><span data-stu-id="f555a-107">[out] A pointer to the address of the stack pointer for this exception debug event.</span></span> <span data-ttu-id="f555a-108">有关详细信息，请参阅备注部分。</span><span class="sxs-lookup"><span data-stu-id="f555a-108">See the Remarks section for more information.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f555a-109">备注</span><span class="sxs-lookup"><span data-stu-id="f555a-109">Remarks</span></span>  

 <span data-ttu-id="f555a-110">此堆栈指针的含义取决于事件类型，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="f555a-110">The meaning of this stack pointer depends on the event type, as shown in the following table.</span></span>  
  
|<span data-ttu-id="f555a-111">事件类型</span><span class="sxs-lookup"><span data-stu-id="f555a-111">Event type</span></span>|<span data-ttu-id="f555a-112">`pStackPointer` 值的含义</span><span class="sxs-lookup"><span data-stu-id="f555a-112">Meaning of `pStackPointer` value</span></span>|  
|----------------|--------------------------------------|  
|[<span data-ttu-id="f555a-113">MANAGED_EXCEPTION_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="f555a-113">MANAGED_EXCEPTION_FIRST_CHANCE</span></span>](cordebugrecordformat-enumeration.md)|<span data-ttu-id="f555a-114">引发异常的帧的堆栈指针。</span><span class="sxs-lookup"><span data-stu-id="f555a-114">The stack pointer for the frame that threw the exception.</span></span>|  
|[<span data-ttu-id="f555a-115">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="f555a-115">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span></span>](cordebugrecordformat-enumeration.md)|<span data-ttu-id="f555a-116">与引发的异常点最接近的用户代码帧的堆栈指针。</span><span class="sxs-lookup"><span data-stu-id="f555a-116">The stack pointer for the user-code frame closest to the point of the thrown exception.</span></span>|  
|[<span data-ttu-id="f555a-117">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span><span class="sxs-lookup"><span data-stu-id="f555a-117">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span></span>](cordebugrecordformat-enumeration.md)|<span data-ttu-id="f555a-118">包含 catch 处理程序的帧的堆栈指针。</span><span class="sxs-lookup"><span data-stu-id="f555a-118">The stack pointer for the frame that contains the catch handler.</span></span>|  
|[<span data-ttu-id="f555a-119">MANAGED_EXCEPTION_UNHANDLED</span><span class="sxs-lookup"><span data-stu-id="f555a-119">MANAGED_EXCEPTION_UNHANDLED</span></span>](cordebugrecordformat-enumeration.md)|<span data-ttu-id="f555a-120">`pStackPointer` 为 null。</span><span class="sxs-lookup"><span data-stu-id="f555a-120">`pStackPointer` is **null**.</span></span>|  
  
> [!NOTE]
> <span data-ttu-id="f555a-121">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="f555a-121">This method is available with .NET Native only.</span></span>  
  
 <span data-ttu-id="f555a-122">可以从 [ICorDebugDebugEvent：： GetEventKind](icordebugdebugevent-geteventkind-method.md) 方法获取事件类型。</span><span class="sxs-lookup"><span data-stu-id="f555a-122">The event type is available from the [ICorDebugDebugEvent::GetEventKind](icordebugdebugevent-geteventkind-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f555a-123">要求</span><span class="sxs-lookup"><span data-stu-id="f555a-123">Requirements</span></span>  

 <span data-ttu-id="f555a-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f555a-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f555a-125">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f555a-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f555a-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f555a-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f555a-127">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f555a-127">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f555a-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="f555a-128">See also</span></span>

- [<span data-ttu-id="f555a-129">“ICor调试异常调试事件”接口</span><span class="sxs-lookup"><span data-stu-id="f555a-129">ICorDebugExceptionDebugEvent Interface</span></span>](icordebugexceptiondebugevent-interface.md)
- [<span data-ttu-id="f555a-130">调试接口</span><span class="sxs-lookup"><span data-stu-id="f555a-130">Debugging Interfaces</span></span>](debugging-interfaces.md)
