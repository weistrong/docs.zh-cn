---
description: 了解详细信息： ICorDebugManagedCallback：： ExitAppDomain 方法
title: ICorDebugManagedCallback::ExitAppDomain 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.ExitAppDomain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::ExitAppDomain
helpviewer_keywords:
- ICorDebugManagedCallback::ExitAppDomain method [.NET Framework debugging]
- ExitAppDomain method [.NET Framework debugging]
ms.assetid: d815486e-b3bd-4fe8-ba28-02abdb4d67ba
topic_type:
- apiref
ms.openlocfilehash: a08f29c6c4c8196b968118433c31afb715935aec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803615"
---
# <a name="icordebugmanagedcallbackexitappdomain-method"></a><span data-ttu-id="e86f7-103">ICorDebugManagedCallback::ExitAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="e86f7-103">ICorDebugManagedCallback::ExitAppDomain Method</span></span>

<span data-ttu-id="e86f7-104">通知调试器应用程序域已退出。</span><span class="sxs-lookup"><span data-stu-id="e86f7-104">Notifies the debugger that an application domain has exited.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e86f7-105">语法</span><span class="sxs-lookup"><span data-stu-id="e86f7-105">Syntax</span></span>  
  
```cpp  
HRESULT ExitAppDomain (  
    [in] ICorDebugProcess   *pProcess,  
    [in] ICorDebugAppDomain *pAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e86f7-106">参数</span><span class="sxs-lookup"><span data-stu-id="e86f7-106">Parameters</span></span>  

 `pProcess`  
 <span data-ttu-id="e86f7-107">中指向 ICorDebugProcess 对象的指针，该对象表示包含给定应用程序域的进程。</span><span class="sxs-lookup"><span data-stu-id="e86f7-107">[in] A pointer to an ICorDebugProcess object that represents the process that contains the given application domain.</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="e86f7-108">中指向 ICorDebugAppDomain 对象的指针，该对象表示已退出的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="e86f7-108">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that has exited.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e86f7-109">要求</span><span class="sxs-lookup"><span data-stu-id="e86f7-109">Requirements</span></span>  

 <span data-ttu-id="e86f7-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e86f7-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e86f7-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e86f7-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e86f7-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e86f7-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e86f7-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e86f7-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e86f7-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="e86f7-114">See also</span></span>

- [<span data-ttu-id="e86f7-115">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="e86f7-115">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
