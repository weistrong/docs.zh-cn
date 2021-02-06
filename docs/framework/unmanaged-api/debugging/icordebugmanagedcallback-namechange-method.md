---
description: 了解详细信息： ICorDebugManagedCallback：： NameChange 方法
title: ICorDebugManagedCallback::NameChange 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.NameChange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::NameChange
helpviewer_keywords:
- ICorDebugManagedCallback::NameChange method [.NET Framework debugging]
- NameChange method [.NET Framework debugging]
ms.assetid: a7018a0e-880e-4b68-b52a-1cd22c7aad62
topic_type:
- apiref
ms.openlocfilehash: 5f337f5e05b80c97e8b8e48f8b7bc76b3232b2c8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660396"
---
# <a name="icordebugmanagedcallbacknamechange-method"></a><span data-ttu-id="c7b11-103">ICorDebugManagedCallback::NameChange 方法</span><span class="sxs-lookup"><span data-stu-id="c7b11-103">ICorDebugManagedCallback::NameChange Method</span></span>

<span data-ttu-id="c7b11-104">通知调试器应用程序域或线程的名称已更改。</span><span class="sxs-lookup"><span data-stu-id="c7b11-104">Notifies the debugger that the name of either an application domain or a thread has changed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7b11-105">语法</span><span class="sxs-lookup"><span data-stu-id="c7b11-105">Syntax</span></span>  
  
```cpp  
HRESULT NameChange (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c7b11-106">参数</span><span class="sxs-lookup"><span data-stu-id="c7b11-106">Parameters</span></span>  

 `pAppDomain`  
 <span data-ttu-id="c7b11-107">中指向 ICorDebugAppDomain 对象的指针，该对象表示具有名称更改或包含名称更改的线程的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="c7b11-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that either had a name change or that contains the thread that had a name change.</span></span>  
  
 `pThread`  
 <span data-ttu-id="c7b11-108">中指向 ICorDebugThread 对象的指针，该对象表示名称发生更改的线程。</span><span class="sxs-lookup"><span data-stu-id="c7b11-108">[in] A pointer to an ICorDebugThread object that represents the thread that had a name change.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7b11-109">要求</span><span class="sxs-lookup"><span data-stu-id="c7b11-109">Requirements</span></span>  

 <span data-ttu-id="c7b11-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c7b11-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7b11-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c7b11-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c7b11-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c7b11-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c7b11-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7b11-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7b11-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="c7b11-114">See also</span></span>

- [<span data-ttu-id="c7b11-115">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="c7b11-115">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
