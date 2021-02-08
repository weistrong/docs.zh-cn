---
description: 了解详细信息： ICorDebugManagedCallback：： CreateAppDomain 方法
title: ICorDebugManagedCallback::CreateAppDomain 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.CreateAppDomain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::CreateAppDomain
helpviewer_keywords:
- CreateAppDomain method [.NET Framework debugging]
- ICorDebugManagedCallback::CreateAppDomain method [.NET Framework debugging]
ms.assetid: 48d410d7-6749-4125-a8fd-f9562c7088e9
topic_type:
- apiref
ms.openlocfilehash: 5f4aa49ce90e8ec1343794db71ae3aa911c9e09f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791060"
---
# <a name="icordebugmanagedcallbackcreateappdomain-method"></a><span data-ttu-id="1a93d-103">ICorDebugManagedCallback::CreateAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="1a93d-103">ICorDebugManagedCallback::CreateAppDomain Method</span></span>

<span data-ttu-id="1a93d-104">通知调试器已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="1a93d-104">Notifies the debugger that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1a93d-105">语法</span><span class="sxs-lookup"><span data-stu-id="1a93d-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateAppDomain (  
    [in] ICorDebugProcess   *pProcess,  
    [in] ICorDebugAppDomain *pAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1a93d-106">参数</span><span class="sxs-lookup"><span data-stu-id="1a93d-106">Parameters</span></span>  

 `pProcess`  
 <span data-ttu-id="1a93d-107">中指向 ICorDebugProcess 对象的指针，该对象表示在其中创建应用程序域的进程。</span><span class="sxs-lookup"><span data-stu-id="1a93d-107">[in] A pointer to an ICorDebugProcess object that represents the process in which the application domain was created.</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="1a93d-108">中指向 ICorDebugAppDomain 对象的指针，该对象表示已创建的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="1a93d-108">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that has been created.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1a93d-109">要求</span><span class="sxs-lookup"><span data-stu-id="1a93d-109">Requirements</span></span>  

 <span data-ttu-id="1a93d-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1a93d-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1a93d-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1a93d-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1a93d-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1a93d-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1a93d-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1a93d-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a93d-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="1a93d-114">See also</span></span>

- [<span data-ttu-id="1a93d-115">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="1a93d-115">ICorDebugManagedCallback Interface</span></span>](icordebugmanagedcallback-interface.md)
