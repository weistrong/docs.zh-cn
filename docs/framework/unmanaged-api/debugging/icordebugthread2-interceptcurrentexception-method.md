---
description: 了解详细信息： ICorDebugThread2：： InterceptCurrentException 方法
title: ICorDebugThread2::InterceptCurrentException 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread2.InterceptCurrentException
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread2::InterceptCurrentException
helpviewer_keywords:
- InterceptCurrentException method [.NET Framework debugging]
- ICorDebugThread2::InterceptCurrentException method [.NET Framework debugging]
ms.assetid: 536d2357-1b97-49e0-a10c-c860aed74e6e
topic_type:
- apiref
ms.openlocfilehash: 5bf8d3adf6f5e4a24d8fc5abddb72c0c8963c142
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790706"
---
# <a name="icordebugthread2interceptcurrentexception-method"></a><span data-ttu-id="f339c-103">ICorDebugThread2::InterceptCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="f339c-103">ICorDebugThread2::InterceptCurrentException Method</span></span>

<span data-ttu-id="f339c-104">允许调试器截获此线程上的当前异常。</span><span class="sxs-lookup"><span data-stu-id="f339c-104">Allows a debugger to intercept the current exception on this thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f339c-105">语法</span><span class="sxs-lookup"><span data-stu-id="f339c-105">Syntax</span></span>  
  
```cpp  
HRESULT InterceptCurrentException (  
    [in] ICorDebugFrame  *pFrame  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f339c-106">参数</span><span class="sxs-lookup"><span data-stu-id="f339c-106">Parameters</span></span>  

 `pFrame`  
 <span data-ttu-id="f339c-107">中指向表示活动堆栈帧的 ICorDebugFrame 的指针。</span><span class="sxs-lookup"><span data-stu-id="f339c-107">[in] A pointer to an ICorDebugFrame that represents the active stack frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f339c-108">备注</span><span class="sxs-lookup"><span data-stu-id="f339c-108">Remarks</span></span>  

 <span data-ttu-id="f339c-109">`InterceptCurrentException`可在异常回调 ([ICorDebugManagedCallback：： Exception](icordebugmanagedcallback-exception-method.md)或[ICorDebugManagedCallback2：： exception](icordebugmanagedcallback2-exception-method.md)) 与[ICorDebugController：： Continue](icordebugcontroller-continue-method.md)的关联调用之间调用此方法。</span><span class="sxs-lookup"><span data-stu-id="f339c-109">The `InterceptCurrentException` method can be called between an exception callback ([ICorDebugManagedCallback::Exception](icordebugmanagedcallback-exception-method.md) or [ICorDebugManagedCallback2::Exception](icordebugmanagedcallback2-exception-method.md)) and the associated call to [ICorDebugController::Continue](icordebugcontroller-continue-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f339c-110">要求</span><span class="sxs-lookup"><span data-stu-id="f339c-110">Requirements</span></span>  

 <span data-ttu-id="f339c-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f339c-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f339c-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f339c-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f339c-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f339c-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f339c-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f339c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
