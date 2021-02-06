---
description: 了解详细信息： ICorDebugManagedCallback2：： MDANotification 方法
title: ICorDebugManagedCallback2::MDANotification 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.MDANotification
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::MDANotification
helpviewer_keywords:
- MDANotification method [.NET Framework debugging]
- ICorDebugManagedCallback2::MDANotification method [.NET Framework debugging]
ms.assetid: 93f79627-bd31-4f4f-b95d-46a032a52fe4
topic_type:
- apiref
ms.openlocfilehash: 3f0c69c13ec30e604e07c284adca05f86283a5cd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650490"
---
# <a name="icordebugmanagedcallback2mdanotification-method"></a><span data-ttu-id="ffe37-103">ICorDebugManagedCallback2::MDANotification 方法</span><span class="sxs-lookup"><span data-stu-id="ffe37-103">ICorDebugManagedCallback2::MDANotification Method</span></span>

<span data-ttu-id="ffe37-104">提供通知，指出代码执行在要调试的应用程序中遇到了托管调试助手 (MDA) 。</span><span class="sxs-lookup"><span data-stu-id="ffe37-104">Provides notification that code execution has encountered a managed debugging assistant (MDA) in the application that is being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ffe37-105">语法</span><span class="sxs-lookup"><span data-stu-id="ffe37-105">Syntax</span></span>  
  
```cpp  
HRESULT MDANotification(  
    [in] ICorDebugController  *pController,  
    [in] ICorDebugThread      *pThread,  
    [in] ICorDebugMDA         *pMDA  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ffe37-106">参数</span><span class="sxs-lookup"><span data-stu-id="ffe37-106">Parameters</span></span>  

 `pController`  
 <span data-ttu-id="ffe37-107">中指向 ICorDebugController 接口的指针，该接口公开发生 MDA 的进程或应用程序域。</span><span class="sxs-lookup"><span data-stu-id="ffe37-107">[in] A pointer to an ICorDebugController interface that exposes the process or application domain in which the MDA occurred.</span></span>  
  
 <span data-ttu-id="ffe37-108">调试器不应对控制器是进程还是应用程序域作出任何假设，尽管它可以始终查询接口来做出决定。</span><span class="sxs-lookup"><span data-stu-id="ffe37-108">A debugger should not make any assumptions about whether the controller is a process or an application domain, although it can always query the interface to make a determination.</span></span>  
  
 `pThread`  
 <span data-ttu-id="ffe37-109">中指向 ICorDebugThread 接口的指针，该接口公开发生调试事件的托管线程。</span><span class="sxs-lookup"><span data-stu-id="ffe37-109">[in] A pointer to an ICorDebugThread interface that exposes the managed thread on which the debug event occurred.</span></span>  
  
 <span data-ttu-id="ffe37-110">如果在非托管线程上发生 MDA，则的值 `pThread` 将为 null。</span><span class="sxs-lookup"><span data-stu-id="ffe37-110">If the MDA occurred on an unmanaged thread, the value of `pThread` will be null.</span></span>  
  
 <span data-ttu-id="ffe37-111">必须从 MDA 对象本身中获取操作系统 (操作系统) 线程 ID。</span><span class="sxs-lookup"><span data-stu-id="ffe37-111">You must get the operating system (OS) thread ID from the MDA object itself.</span></span>  
  
 `pMDA`  
 <span data-ttu-id="ffe37-112">中指向公开 MDA 信息的 [ICorDebugMDA](icordebugmda-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="ffe37-112">[in] A pointer to an [ICorDebugMDA](icordebugmda-interface.md) interface that exposes the MDA information.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ffe37-113">备注</span><span class="sxs-lookup"><span data-stu-id="ffe37-113">Remarks</span></span>  

 <span data-ttu-id="ffe37-114">MDA 是启发式警告，不需要任何显式调试器操作，只需调用 [ICorDebugController：： Continue 继续](icordebugcontroller-continue-method.md) 执行正在调试的应用程序。</span><span class="sxs-lookup"><span data-stu-id="ffe37-114">An MDA is a heuristic warning and does not require any explicit debugger action except for calling [ICorDebugController::Continue](icordebugcontroller-continue-method.md) to resume execution of the application that is being debugged.</span></span>  
  
 <span data-ttu-id="ffe37-115">公共语言运行时 (CLR) 可以确定哪些 Mda 被激发，哪些数据在任意时间点处于任意给定的 MDA。</span><span class="sxs-lookup"><span data-stu-id="ffe37-115">The common language runtime (CLR) can determine which MDAs are fired and which data is in any given MDA at any point.</span></span> <span data-ttu-id="ffe37-116">因此，调试器不应生成需要特定 MDA 模式的任何功能。</span><span class="sxs-lookup"><span data-stu-id="ffe37-116">Therefore, debuggers should not build any functionality requiring specific MDA patterns.</span></span>  
  
 <span data-ttu-id="ffe37-117">Mda 可以排队，并在遇到 MDA 之后立即触发。</span><span class="sxs-lookup"><span data-stu-id="ffe37-117">MDAs may be queued and fired shortly after the MDA is encountered.</span></span> <span data-ttu-id="ffe37-118">如果运行时需要等待到一个安全点来激发 MDA，则会发生这种情况，而不是在遇到 MDA 时激发 MDA。</span><span class="sxs-lookup"><span data-stu-id="ffe37-118">This could happen if the runtime needs to wait until it reaches a safe point for firing the MDA, instead of firing the MDA when it encounters it.</span></span> <span data-ttu-id="ffe37-119">这也意味着，运行时可能会在一组排队的回调中引发许多 Mda， (类似于) 的 "附加" 事件操作。</span><span class="sxs-lookup"><span data-stu-id="ffe37-119">It also means that the runtime may fire a number of MDAs in a single set of queued callbacks (similar to an "attach" event operation).</span></span>  
  
 <span data-ttu-id="ffe37-120">调试器应在 `ICorDebugMDA` 从回调返回后立即释放对实例的引用 `MDANotification` ，以允许 CLR 回收 MDA 使用的内存。</span><span class="sxs-lookup"><span data-stu-id="ffe37-120">A debugger should release the reference to an `ICorDebugMDA` instance immediately after returning from the `MDANotification` callback, to allow the CLR to recycle the memory consumed by an MDA.</span></span> <span data-ttu-id="ffe37-121">如果激发多个 Mda，则释放实例可以提高性能。</span><span class="sxs-lookup"><span data-stu-id="ffe37-121">Releasing the instance may improve performance if many MDAs are firing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ffe37-122">要求</span><span class="sxs-lookup"><span data-stu-id="ffe37-122">Requirements</span></span>  

 <span data-ttu-id="ffe37-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ffe37-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ffe37-124">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ffe37-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ffe37-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ffe37-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ffe37-126">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ffe37-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ffe37-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="ffe37-127">See also</span></span>

- [<span data-ttu-id="ffe37-128">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="ffe37-128">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [<span data-ttu-id="ffe37-129">ICorDebugManagedCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="ffe37-129">ICorDebugManagedCallback2 Interface</span></span>](icordebugmanagedcallback2-interface.md)
- [<span data-ttu-id="ffe37-130">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="ffe37-130">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
