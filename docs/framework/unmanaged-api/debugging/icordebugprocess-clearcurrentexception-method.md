---
description: 了解详细信息： ICorDebugProcess：： ClearCurrentException 方法
title: ICorDebugProcess::ClearCurrentException 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.ClearCurrentException
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::ClearCurrentException
helpviewer_keywords:
- ClearCurrentException method, ICorDebugProcess interface [.NET Framework debugging]
- ICorDebugProcess::ClearCurrentException method [.NET Framework debugging]
ms.assetid: 9e02ee1a-e495-4578-bfb5-b946274bede7
topic_type:
- apiref
ms.openlocfilehash: 6f356078d8d303acb39cbaa500b7592185ad55ef
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754025"
---
# <a name="icordebugprocessclearcurrentexception-method"></a><span data-ttu-id="63dcd-103">ICorDebugProcess::ClearCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="63dcd-103">ICorDebugProcess::ClearCurrentException Method</span></span>

<span data-ttu-id="63dcd-104">清除给定线程上的当前非托管异常。</span><span class="sxs-lookup"><span data-stu-id="63dcd-104">Clears the current unmanaged exception on the given thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63dcd-105">语法</span><span class="sxs-lookup"><span data-stu-id="63dcd-105">Syntax</span></span>  
  
```cpp  
HRESULT ClearCurrentException([in] DWORD threadID);  
```  
  
## <a name="parameters"></a><span data-ttu-id="63dcd-106">参数</span><span class="sxs-lookup"><span data-stu-id="63dcd-106">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="63dcd-107">中将清除当前非托管异常的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="63dcd-107">[in] The ID of the thread on which the current unmanaged exception will be cleared.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="63dcd-108">备注</span><span class="sxs-lookup"><span data-stu-id="63dcd-108">Remarks</span></span>  

 <span data-ttu-id="63dcd-109">在线程报告了应被调试对象忽略的非托管异常之前，请在调用 [ICorDebugController：： Continue](icordebugcontroller-continue-method.md) 之前调用此方法。</span><span class="sxs-lookup"><span data-stu-id="63dcd-109">Call this method before calling [ICorDebugController::Continue](icordebugcontroller-continue-method.md) when a thread has reported an unmanaged exception that should be ignored by the debuggee.</span></span> <span data-ttu-id="63dcd-110">这会清除给定线程上未完成的带外 (IB) 和带外 (OOB) 事件。</span><span class="sxs-lookup"><span data-stu-id="63dcd-110">This will clear both the outstanding in-band (IB) and out-of-band (OOB) events on the given thread.</span></span> <span data-ttu-id="63dcd-111">自动清除所有 OOB 断点和单步例外。</span><span class="sxs-lookup"><span data-stu-id="63dcd-111">All OOB breakpoints and single-step exceptions are automatically cleared.</span></span>  
  
 <span data-ttu-id="63dcd-112">使用 [ICorDebugThread2：： InterceptCurrentException](icordebugthread2-interceptcurrentexception-method.md) 来截获线程上的当前托管异常。</span><span class="sxs-lookup"><span data-stu-id="63dcd-112">Use [ICorDebugThread2::InterceptCurrentException](icordebugthread2-interceptcurrentexception-method.md) to intercept the current managed exception on a thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="63dcd-113">要求</span><span class="sxs-lookup"><span data-stu-id="63dcd-113">Requirements</span></span>  

 <span data-ttu-id="63dcd-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="63dcd-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="63dcd-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="63dcd-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="63dcd-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="63dcd-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="63dcd-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="63dcd-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
