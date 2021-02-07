---
description: 了解详细信息： ICorDebugManagedCallback2 接口
title: ICorDebugManagedCallback2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2
helpviewer_keywords:
- ICorDebugManagedCallback2 interface [.NET Framework debugging]
ms.assetid: cf7b7cfa-1c4b-4d8c-be70-4f9ed15a788b
topic_type:
- apiref
ms.openlocfilehash: a6a5b05479ea0f9e2d86f7c0ce42f5edd35bcb7a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691752"
---
# <a name="icordebugmanagedcallback2-interface"></a><span data-ttu-id="dd737-103">ICorDebugManagedCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="dd737-103">ICorDebugManagedCallback2 Interface</span></span>

<span data-ttu-id="dd737-104">提供支持调试器异常处理和托管调试助手 (MDA) 的方法。</span><span class="sxs-lookup"><span data-stu-id="dd737-104">Provides methods to support debugger exception handling and managed debugging assistants (MDAs).</span></span> <span data-ttu-id="dd737-105">`ICorDebugManagedCallback2` 是 [ICorDebugManagedCallback](icordebugmanagedcallback-interface.md) 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="dd737-105">`ICorDebugManagedCallback2` is a logical extension of the [ICorDebugManagedCallback](icordebugmanagedcallback-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="dd737-106">方法</span><span class="sxs-lookup"><span data-stu-id="dd737-106">Methods</span></span>  
  
|<span data-ttu-id="dd737-107">方法</span><span class="sxs-lookup"><span data-stu-id="dd737-107">Method</span></span>|<span data-ttu-id="dd737-108">说明</span><span class="sxs-lookup"><span data-stu-id="dd737-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="dd737-109">ChangeConnection 方法</span><span class="sxs-lookup"><span data-stu-id="dd737-109">ChangeConnection Method</span></span>](icordebugmanagedcallback2-changeconnection-method.md)|<span data-ttu-id="dd737-110">通知调试器与指定连接关联的任务集已更改。</span><span class="sxs-lookup"><span data-stu-id="dd737-110">Notifies the debugger that the set of tasks associated with the specified connection has changed.</span></span>|  
|[<span data-ttu-id="dd737-111">CreateConnection 方法</span><span class="sxs-lookup"><span data-stu-id="dd737-111">CreateConnection Method</span></span>](icordebugmanagedcallback2-createconnection-method.md)|<span data-ttu-id="dd737-112">通知调试器已创建新连接。</span><span class="sxs-lookup"><span data-stu-id="dd737-112">Notifies the debugger that a new connection has been created.</span></span>|  
|[<span data-ttu-id="dd737-113">DestroyConnection 方法</span><span class="sxs-lookup"><span data-stu-id="dd737-113">DestroyConnection Method</span></span>](icordebugmanagedcallback2-destroyconnection-method.md)|<span data-ttu-id="dd737-114">通知调试器指定的连接已终止。</span><span class="sxs-lookup"><span data-stu-id="dd737-114">Notifies the debugger that the specified connection has been terminated.</span></span>|  
|[<span data-ttu-id="dd737-115">Exception 方法</span><span class="sxs-lookup"><span data-stu-id="dd737-115">Exception Method</span></span>](icordebugmanagedcallback2-exception-method.md)|<span data-ttu-id="dd737-116">通知调试器已开始搜索异常处理程序。</span><span class="sxs-lookup"><span data-stu-id="dd737-116">Notifies the debugger that a search for an exception handler has started.</span></span>|  
|[<span data-ttu-id="dd737-117">ExceptionUnwind 方法</span><span class="sxs-lookup"><span data-stu-id="dd737-117">ExceptionUnwind Method</span></span>](icordebugmanagedcallback2-exceptionunwind-method.md)|<span data-ttu-id="dd737-118">在异常展开过程中提供状态通知。</span><span class="sxs-lookup"><span data-stu-id="dd737-118">Provides a status notification during the exception unwinding process.</span></span>|  
|[<span data-ttu-id="dd737-119">FunctionRemapComplete 方法</span><span class="sxs-lookup"><span data-stu-id="dd737-119">FunctionRemapComplete Method</span></span>](icordebugmanagedcallback2-functionremapcomplete-method.md)|<span data-ttu-id="dd737-120">通知调试器，代码执行已切换到已编辑函数的新版本。</span><span class="sxs-lookup"><span data-stu-id="dd737-120">Notifies the debugger that code execution has switched to a new version of an edited function.</span></span>|  
|[<span data-ttu-id="dd737-121">FunctionRemapOpportunity 方法</span><span class="sxs-lookup"><span data-stu-id="dd737-121">FunctionRemapOpportunity Method</span></span>](icordebugmanagedcallback2-functionremapopportunity-method.md)|<span data-ttu-id="dd737-122">通知调试程序代码执行已到达已编辑函数的较早版本中的序列点。</span><span class="sxs-lookup"><span data-stu-id="dd737-122">Notifies the debugger that code execution has reached a sequence point in an older version of an edited function.</span></span>|  
|[<span data-ttu-id="dd737-123">MDANotification 方法</span><span class="sxs-lookup"><span data-stu-id="dd737-123">MDANotification Method</span></span>](icordebugmanagedcallback2-mdanotification-method.md)|<span data-ttu-id="dd737-124">提供通知，指出代码执行 (MDA) 消息中发生了托管调试助手。</span><span class="sxs-lookup"><span data-stu-id="dd737-124">Provides notification that code execution has encountered a managed debugging assistant (MDA) message.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dd737-125">备注</span><span class="sxs-lookup"><span data-stu-id="dd737-125">Remarks</span></span>  

 <span data-ttu-id="dd737-126">`ICorDebugManagedCallback2`接口扩展 `ICorDebugManagedCallback` 接口以处理 .NET Framework 版本2.0 中引入的新调试事件。</span><span class="sxs-lookup"><span data-stu-id="dd737-126">The `ICorDebugManagedCallback2` interface extends the `ICorDebugManagedCallback` interface to handle new debug events introduced in the .NET Framework version 2.0.</span></span>  
  
 <span data-ttu-id="dd737-127">调试程序在 `ICorDebugManagedCallback2` 调试 .NET Framework 2.0 应用程序时必须实现。</span><span class="sxs-lookup"><span data-stu-id="dd737-127">A debugger must implement `ICorDebugManagedCallback2` if it is debugging .NET Framework 2.0 applications.</span></span> <span data-ttu-id="dd737-128">或的实例 `ICorDebugManagedCallback` `ICorDebugManagedCallback2` 作为回调对象传递给 [ICorDebug：： SetManagedHandler](icordebug-setmanagedhandler-method.md)。</span><span class="sxs-lookup"><span data-stu-id="dd737-128">An instance of `ICorDebugManagedCallback` or `ICorDebugManagedCallback2` is passed as the callback object to [ICorDebug::SetManagedHandler](icordebug-setmanagedhandler-method.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="dd737-129">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="dd737-129">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dd737-130">要求</span><span class="sxs-lookup"><span data-stu-id="dd737-130">Requirements</span></span>  

 <span data-ttu-id="dd737-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dd737-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dd737-132">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="dd737-132">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="dd737-133">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dd737-133">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dd737-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dd737-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd737-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="dd737-135">See also</span></span>

- [<span data-ttu-id="dd737-136">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="dd737-136">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [<span data-ttu-id="dd737-137">调试接口</span><span class="sxs-lookup"><span data-stu-id="dd737-137">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="dd737-138">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="dd737-138">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
