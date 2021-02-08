---
description: 了解详细信息： ICorDebugManagedCallback：： CreateThread 方法
title: ICorDebugManagedCallback::CreateThread 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.CreateThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::CreateThread method
helpviewer_keywords:
- ICorDebugManagedCallback::CreateThread method [.NET Framework debugging]
- CreateThread method [.NET Framework debugging]
ms.assetid: 6b961728-21c4-4e8d-ae81-197458be62f4
topic_type:
- apiref
ms.openlocfilehash: 20d5ce9da34e7082502252eeece2ab34b1f2e902
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791024"
---
# <a name="icordebugmanagedcallbackcreatethread-method"></a><span data-ttu-id="c33f6-103">ICorDebugManagedCallback::CreateThread 方法</span><span class="sxs-lookup"><span data-stu-id="c33f6-103">ICorDebugManagedCallback::CreateThread Method</span></span>

<span data-ttu-id="c33f6-104">通知调试器线程已开始执行托管代码。</span><span class="sxs-lookup"><span data-stu-id="c33f6-104">Notifies the debugger that a thread has started executing managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c33f6-105">语法</span><span class="sxs-lookup"><span data-stu-id="c33f6-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateThread (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *thread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c33f6-106">参数</span><span class="sxs-lookup"><span data-stu-id="c33f6-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="c33f6-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示包含线程的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="c33f6-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contains the thread.</span></span>  
  
 `thread`  
 <span data-ttu-id="c33f6-108">中指向表示线程的 ICorDebugThread 对象的指针。</span><span class="sxs-lookup"><span data-stu-id="c33f6-108">[in] A pointer to an ICorDebugThread object that represents the thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c33f6-109">备注</span><span class="sxs-lookup"><span data-stu-id="c33f6-109">Remarks</span></span>  

 <span data-ttu-id="c33f6-110">线程将定位在要执行的第一个托管代码指令上。</span><span class="sxs-lookup"><span data-stu-id="c33f6-110">The thread will be positioned at the first managed code instruction to be executed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c33f6-111">要求</span><span class="sxs-lookup"><span data-stu-id="c33f6-111">Requirements</span></span>  

 <span data-ttu-id="c33f6-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c33f6-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c33f6-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c33f6-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c33f6-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c33f6-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c33f6-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c33f6-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c33f6-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="c33f6-116">See also</span></span>

- [<span data-ttu-id="c33f6-117">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="c33f6-117">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
