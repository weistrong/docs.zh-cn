---
description: 了解详细信息： ICorDebugManagedCallback：： EvalException 方法
title: ICorDebugManagedCallback::EvalException 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.EvalException
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::EvalException
helpviewer_keywords:
- EvalException method [.NET Framework debugging]
- ICorDebugManagedCallback::EvalException method [.NET Framework debugging]
ms.assetid: d6036345-18a3-45c1-a302-b1c6f2dced9b
topic_type:
- apiref
ms.openlocfilehash: 0938276a854020efa897499af8c0fd69c0541124
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790979"
---
# <a name="icordebugmanagedcallbackevalexception-method"></a><span data-ttu-id="a0e05-103">ICorDebugManagedCallback::EvalException 方法</span><span class="sxs-lookup"><span data-stu-id="a0e05-103">ICorDebugManagedCallback::EvalException Method</span></span>

<span data-ttu-id="a0e05-104">通知调试器，计算已终止，并出现未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="a0e05-104">Notifies the debugger that an evaluation has terminated with an unhandled exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0e05-105">语法</span><span class="sxs-lookup"><span data-stu-id="a0e05-105">Syntax</span></span>  
  
```cpp  
HRESULT EvalException (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread,  
    [in] ICorDebugEval      *pEval  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a0e05-106">参数</span><span class="sxs-lookup"><span data-stu-id="a0e05-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="a0e05-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示评估终止的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="a0e05-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain in which the evaluation terminated.</span></span>  
  
 `pThread`  
 <span data-ttu-id="a0e05-108">中指向 ICorDebugThread 对象的指针，该对象表示在其中终止计算的线程。</span><span class="sxs-lookup"><span data-stu-id="a0e05-108">[in] A pointer to an ICorDebugThread object that represents the thread in which the evaluation terminated.</span></span>  
  
 `pEval`  
 <span data-ttu-id="a0e05-109">中指向 ICorDebugEval 对象的指针，该对象表示执行计算的代码。</span><span class="sxs-lookup"><span data-stu-id="a0e05-109">[in] A pointer to an ICorDebugEval object that represents the code that performed the evaluation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a0e05-110">要求</span><span class="sxs-lookup"><span data-stu-id="a0e05-110">Requirements</span></span>  

 <span data-ttu-id="a0e05-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a0e05-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a0e05-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a0e05-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a0e05-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a0e05-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a0e05-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a0e05-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0e05-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="a0e05-115">See also</span></span>

- [<span data-ttu-id="a0e05-116">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="a0e05-116">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
