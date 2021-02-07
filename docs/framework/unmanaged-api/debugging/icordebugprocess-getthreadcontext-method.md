---
description: 了解详细信息： ICorDebugProcess：： GetThreadContext 方法
title: ICorDebugProcess::GetThreadContext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.GetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::GetThreadContext
helpviewer_keywords:
- ICorDebugProcess::GetThreadContext method [.NET Framework debugging]
- GetThreadContext method, ICorDebugProcess interface [.NET Framework debugging]
ms.assetid: 5b132ef1-8d4b-4525-89b3-54123596c194
topic_type:
- apiref
ms.openlocfilehash: 4cb926183522548e924013580f207d1d0677a0d3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746862"
---
# <a name="icordebugprocessgetthreadcontext-method"></a><span data-ttu-id="c7f67-103">ICorDebugProcess::GetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="c7f67-103">ICorDebugProcess::GetThreadContext Method</span></span>

<span data-ttu-id="c7f67-104">获取此进程中给定线程的上下文。</span><span class="sxs-lookup"><span data-stu-id="c7f67-104">Gets the context for the given thread in this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7f67-105">语法</span><span class="sxs-lookup"><span data-stu-id="c7f67-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThreadContext(  
    [in] DWORD threadID,  
    [in] ULONG32 contextSize,  
    [in, out, length_is(contextSize), size_is(contextSize)]  
    BYTE context[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c7f67-106">参数</span><span class="sxs-lookup"><span data-stu-id="c7f67-106">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="c7f67-107">中要为其检索上下文的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="c7f67-107">[in] The ID of the thread for which to retrieve the context.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="c7f67-108">[in] `context` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="c7f67-108">[in] The size of the `context` array.</span></span>  
  
 `context`  
 <span data-ttu-id="c7f67-109">[in，out]用于描述线程上下文的字节数组。</span><span class="sxs-lookup"><span data-stu-id="c7f67-109">[in, out] An array of bytes that describe the thread's context.</span></span>  
  
 <span data-ttu-id="c7f67-110">上下文指定正在执行线程的处理器的体系结构。</span><span class="sxs-lookup"><span data-stu-id="c7f67-110">The context specifies the architecture of the processor on which the thread is executing.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c7f67-111">备注</span><span class="sxs-lookup"><span data-stu-id="c7f67-111">Remarks</span></span>  

 <span data-ttu-id="c7f67-112">调试器应调用此方法而不是 Win32 `GetThreadContext` 方法，因为该线程实际可能处于 "被劫持" 状态，在该状态下，其上下文已暂时更改。</span><span class="sxs-lookup"><span data-stu-id="c7f67-112">The debugger should call this method rather than the Win32 `GetThreadContext` method, because the thread may actually be in a "hijacked" state, in which its context has been temporarily changed.</span></span> <span data-ttu-id="c7f67-113">仅当线程在本机代码中时，才应使用此方法。</span><span class="sxs-lookup"><span data-stu-id="c7f67-113">This method should be used only when a thread is in native code.</span></span> <span data-ttu-id="c7f67-114">在托管代码中对线程使用 [ICorDebugRegisterSet](icordebugregisterset-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="c7f67-114">Use [ICorDebugRegisterSet](icordebugregisterset-interface.md) for threads in managed code.</span></span>  
  
 <span data-ttu-id="c7f67-115">返回的数据是当前平台的上下文结构。</span><span class="sxs-lookup"><span data-stu-id="c7f67-115">The data returned is a context structure for the current platform.</span></span> <span data-ttu-id="c7f67-116">与 Win32 `GetThreadContext` 方法一样，调用方应在 `context` 调用此方法之前初始化参数。</span><span class="sxs-lookup"><span data-stu-id="c7f67-116">Just as with the Win32 `GetThreadContext` method, the caller should initialize the `context` parameter before calling this method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7f67-117">要求</span><span class="sxs-lookup"><span data-stu-id="c7f67-117">Requirements</span></span>  

 <span data-ttu-id="c7f67-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c7f67-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7f67-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c7f67-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c7f67-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c7f67-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c7f67-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7f67-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
