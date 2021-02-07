---
description: 了解详细信息： ICorDebugProcess 接口
title: ICorDebugProcess 接口
ms.date: 03/30/2017
api_name:
- ICorDebugProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess
helpviewer_keywords:
- ICorDebugProcess interface [.NET Framework debugging]
ms.assetid: be86f4b5-418a-4c5c-a67c-97148c65ed8c
topic_type:
- apiref
ms.openlocfilehash: 7172ee12bf450235db1c18601c8ff7de51435520
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746784"
---
# <a name="icordebugprocess-interface"></a><span data-ttu-id="7e31a-103">ICorDebugProcess 接口</span><span class="sxs-lookup"><span data-stu-id="7e31a-103">ICorDebugProcess Interface</span></span>

<span data-ttu-id="7e31a-104">表示正在执行托管代码的进程。</span><span class="sxs-lookup"><span data-stu-id="7e31a-104">Represents a process that is executing managed code.</span></span> <span data-ttu-id="7e31a-105">此接口是 ICorDebugController 的子类。</span><span class="sxs-lookup"><span data-stu-id="7e31a-105">This interface is a subclass of ICorDebugController.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7e31a-106">方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-106">Methods</span></span>  
  
|<span data-ttu-id="7e31a-107">方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-107">Method</span></span>|<span data-ttu-id="7e31a-108">说明</span><span class="sxs-lookup"><span data-stu-id="7e31a-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7e31a-109">ClearCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-109">ClearCurrentException Method</span></span>](icordebugprocess-clearcurrentexception-method.md)|<span data-ttu-id="7e31a-110">清除给定线程上的当前非托管异常。</span><span class="sxs-lookup"><span data-stu-id="7e31a-110">Clears the current unmanaged exception on the given thread.</span></span>|  
|[<span data-ttu-id="7e31a-111">EnableLogMessages 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-111">EnableLogMessages Method</span></span>](icordebugprocess-enablelogmessages-method.md)|<span data-ttu-id="7e31a-112">启用和禁用向调试器发送日志消息。</span><span class="sxs-lookup"><span data-stu-id="7e31a-112">Enables and disables the sending of log messages to the debugger.</span></span>|  
|[<span data-ttu-id="7e31a-113">EnumerateAppDomains 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-113">EnumerateAppDomains Method</span></span>](icordebugprocess-enumerateappdomains-method.md)|<span data-ttu-id="7e31a-114">枚举进程中的所有应用程序域。</span><span class="sxs-lookup"><span data-stu-id="7e31a-114">Enumerates all of the application domains in the process.</span></span>|  
|[<span data-ttu-id="7e31a-115">EnumerateObjects 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-115">EnumerateObjects Method</span></span>](icordebugprocess-enumerateobjects-method.md)|<span data-ttu-id="7e31a-116">未实现。</span><span class="sxs-lookup"><span data-stu-id="7e31a-116">Not implemented.</span></span>|  
|[<span data-ttu-id="7e31a-117">GetHandle 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-117">GetHandle Method</span></span>](icordebugprocess-gethandle-method.md)|<span data-ttu-id="7e31a-118">获取进程的句柄。</span><span class="sxs-lookup"><span data-stu-id="7e31a-118">Gets a handle to the process.</span></span>|  
|[<span data-ttu-id="7e31a-119">GetHelperThreadID 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-119">GetHelperThreadID Method</span></span>](icordebugprocess-gethelperthreadid-method.md)|<span data-ttu-id="7e31a-120">获取调试器的内部帮助器线程 (操作系统) 线程 ID。</span><span class="sxs-lookup"><span data-stu-id="7e31a-120">Gets the operating system (OS) thread ID for the debugger's internal helper thread.</span></span>|  
|[<span data-ttu-id="7e31a-121">GetID 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-121">GetID Method</span></span>](icordebugprocess-getid-method.md)|<span data-ttu-id="7e31a-122">获取进程的操作系统 (操作系统) ID。</span><span class="sxs-lookup"><span data-stu-id="7e31a-122">Gets the operating system (OS) ID of the process.</span></span>|  
|[<span data-ttu-id="7e31a-123">GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-123">GetObject Method</span></span>](icordebugprocess-getobject-method.md)|<span data-ttu-id="7e31a-124">未实现。</span><span class="sxs-lookup"><span data-stu-id="7e31a-124">Not implemented.</span></span>|  
|[<span data-ttu-id="7e31a-125">GetThread 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-125">GetThread Method</span></span>](icordebugprocess-getthread-method.md)|<span data-ttu-id="7e31a-126">获取具有指定 OS 线程 ID 的 ICorDebugThread 实例。</span><span class="sxs-lookup"><span data-stu-id="7e31a-126">Gets the ICorDebugThread instance that has the specified OS thread ID.</span></span>|  
|[<span data-ttu-id="7e31a-127">GetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-127">GetThreadContext Method</span></span>](icordebugprocess-getthreadcontext-method.md)|<span data-ttu-id="7e31a-128">获取给定线程的上下文。</span><span class="sxs-lookup"><span data-stu-id="7e31a-128">Gets the context for the given thread.</span></span>|  
|[<span data-ttu-id="7e31a-129">IsOSSuspended 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-129">IsOSSuspended Method</span></span>](icordebugprocess-isossuspended-method.md)|<span data-ttu-id="7e31a-130">确定线程是否由于调试器停止进程而挂起。</span><span class="sxs-lookup"><span data-stu-id="7e31a-130">Determines whether the thread has been suspended as a result of the debugger stopping the process.</span></span>|  
|[<span data-ttu-id="7e31a-131">IsTransitionStub 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-131">IsTransitionStub Method</span></span>](icordebugprocess-istransitionstub-method.md)|<span data-ttu-id="7e31a-132">确定地址是否在将导致转换到托管代码的存根内。</span><span class="sxs-lookup"><span data-stu-id="7e31a-132">Determines whether an address is inside a stub that will cause a transition to managed code.</span></span>|  
|[<span data-ttu-id="7e31a-133">ModifyLogSwitch 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-133">ModifyLogSwitch Method</span></span>](icordebugprocess-modifylogswitch-method.md)|<span data-ttu-id="7e31a-134">设置指定的日志开关的严重性级别。</span><span class="sxs-lookup"><span data-stu-id="7e31a-134">Sets the severity level of the specified log switch.</span></span>|  
|[<span data-ttu-id="7e31a-135">ReadMemory 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-135">ReadMemory Method</span></span>](icordebugprocess-readmemory-method.md)|<span data-ttu-id="7e31a-136">从进程读取内存。</span><span class="sxs-lookup"><span data-stu-id="7e31a-136">Reads memory from the process.</span></span>|  
|[<span data-ttu-id="7e31a-137">SetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-137">SetThreadContext Method</span></span>](icordebugprocess-setthreadcontext-method.md)|<span data-ttu-id="7e31a-138">设置给定线程的上下文。</span><span class="sxs-lookup"><span data-stu-id="7e31a-138">Sets the context for the given thread.</span></span>|  
|[<span data-ttu-id="7e31a-139">ThreadForFiberCookie 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-139">ThreadForFiberCookie Method</span></span>](icordebugprocess-threadforfibercookie-method.md)|<span data-ttu-id="7e31a-140">已弃用。</span><span class="sxs-lookup"><span data-stu-id="7e31a-140">Deprecated.</span></span>|  
|[<span data-ttu-id="7e31a-141">WriteMemory 方法</span><span class="sxs-lookup"><span data-stu-id="7e31a-141">WriteMemory Method</span></span>](icordebugprocess-writememory-method.md)|<span data-ttu-id="7e31a-142">将数据写入进程中的内存区域。</span><span class="sxs-lookup"><span data-stu-id="7e31a-142">Writes data to an area of memory in the process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7e31a-143">备注</span><span class="sxs-lookup"><span data-stu-id="7e31a-143">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7e31a-144">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="7e31a-144">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7e31a-145">要求</span><span class="sxs-lookup"><span data-stu-id="7e31a-145">Requirements</span></span>  

 <span data-ttu-id="7e31a-146">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7e31a-146">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7e31a-147">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7e31a-147">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7e31a-148">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7e31a-148">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7e31a-149">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7e31a-149">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e31a-150">请参阅</span><span class="sxs-lookup"><span data-stu-id="7e31a-150">See also</span></span>

- [<span data-ttu-id="7e31a-151">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="7e31a-151">ICorDebug Interface</span></span>](icordebug-interface.md)
- [<span data-ttu-id="7e31a-152">调试接口</span><span class="sxs-lookup"><span data-stu-id="7e31a-152">Debugging Interfaces</span></span>](debugging-interfaces.md)
