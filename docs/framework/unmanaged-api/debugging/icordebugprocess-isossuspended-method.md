---
description: 了解详细信息： ICorDebugProcess：： IsOSSuspended 方法
title: ICorDebugProcess::IsOSSuspended 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.IsOSSuspended
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::IsOSSuspended
helpviewer_keywords:
- IsOSSuspended method [.NET Framework debugging]
- ICorDebugProcess::IsOSSuspended method [.NET Framework debugging]
ms.assetid: 83406cb2-5797-4402-872d-89c9516aefec
topic_type:
- apiref
ms.openlocfilehash: aa5e438418330d9fee51fcdb56a617421df06904
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746732"
---
# <a name="icordebugprocessisossuspended-method"></a><span data-ttu-id="e6366-103">ICorDebugProcess::IsOSSuspended 方法</span><span class="sxs-lookup"><span data-stu-id="e6366-103">ICorDebugProcess::IsOSSuspended Method</span></span>

<span data-ttu-id="e6366-104">获取一个值，该值指示是否由于调试器停止此进程而挂起了指定线程。</span><span class="sxs-lookup"><span data-stu-id="e6366-104">Gets a value that indicates whether the specified thread has been suspended as a result of the debugger stopping this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6366-105">语法</span><span class="sxs-lookup"><span data-stu-id="e6366-105">Syntax</span></span>  
  
```cpp  
HRESULT IsOSSuspended(  
    [in]  DWORD threadID,  
    [out] BOOL  *pbSuspended);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e6366-106">参数</span><span class="sxs-lookup"><span data-stu-id="e6366-106">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="e6366-107">中相关线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="e6366-107">[in] The ID of thread in question.</span></span>  
  
 `pbSuspended`  
 <span data-ttu-id="e6366-108">弄指向布尔值的指针， `true` 如果指定线程已挂起，则为; 否则 `pbSuspended` 为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="e6366-108">[out] A pointer to a Boolean value that is `true` if the specified thread has been suspended; otherwise \*`pbSuspended` is `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e6366-109">备注</span><span class="sxs-lookup"><span data-stu-id="e6366-109">Remarks</span></span>  

 <span data-ttu-id="e6366-110">当由于调试器停止此进程而暂停指定的线程时，指定线程的 Win32 挂起计数将递增1。</span><span class="sxs-lookup"><span data-stu-id="e6366-110">When the specified thread has been suspended as a result of the debugger stopping this process, the specified thread's Win32 suspend count is incremented by one.</span></span> <span data-ttu-id="e6366-111">如果调试器用户界面向用户显示操作系统 (OS) 挂起线程计数，则 (UI) 可能需要考虑此信息。</span><span class="sxs-lookup"><span data-stu-id="e6366-111">The debugger user interface (UI) may want to take this information into account if it displays the operating system (OS) suspend count of the thread to the user.</span></span>  
  
 <span data-ttu-id="e6366-112">此 `IsOSSuspended` 方法仅在非托管调试的上下文中有意义。</span><span class="sxs-lookup"><span data-stu-id="e6366-112">The `IsOSSuspended` method makes sense only in the context of unmanaged debugging.</span></span> <span data-ttu-id="e6366-113">在托管调试期间，线程会以协作方式暂停，而不是由 OS 挂起。</span><span class="sxs-lookup"><span data-stu-id="e6366-113">During managed debugging, threads are cooperatively suspended rather than OS-suspended.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6366-114">要求</span><span class="sxs-lookup"><span data-stu-id="e6366-114">Requirements</span></span>  

 <span data-ttu-id="e6366-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e6366-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e6366-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e6366-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e6366-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e6366-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e6366-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e6366-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
