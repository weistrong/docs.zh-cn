---
description: 了解详细信息： ICorDebugManagedCallback：： Exception 方法
title: ICorDebugManagedCallback::Exception 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.Exception
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::Exception
helpviewer_keywords:
- Exception method, ICorDebugManagedCallback interface [.NET Framework debugging]
- ICorDebugManagedCallback::Exception method [.NET Framework debugging]
ms.assetid: ab18a509-dff3-4930-b585-bd15e0414176
topic_type:
- apiref
ms.openlocfilehash: f738c328e1f6edfeb61a1d5e2ba8f9dd827d05dd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790966"
---
# <a name="icordebugmanagedcallbackexception-method"></a><span data-ttu-id="23ba7-103">ICorDebugManagedCallback::Exception 方法</span><span class="sxs-lookup"><span data-stu-id="23ba7-103">ICorDebugManagedCallback::Exception Method</span></span>

<span data-ttu-id="23ba7-104">通知调试器已从托管代码引发了异常。</span><span class="sxs-lookup"><span data-stu-id="23ba7-104">Notifies the debugger that an exception has been thrown from managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="23ba7-105">语法</span><span class="sxs-lookup"><span data-stu-id="23ba7-105">Syntax</span></span>  
  
```cpp  
HRESULT Exception (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread,  
    [in] BOOL                unhandled  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="23ba7-106">参数</span><span class="sxs-lookup"><span data-stu-id="23ba7-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="23ba7-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示引发异常的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="23ba7-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain in which the exception was thrown.</span></span>  
  
 `pThread`  
 <span data-ttu-id="23ba7-108">中指向 ICorDebugThread 对象的指针，该对象表示引发异常的线程。</span><span class="sxs-lookup"><span data-stu-id="23ba7-108">[in] A pointer to an ICorDebugThread object that represents the thread in which the exception was thrown.</span></span>  
  
 `unhandled`  
 <span data-ttu-id="23ba7-109">中如果此值为 `false` ，则应用程序尚未处理异常; 否则，异常未得到处理，将终止进程。</span><span class="sxs-lookup"><span data-stu-id="23ba7-109">[in] If this value is `false`, the exception has not yet been processed by the application; otherwise, the exception is unhandled and will terminate the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="23ba7-110">备注</span><span class="sxs-lookup"><span data-stu-id="23ba7-110">Remarks</span></span>  

 <span data-ttu-id="23ba7-111">可以从线程对象中检索特定的异常。</span><span class="sxs-lookup"><span data-stu-id="23ba7-111">The specific exception can be retrieved from the thread object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="23ba7-112">要求</span><span class="sxs-lookup"><span data-stu-id="23ba7-112">Requirements</span></span>  

 <span data-ttu-id="23ba7-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="23ba7-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="23ba7-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="23ba7-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="23ba7-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="23ba7-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="23ba7-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="23ba7-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="23ba7-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="23ba7-117">See also</span></span>

- [<span data-ttu-id="23ba7-118">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="23ba7-118">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
