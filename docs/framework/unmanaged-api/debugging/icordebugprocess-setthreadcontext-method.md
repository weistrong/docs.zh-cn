---
description: 了解详细信息： ICorDebugProcess：： SetThreadContext 方法
title: ICorDebugProcess::SetThreadContext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.SetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::SetThreadContext
helpviewer_keywords:
- ICorDebugProcess::SetThreadContext method [.NET Framework debugging]
- SetThreadContext method, ICorDebugProcess interface [.NET Framework debugging]
ms.assetid: a7b50175-2bf1-40be-8f65-64aec7aa1247
topic_type:
- apiref
ms.openlocfilehash: 3576c3bf3159e3960e7d2d4601ac2fb67d7218f7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753973"
---
# <a name="icordebugprocesssetthreadcontext-method"></a><span data-ttu-id="426d9-103">ICorDebugProcess::SetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="426d9-103">ICorDebugProcess::SetThreadContext Method</span></span>

<span data-ttu-id="426d9-104">设置此进程中给定线程的上下文。</span><span class="sxs-lookup"><span data-stu-id="426d9-104">Sets the context for the given thread in this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="426d9-105">语法</span><span class="sxs-lookup"><span data-stu-id="426d9-105">Syntax</span></span>  
  
```cpp  
HRESULT SetThreadContext(  
    [in] DWORD threadID,  
    [in] ULONG32 contextSize,  
    [in, length_is(contextSize), size_is(contextSize)]  
    BYTE context[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="426d9-106">参数</span><span class="sxs-lookup"><span data-stu-id="426d9-106">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="426d9-107">中要为其设置上下文的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="426d9-107">[in] The ID of the thread for which to set the context.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="426d9-108">[in] `context` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="426d9-108">[in] The size of the `context` array.</span></span>  
  
 `context`  
 <span data-ttu-id="426d9-109">中用于描述线程上下文的字节数组。</span><span class="sxs-lookup"><span data-stu-id="426d9-109">[in] An array of bytes that describe the thread's context.</span></span>  
  
 <span data-ttu-id="426d9-110">上下文指定正在执行线程的处理器的体系结构。</span><span class="sxs-lookup"><span data-stu-id="426d9-110">The context specifies the architecture of the processor on which the thread is executing.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="426d9-111">备注</span><span class="sxs-lookup"><span data-stu-id="426d9-111">Remarks</span></span>  

 <span data-ttu-id="426d9-112">调试器应调用此方法而不是 Win32 `SetThreadContext` 函数，因为该线程实际可能处于 "被劫持" 状态，在该状态下，其上下文已暂时更改。</span><span class="sxs-lookup"><span data-stu-id="426d9-112">The debugger should call this method rather than the Win32 `SetThreadContext` function, because the thread may actually be in a "hijacked" state, in which its context has been temporarily changed.</span></span> <span data-ttu-id="426d9-113">仅当线程在本机代码中时，才应使用此方法。</span><span class="sxs-lookup"><span data-stu-id="426d9-113">This method should be used only when a thread is in native code.</span></span> <span data-ttu-id="426d9-114">在托管代码中对线程使用 [ICorDebugRegisterSet](icordebugregisterset-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="426d9-114">Use [ICorDebugRegisterSet](icordebugregisterset-interface.md) for threads in managed code.</span></span> <span data-ttu-id="426d9-115">在带外 (OOB) 调试事件期间，你永远不需要修改线程的上下文。</span><span class="sxs-lookup"><span data-stu-id="426d9-115">You should never need to modify the context of a thread during an out-of-band (OOB) debug event.</span></span>  
  
 <span data-ttu-id="426d9-116">传递的数据必须是当前平台的上下文结构。</span><span class="sxs-lookup"><span data-stu-id="426d9-116">The data passed must be a context structure for the current platform.</span></span>  
  
 <span data-ttu-id="426d9-117">如果使用不当，此方法可能会损坏运行时。</span><span class="sxs-lookup"><span data-stu-id="426d9-117">This method can corrupt the runtime if used improperly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="426d9-118">要求</span><span class="sxs-lookup"><span data-stu-id="426d9-118">Requirements</span></span>  

 <span data-ttu-id="426d9-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="426d9-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="426d9-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="426d9-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="426d9-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="426d9-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="426d9-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="426d9-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
