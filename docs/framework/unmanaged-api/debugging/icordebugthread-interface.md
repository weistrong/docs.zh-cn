---
description: 了解详细信息： ICorDebugThread 接口
title: ICorDebugThread 接口
ms.date: 03/30/2017
api_name:
- ICorDebugThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread
helpviewer_keywords:
- ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 3930fd9b-2bc3-4b72-80a0-b6eeb94d60c6
topic_type:
- apiref
ms.openlocfilehash: 7e16fa2a82a004a5c85d60a278cdd14df6ab2300
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658823"
---
# <a name="icordebugthread-interface"></a><span data-ttu-id="17ecf-103">ICorDebugThread 接口</span><span class="sxs-lookup"><span data-stu-id="17ecf-103">ICorDebugThread Interface</span></span>

<span data-ttu-id="17ecf-104">表示进程中的线程。</span><span class="sxs-lookup"><span data-stu-id="17ecf-104">Represents a thread in a process.</span></span> <span data-ttu-id="17ecf-105">`ICorDebugThread` 实例的生存期与它表示的线程的生存期相同。</span><span class="sxs-lookup"><span data-stu-id="17ecf-105">The lifetime of an `ICorDebugThread` instance is the same as the lifetime of the thread it represents.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="17ecf-106">方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-106">Methods</span></span>  
  
|<span data-ttu-id="17ecf-107">方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-107">Method</span></span>|<span data-ttu-id="17ecf-108">说明</span><span class="sxs-lookup"><span data-stu-id="17ecf-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="17ecf-109">ClearCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-109">ClearCurrentException Method</span></span>](icordebugthread-clearcurrentexception-method.md)|<span data-ttu-id="17ecf-110">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="17ecf-110">This method is not implemented.</span></span> <span data-ttu-id="17ecf-111">请勿使用。</span><span class="sxs-lookup"><span data-stu-id="17ecf-111">Do not use it.</span></span>|  
|[<span data-ttu-id="17ecf-112">CreateEval 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-112">CreateEval Method</span></span>](icordebugthread-createeval-method.md)|<span data-ttu-id="17ecf-113">创建一个对此运行的 ICorDebugEval 对象 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-113">Creates an ICorDebugEval object that operates on this `ICorDebugThread`.</span></span>|  
|[<span data-ttu-id="17ecf-114">CreateStepper 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-114">CreateStepper Method</span></span>](icordebugthread-createstepper-method.md)|<span data-ttu-id="17ecf-115">创建一个 ICorDebugStepper 对象，该对象允许单步执行此中的活动框架 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-115">Creates an ICorDebugStepper object that allows stepping through the active frame in this `ICorDebugThread`.</span></span>|  
|[<span data-ttu-id="17ecf-116">EnumerateChains 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-116">EnumerateChains Method</span></span>](icordebugthread-enumeratechains-method.md)|<span data-ttu-id="17ecf-117">获取一个接口指针，该指针指向包含此中所有堆栈链的 ICorDebugChainEnum 枚举器 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-117">Gets an interface pointer to an ICorDebugChainEnum enumerator that contains all the stack chains in this `ICorDebugThread`.</span></span>|  
|[<span data-ttu-id="17ecf-118">GetActiveChain 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-118">GetActiveChain Method</span></span>](icordebugthread-getactivechain-method.md)|<span data-ttu-id="17ecf-119">获取此上的活动 ICorDebugChain 的接口指针 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-119">Gets an interface pointer to the active ICorDebugChain on this `ICorDebugThread`.</span></span>|  
|[<span data-ttu-id="17ecf-120">GetActiveFrame 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-120">GetActiveFrame Method</span></span>](icordebugthread-getactiveframe-method.md)|<span data-ttu-id="17ecf-121">获取此上的活动 ICorDebugFrame 的接口指针 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-121">Gets an interface pointer to the active ICorDebugFrame on this `ICorDebugThread`.</span></span>|  
|[<span data-ttu-id="17ecf-122">GetAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-122">GetAppDomain Method</span></span>](icordebugthread-getappdomain-method.md)|<span data-ttu-id="17ecf-123">获取一个接口指针，该指针指向此当前正在执行的应用程序域 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-123">Gets an interface pointer to the application domain in which this `ICorDebugThread` is currently executing.</span></span>|  
|[<span data-ttu-id="17ecf-124">GetCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-124">GetCurrentException Method</span></span>](icordebugthread-getcurrentexception-method.md)|<span data-ttu-id="17ecf-125">获取一个指向 ICorDebugValue 对象的接口指针，该对象表示当前由托管代码引发的异常。</span><span class="sxs-lookup"><span data-stu-id="17ecf-125">Gets an interface pointer to an ICorDebugValue object that represents an exception currently being thrown by managed code.</span></span>|  
|[<span data-ttu-id="17ecf-126">GetDebugState 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-126">GetDebugState Method</span></span>](icordebugthread-getdebugstate-method.md)|<span data-ttu-id="17ecf-127">获取描述此的当前调试状态的 CorDebugThreadState 值 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-127">Gets a CorDebugThreadState value that describes the current debug state of this `ICorDebugThread`.</span></span>|  
|[<span data-ttu-id="17ecf-128">GetHandle 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-128">GetHandle Method</span></span>](icordebugthread-gethandle-method.md)|<span data-ttu-id="17ecf-129">获取此的活动部分的当前句柄 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-129">Gets the current handle for the active part of this `ICorDebugThread`.</span></span>|  
|[<span data-ttu-id="17ecf-130">GetID 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-130">GetID Method</span></span>](icordebugthread-getid-method.md)|<span data-ttu-id="17ecf-131">获取此的活动部分的当前操作系统标识符 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-131">Gets the current operating system identifier of the active part of this `ICorDebugThread`.</span></span>|  
|[<span data-ttu-id="17ecf-132">GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-132">GetObject Method</span></span>](icordebugthread-getobject-method.md)|<span data-ttu-id="17ecf-133"> (CLR) 线程获取公共语言运行时的接口指针。</span><span class="sxs-lookup"><span data-stu-id="17ecf-133">Gets an interface pointer to the common language runtime (CLR) thread.</span></span>|  
|[<span data-ttu-id="17ecf-134">GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-134">GetProcess Method</span></span>](icordebugthread-getprocess-method.md)|<span data-ttu-id="17ecf-135">获取一个接口指针，该指针指向此 `ICorDebugThread` 构成部分的进程。</span><span class="sxs-lookup"><span data-stu-id="17ecf-135">Gets an interface pointer to the process of which this `ICorDebugThread` forms a part.</span></span>|  
|[<span data-ttu-id="17ecf-136">GetRegisterSet 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-136">GetRegisterSet Method</span></span>](icordebugthread-getregisterset-method.md)|<span data-ttu-id="17ecf-137">获取一个接口指针，该指针指向与此关联的寄存器集 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-137">Gets an interface pointer to the register set associated with this `ICorDebugThread`.</span></span>|  
|[<span data-ttu-id="17ecf-138">GetUserState 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-138">GetUserState Method</span></span>](icordebugthread-getuserstate-method.md)|<span data-ttu-id="17ecf-139">获取描述此的当前状态的 CorDebugUserState 值的按位组合 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-139">Gets a bitwise combination of CorDebugUserState values that describe the current state of this `ICorDebugThread`.</span></span>|  
|[<span data-ttu-id="17ecf-140">SetDebugState 方法</span><span class="sxs-lookup"><span data-stu-id="17ecf-140">SetDebugState Method</span></span>](icordebugthread-setdebugstate-method.md)|<span data-ttu-id="17ecf-141">设置 `CorDebugThreadState` 描述此的调试状态的值的按位组合 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="17ecf-141">Sets a bitwise combination of `CorDebugThreadState` values that describe the debugging state of this `ICorDebugThread`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="17ecf-142">备注</span><span class="sxs-lookup"><span data-stu-id="17ecf-142">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="17ecf-143">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="17ecf-143">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="17ecf-144">要求</span><span class="sxs-lookup"><span data-stu-id="17ecf-144">Requirements</span></span>  

 <span data-ttu-id="17ecf-145">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="17ecf-145">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="17ecf-146">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="17ecf-146">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="17ecf-147">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="17ecf-147">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="17ecf-148">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="17ecf-148">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="17ecf-149">请参阅</span><span class="sxs-lookup"><span data-stu-id="17ecf-149">See also</span></span>

- [<span data-ttu-id="17ecf-150">调试接口</span><span class="sxs-lookup"><span data-stu-id="17ecf-150">Debugging Interfaces</span></span>](debugging-interfaces.md)
