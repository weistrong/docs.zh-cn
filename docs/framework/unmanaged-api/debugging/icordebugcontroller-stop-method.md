---
description: 了解详细信息： ICorDebugController：： Stop 方法
title: ICorDebugController::Stop 方法
ms.date: 03/30/2017
api_name:
- ICorDebugController.Stop
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Stop
helpviewer_keywords:
- Stop method, ICorDebugController interface [.NET Framework debugging]
- ICorDebugController::Stop method [.NET Framework debugging]
ms.assetid: c34e79be-a7fb-479e-8dec-d126a4c330e5
topic_type:
- apiref
ms.openlocfilehash: 613fd81a03114580ae3d826a94d855023895b694
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764601"
---
# <a name="icordebugcontrollerstop-method"></a><span data-ttu-id="2cb7e-103">ICorDebugController::Stop 方法</span><span class="sxs-lookup"><span data-stu-id="2cb7e-103">ICorDebugController::Stop Method</span></span>

<span data-ttu-id="2cb7e-104">在进程中运行托管代码的所有线程上执行协作停止。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-104">Performs a cooperative stop on all threads that are running managed code in the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2cb7e-105">语法</span><span class="sxs-lookup"><span data-stu-id="2cb7e-105">Syntax</span></span>  
  
```cpp  
HRESULT Stop (  
    [in] DWORD dwTimeoutIgnored  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2cb7e-106">参数</span><span class="sxs-lookup"><span data-stu-id="2cb7e-106">Parameters</span></span>  

 `dwTimeoutIgnored`  
 <span data-ttu-id="2cb7e-107">未使用。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-107">Not used.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2cb7e-108">备注</span><span class="sxs-lookup"><span data-stu-id="2cb7e-108">Remarks</span></span>  

 <span data-ttu-id="2cb7e-109">`Stop` 在进程中运行托管代码的所有线程上执行协作停止。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-109">`Stop` performs a cooperative stop on all threads running managed code in the process.</span></span> <span data-ttu-id="2cb7e-110">在仅限托管的调试会话期间，非托管线程可能会继续运行 (但在尝试调用托管代码) 时将被阻止。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-110">During a managed-only debugging session, unmanaged threads may continue to run (but will be blocked when trying to call managed code).</span></span> <span data-ttu-id="2cb7e-111">在互操作调试会话期间，也将停止非托管线程。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-111">During an interop debugging session, unmanaged threads will also be stopped.</span></span> <span data-ttu-id="2cb7e-112">`dwTimeoutIgnored`该值当前被忽略，并被视为无限 (-1) 。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-112">The `dwTimeoutIgnored` value is currently ignored and treated as INFINITE (-1).</span></span> <span data-ttu-id="2cb7e-113">如果协作式停止由于死锁而失败，则所有线程都将被挂起并返回 E_TIMEOUT。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-113">If the cooperative stop fails due to a deadlock, all threads are suspended and E_TIMEOUT is returned.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="2cb7e-114">`Stop` 是调试 API 中唯一的同步方法。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-114">`Stop` is the only synchronous method in the debugging API.</span></span> <span data-ttu-id="2cb7e-115">如果 `Stop` 返回 S_OK，则停止该进程。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-115">When `Stop` returns S_OK, the process is stopped.</span></span> <span data-ttu-id="2cb7e-116">不会提供回调以通知侦听器停止。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-116">No callback is given to notify listeners of the stop.</span></span> <span data-ttu-id="2cb7e-117">调试器必须调用 [ICorDebugController：： Continue](icordebugcontroller-continue-method.md) 以允许进程恢复。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-117">The debugger must call [ICorDebugController::Continue](icordebugcontroller-continue-method.md) to allow the process to resume.</span></span>  
  
 <span data-ttu-id="2cb7e-118">调试器维护一个停止计数器。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-118">The debugger maintains a stop counter.</span></span> <span data-ttu-id="2cb7e-119">当计数器变为零时，控制器会恢复。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-119">When the counter goes to zero, the controller is resumed.</span></span> <span data-ttu-id="2cb7e-120">每次调用 `Stop` 或每个调度回调都会递增计数器。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-120">Each call to `Stop` or each dispatched callback increments the counter.</span></span> <span data-ttu-id="2cb7e-121">每次调用都会 `ICorDebugController::Continue` 递减计数器。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-121">Each call to `ICorDebugController::Continue` decrements the counter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2cb7e-122">要求</span><span class="sxs-lookup"><span data-stu-id="2cb7e-122">Requirements</span></span>  

 <span data-ttu-id="2cb7e-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2cb7e-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2cb7e-124">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2cb7e-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2cb7e-125">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2cb7e-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2cb7e-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2cb7e-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2cb7e-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="2cb7e-127">See also</span></span>
