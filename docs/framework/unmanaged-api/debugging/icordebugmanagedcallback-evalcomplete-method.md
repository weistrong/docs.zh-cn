---
description: 了解详细信息： ICorDebugManagedCallback：： EvalComplete 方法
title: ICorDebugManagedCallback::EvalComplete 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.EvalComplete
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::EvalComplete
helpviewer_keywords:
- ICorDebugManagedCallback::EvalComplete method [.NET Framework debugging]
- EvalComplete method [.NET Framework debugging]
ms.assetid: f74ab4eb-cd1b-407c-a66d-8ec0d85647f3
topic_type:
- apiref
ms.openlocfilehash: 729b00bc630ef5d6e508b75bd6483580f1dd75b5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791018"
---
# <a name="icordebugmanagedcallbackevalcomplete-method"></a><span data-ttu-id="66469-103">ICorDebugManagedCallback::EvalComplete 方法</span><span class="sxs-lookup"><span data-stu-id="66469-103">ICorDebugManagedCallback::EvalComplete Method</span></span>

<span data-ttu-id="66469-104">通知调试器已完成计算。</span><span class="sxs-lookup"><span data-stu-id="66469-104">Notifies the debugger that an evaluation has been completed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="66469-105">语法</span><span class="sxs-lookup"><span data-stu-id="66469-105">Syntax</span></span>  
  
```cpp  
HRESULT EvalComplete (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread,  
    [in] ICorDebugEval      *pEval  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="66469-106">参数</span><span class="sxs-lookup"><span data-stu-id="66469-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="66469-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示在其中执行计算的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="66469-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain in which the evaluation was performed.</span></span>  
  
 `pThread`  
 <span data-ttu-id="66469-108">中指向 ICorDebugThread 对象的指针，该对象表示在其中执行计算的线程。</span><span class="sxs-lookup"><span data-stu-id="66469-108">[in] A pointer to an ICorDebugThread object that represents the thread in which the evaluation was performed.</span></span>  
  
 `pEval`  
 <span data-ttu-id="66469-109">中指向 ICorDebugEval 对象的指针，该对象表示执行计算的代码。</span><span class="sxs-lookup"><span data-stu-id="66469-109">[in] A pointer to an ICorDebugEval object that represents the code that performed the evaluation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="66469-110">要求</span><span class="sxs-lookup"><span data-stu-id="66469-110">Requirements</span></span>  

 <span data-ttu-id="66469-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="66469-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="66469-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="66469-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="66469-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="66469-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="66469-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="66469-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66469-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="66469-115">See also</span></span>

- [<span data-ttu-id="66469-116">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="66469-116">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
