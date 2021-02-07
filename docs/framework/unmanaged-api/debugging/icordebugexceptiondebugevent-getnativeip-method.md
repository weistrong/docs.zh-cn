---
description: 了解详细信息： ICorDebugExceptionDebugEvent：： GetNativeIP 方法
title: ICorDebugExceptionDebugEvent::GetNativeIP 方法
ms.date: 03/30/2017
ms.assetid: 12e6a262-d9ac-49b8-9b80-1e653a2a3819
ms.openlocfilehash: 89bda36efc59e2462634c3d8a3a5835c9d4b3354
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693455"
---
# <a name="icordebugexceptiondebugeventgetnativeip-method"></a><span data-ttu-id="313a8-103">ICorDebugExceptionDebugEvent::GetNativeIP 方法</span><span class="sxs-lookup"><span data-stu-id="313a8-103">ICorDebugExceptionDebugEvent::GetNativeIP Method</span></span>

<span data-ttu-id="313a8-104">获取此异常调试事件的本机指令指针。</span><span class="sxs-lookup"><span data-stu-id="313a8-104">Gets the native instruction pointer for this exception debug event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="313a8-105">语法</span><span class="sxs-lookup"><span data-stu-id="313a8-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNativeIP(  
   [out]CORDB_ADDRESS *pIP  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="313a8-106">参数</span><span class="sxs-lookup"><span data-stu-id="313a8-106">Parameters</span></span>  

 `pIP`  
 <span data-ttu-id="313a8-107">[out] 指向此异常调试事件的指令指针的指针。</span><span class="sxs-lookup"><span data-stu-id="313a8-107">[out] A pointer to the instruction pointer for this exception debug event.</span></span> <span data-ttu-id="313a8-108">有关详细信息，请参阅备注部分。</span><span class="sxs-lookup"><span data-stu-id="313a8-108">See the Remarks section for more information.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="313a8-109">备注</span><span class="sxs-lookup"><span data-stu-id="313a8-109">Remarks</span></span>  

 <span data-ttu-id="313a8-110">此指令指针的含义取决于事件类型，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="313a8-110">The meaning of this instruction pointer depends on the event type, as shown in the following table.</span></span>  
  
|<span data-ttu-id="313a8-111">事件类型</span><span class="sxs-lookup"><span data-stu-id="313a8-111">Event type</span></span>|<span data-ttu-id="313a8-112">`pStackPointer` 值的含义</span><span class="sxs-lookup"><span data-stu-id="313a8-112">Meaning of `pStackPointer` value</span></span>|  
|----------------|--------------------------------------|  
|[<span data-ttu-id="313a8-113">MANAGED_EXCEPTION_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="313a8-113">MANAGED_EXCEPTION_FIRST_CHANCE</span></span>](cordebugrecordformat-enumeration.md)|<span data-ttu-id="313a8-114">出错指令的地址。</span><span class="sxs-lookup"><span data-stu-id="313a8-114">The address of the faulting instruction.</span></span>|  
|[<span data-ttu-id="313a8-115">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="313a8-115">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span></span>](cordebugrecordformat-enumeration.md)|<span data-ttu-id="313a8-116">[GetStackPointer](icordebugexceptiondebugevent-getstackpointer-method.md)方法指示的帧中的代码地址，如果未引发异常，则执行将继续执行。</span><span class="sxs-lookup"><span data-stu-id="313a8-116">The code address in the frame indicated by the [GetStackPointer](icordebugexceptiondebugevent-getstackpointer-method.md) method where execution would resume if no exception had been raised.</span></span> <span data-ttu-id="313a8-117">此异常可能会，也可能不会导致在此帧中执行的不同代码（例如，`try/catch/finally` 子句的 catch 块）。</span><span class="sxs-lookup"><span data-stu-id="313a8-117">The exception may or may not cause different code, such as the catch block of a `try/catch/finally` clause, to be executed in this frame.</span></span>|  
|[<span data-ttu-id="313a8-118">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span><span class="sxs-lookup"><span data-stu-id="313a8-118">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span></span>](cordebugrecordformat-enumeration.md)|<span data-ttu-id="313a8-119">`catch`处理程序执行将在[GetStackPointer](icordebugexceptiondebugevent-getstackpointer-method.md)方法指示的帧中开始的代码地址。</span><span class="sxs-lookup"><span data-stu-id="313a8-119">The code address where `catch` handler execution will start in the frame indicated by the [GetStackPointer](icordebugexceptiondebugevent-getstackpointer-method.md) method.</span></span>|  
|[<span data-ttu-id="313a8-120">MANAGED_EXCEPTION_UNHANDLED</span><span class="sxs-lookup"><span data-stu-id="313a8-120">MANAGED_EXCEPTION_UNHANDLED</span></span>](cordebugrecordformat-enumeration.md)|<span data-ttu-id="313a8-121">`pIP` 为 0。</span><span class="sxs-lookup"><span data-stu-id="313a8-121">`pIP` is 0.</span></span>|  
  
 <span data-ttu-id="313a8-122">可以从 [ICorDebugDebugEvent：： GetEventKind](icordebugdebugevent-geteventkind-method.md) 方法获取事件类型。</span><span class="sxs-lookup"><span data-stu-id="313a8-122">The event type is available from the [ICorDebugDebugEvent::GetEventKind](icordebugdebugevent-geteventkind-method.md) method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="313a8-123">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="313a8-123">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="313a8-124">要求</span><span class="sxs-lookup"><span data-stu-id="313a8-124">Requirements</span></span>  

 <span data-ttu-id="313a8-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="313a8-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="313a8-126">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="313a8-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="313a8-127">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="313a8-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="313a8-128">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="313a8-128">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="313a8-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="313a8-129">See also</span></span>

- [<span data-ttu-id="313a8-130">“ICor调试异常调试事件”接口</span><span class="sxs-lookup"><span data-stu-id="313a8-130">ICorDebugExceptionDebugEvent Interface</span></span>](icordebugexceptiondebugevent-interface.md)
- [<span data-ttu-id="313a8-131">调试接口</span><span class="sxs-lookup"><span data-stu-id="313a8-131">Debugging Interfaces</span></span>](debugging-interfaces.md)
