---
description: 了解详细信息： ICorDebugExceptionDebugEvent 接口
title: “ICor调试异常调试事件”接口
ms.date: 03/30/2017
ms.assetid: f9ba60d8-b54d-417e-bb3e-fde4b41ca44c
ms.openlocfilehash: eacaa344763fb77faef5f66282809d741f017b37
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693416"
---
# <a name="icordebugexceptiondebugevent-interface"></a><span data-ttu-id="a76d3-103">“ICor调试异常调试事件”接口</span><span class="sxs-lookup"><span data-stu-id="a76d3-103">ICorDebugExceptionDebugEvent Interface</span></span>

<span data-ttu-id="a76d3-104">扩展 [ICorDebugDebugEvent](icordebugdebugevent-interface.md) 接口以支持异常事件。</span><span class="sxs-lookup"><span data-stu-id="a76d3-104">Extends the [ICorDebugDebugEvent](icordebugdebugevent-interface.md) interface to support exception events.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a76d3-105">方法</span><span class="sxs-lookup"><span data-stu-id="a76d3-105">Methods</span></span>  
  
|<span data-ttu-id="a76d3-106">方法</span><span class="sxs-lookup"><span data-stu-id="a76d3-106">Method</span></span>|<span data-ttu-id="a76d3-107">说明</span><span class="sxs-lookup"><span data-stu-id="a76d3-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a76d3-108">GetFlags 方法</span><span class="sxs-lookup"><span data-stu-id="a76d3-108">GetFlags Method</span></span>](icordebugexceptiondebugevent-getflags-method.md)|<span data-ttu-id="a76d3-109">获取指示是否可拦截异常的标志。</span><span class="sxs-lookup"><span data-stu-id="a76d3-109">Gets a flag that indicates whether the exception is can be intercepted.</span></span>|  
|[<span data-ttu-id="a76d3-110">GetNativeIP 方法</span><span class="sxs-lookup"><span data-stu-id="a76d3-110">GetNativeIP Method</span></span>](icordebugexceptiondebugevent-getnativeip-method.md)|<span data-ttu-id="a76d3-111">获取此异常调试事件的本机接口指针。</span><span class="sxs-lookup"><span data-stu-id="a76d3-111">Gets the native interface pointer for this exception debug event.</span></span>|  
|[<span data-ttu-id="a76d3-112">GetStackPointer 方法</span><span class="sxs-lookup"><span data-stu-id="a76d3-112">GetStackPointer Method</span></span>](icordebugexceptiondebugevent-getstackpointer-method.md)|<span data-ttu-id="a76d3-113">获取此异常调试事件的堆栈指针。</span><span class="sxs-lookup"><span data-stu-id="a76d3-113">Gets the stack pointer for this exception debug event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a76d3-114">备注</span><span class="sxs-lookup"><span data-stu-id="a76d3-114">Remarks</span></span>  

 <span data-ttu-id="a76d3-115">`ICorDebugExceptionDebugEvent` 接口由以下事件类型实现：</span><span class="sxs-lookup"><span data-stu-id="a76d3-115">The `ICorDebugExceptionDebugEvent` interface is implemented by the following event types:</span></span>  
  
- [<span data-ttu-id="a76d3-116">MANAGED_EXCEPTION_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="a76d3-116">MANAGED_EXCEPTION_FIRST_CHANCE</span></span>](cordebugrecordformat-enumeration.md)  
  
- [<span data-ttu-id="a76d3-117">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="a76d3-117">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span></span>](cordebugrecordformat-enumeration.md)  
  
- [<span data-ttu-id="a76d3-118">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span><span class="sxs-lookup"><span data-stu-id="a76d3-118">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span></span>](cordebugrecordformat-enumeration.md)  
  
- [<span data-ttu-id="a76d3-119">MANAGED_EXCEPTION_UNHANDLED</span><span class="sxs-lookup"><span data-stu-id="a76d3-119">MANAGED_EXCEPTION_UNHANDLED</span></span>](cordebugrecordformat-enumeration.md)  
  
> [!NOTE]
> <span data-ttu-id="a76d3-120">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="a76d3-120">The interface is available with .NET Native only.</span></span> <span data-ttu-id="a76d3-121">尝试调用 `QueryInterface` 来检索接口指针会为 .NET Native 外部的 ICorDebug 方案返回 `E_NOINTERFACE`。</span><span class="sxs-lookup"><span data-stu-id="a76d3-121">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a76d3-122">要求</span><span class="sxs-lookup"><span data-stu-id="a76d3-122">Requirements</span></span>  

 <span data-ttu-id="a76d3-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a76d3-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a76d3-124">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a76d3-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a76d3-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a76d3-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a76d3-126">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a76d3-126">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a76d3-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="a76d3-127">See also</span></span>

- [<span data-ttu-id="a76d3-128">调试接口</span><span class="sxs-lookup"><span data-stu-id="a76d3-128">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="a76d3-129">调试</span><span class="sxs-lookup"><span data-stu-id="a76d3-129">Debugging</span></span>](index.md)
