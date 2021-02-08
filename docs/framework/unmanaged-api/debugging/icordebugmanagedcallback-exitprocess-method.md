---
description: 了解详细信息： ICorDebugManagedCallback：： ExitProcess 方法
title: ICorDebugManagedCallback::ExitProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.ExitProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::ExitProcess
helpviewer_keywords:
- ExitProcess method, ICorDebugManagedCallback interface [.NET Framework debugging]
- ICorDebugManagedCallback::ExitProcess method [.NET Framework debugging]
ms.assetid: 63a7d47a-0d54-4e29-9767-9f09feaa38b7
topic_type:
- apiref
ms.openlocfilehash: 3418931b8397edefcb801986275c35b28e00072d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790953"
---
# <a name="icordebugmanagedcallbackexitprocess-method"></a><span data-ttu-id="f9179-103">ICorDebugManagedCallback::ExitProcess 方法</span><span class="sxs-lookup"><span data-stu-id="f9179-103">ICorDebugManagedCallback::ExitProcess Method</span></span>

<span data-ttu-id="f9179-104">通知调试器进程已退出。</span><span class="sxs-lookup"><span data-stu-id="f9179-104">Notifies the debugger that a process has exited.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f9179-105">语法</span><span class="sxs-lookup"><span data-stu-id="f9179-105">Syntax</span></span>  
  
```cpp  
HRESULT ExitProcess (  
    [in] ICorDebugProcess *pProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f9179-106">参数</span><span class="sxs-lookup"><span data-stu-id="f9179-106">Parameters</span></span>  

 `pProcess`  
 <span data-ttu-id="f9179-107">中指向表示进程的 ICorDebugProcess 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="f9179-107">[in] A pointer to an ICorDebugProcess object that represents the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f9179-108">备注</span><span class="sxs-lookup"><span data-stu-id="f9179-108">Remarks</span></span>  

 <span data-ttu-id="f9179-109">无法从 `ExitProcess` 事件继续。</span><span class="sxs-lookup"><span data-stu-id="f9179-109">You cannot continue from an `ExitProcess` event.</span></span> <span data-ttu-id="f9179-110">此事件可能会在进程显示为停止时异步激发其他事件。</span><span class="sxs-lookup"><span data-stu-id="f9179-110">This event may fire asynchronously to other events while the process appears to be stopped.</span></span> <span data-ttu-id="f9179-111">如果进程在停止时终止，通常是由某个外部强制导致的，则可能会发生这种情况。</span><span class="sxs-lookup"><span data-stu-id="f9179-111">This can occur if the process terminates while stopped, usually due to some external force.</span></span>  
  
 <span data-ttu-id="f9179-112">如果公共语言运行时 (CLR) 已调度托管回调，则此事件将被延迟，直到该回调返回。</span><span class="sxs-lookup"><span data-stu-id="f9179-112">If the common language runtime (CLR) is already dispatching a managed callback, this event will be delayed until after that callback has returned.</span></span>  
  
 <span data-ttu-id="f9179-113">`ExitProcess`事件是唯一一种可保证在关闭时调用的退出/卸载事件。</span><span class="sxs-lookup"><span data-stu-id="f9179-113">The `ExitProcess` event is the only exit/unload event that is guaranteed to get called on shutdown.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f9179-114">要求</span><span class="sxs-lookup"><span data-stu-id="f9179-114">Requirements</span></span>  

 <span data-ttu-id="f9179-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f9179-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f9179-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f9179-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f9179-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f9179-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f9179-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f9179-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f9179-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="f9179-119">See also</span></span>

- [<span data-ttu-id="f9179-120">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="f9179-120">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
