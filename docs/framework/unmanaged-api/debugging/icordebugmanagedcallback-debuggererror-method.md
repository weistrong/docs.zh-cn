---
description: 了解详细信息： ICorDebugManagedCallback：:D ebuggerError 方法
title: ICorDebugManagedCallback::DebuggerError 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.DebuggerError
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::DebuggerError
helpviewer_keywords:
- DebuggerError method [.NET Framework debugging]
- ICorDebugManagedCallback::DebuggerError method [.NET Framework debugging]
ms.assetid: 9e983d11-eaf3-4741-b936-29ec456384a3
topic_type:
- apiref
ms.openlocfilehash: 2f73e07711f7d2ce865aab8f90862563e767fd16
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790993"
---
# <a name="icordebugmanagedcallbackdebuggererror-method"></a><span data-ttu-id="d4a9f-103">ICorDebugManagedCallback::DebuggerError 方法</span><span class="sxs-lookup"><span data-stu-id="d4a9f-103">ICorDebugManagedCallback::DebuggerError Method</span></span>

<span data-ttu-id="d4a9f-104">通知调试器在尝试处理来自公共语言运行时 (CLR) 的事件时出错。</span><span class="sxs-lookup"><span data-stu-id="d4a9f-104">Notifies the debugger that an error has occurred while attempting to handle an event from the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d4a9f-105">语法</span><span class="sxs-lookup"><span data-stu-id="d4a9f-105">Syntax</span></span>  
  
```cpp  
HRESULT DebuggerError (  
    [in] ICorDebugProcess *pProcess,  
    [in] HRESULT           errorHR,  
    [in] DWORD             errorCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d4a9f-106">参数</span><span class="sxs-lookup"><span data-stu-id="d4a9f-106">Parameters</span></span>  

 `pProcess`  
 <span data-ttu-id="d4a9f-107">中一个指向 "ICorDebugProcess" 对象的指针，该对象表示发生事件的进程。</span><span class="sxs-lookup"><span data-stu-id="d4a9f-107">[in] A pointer to an "ICorDebugProcess" object that represents the process in which the event occurred.</span></span>  
  
 `errorHR`  
 <span data-ttu-id="d4a9f-108">中从事件处理程序返回的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="d4a9f-108">[in] The HRESULT value that was returned from the event handler.</span></span>  
  
 `errorCode`  
 <span data-ttu-id="d4a9f-109">中一个整数，指定 CLR 错误。</span><span class="sxs-lookup"><span data-stu-id="d4a9f-109">[in] An integer that specifies the CLR error.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d4a9f-110">备注</span><span class="sxs-lookup"><span data-stu-id="d4a9f-110">Remarks</span></span>  

 <span data-ttu-id="d4a9f-111">根据错误的性质，此过程可能会置于直通模式下。</span><span class="sxs-lookup"><span data-stu-id="d4a9f-111">The process may be placed into pass-through mode, depending on the nature of the error.</span></span>  
  
 <span data-ttu-id="d4a9f-112">`DebugError`回调指示调试服务由于错误而被禁用，因此调试器应向用户提供错误消息。</span><span class="sxs-lookup"><span data-stu-id="d4a9f-112">The `DebugError` callback indicates that debugging services have been disabled due to an error, so debuggers should make the error message available to the user.</span></span> <span data-ttu-id="d4a9f-113">[ICorDebugProcess：： GetID](icordebugprocess-getid-method.md) 可以安全调用，但所有其他方法（包括 [ICorDebug：： Terminate](icordebug-terminate-method.md)）都不应调用。</span><span class="sxs-lookup"><span data-stu-id="d4a9f-113">[ICorDebugProcess::GetID](icordebugprocess-getid-method.md) will be safe to call, but all other methods, including [ICorDebug::Terminate](icordebug-terminate-method.md), should not be called.</span></span> <span data-ttu-id="d4a9f-114">调试器应使用操作系统工具来终止进程。</span><span class="sxs-lookup"><span data-stu-id="d4a9f-114">The debugger should use operating-system facilities for terminating processes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d4a9f-115">要求</span><span class="sxs-lookup"><span data-stu-id="d4a9f-115">Requirements</span></span>  

 <span data-ttu-id="d4a9f-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d4a9f-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d4a9f-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d4a9f-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d4a9f-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d4a9f-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d4a9f-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d4a9f-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4a9f-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="d4a9f-120">See also</span></span>

- [<span data-ttu-id="d4a9f-121">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="d4a9f-121">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
