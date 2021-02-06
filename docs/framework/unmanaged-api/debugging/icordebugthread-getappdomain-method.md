---
description: 了解详细信息： ICorDebugThread：： GetAppDomain 方法
title: ICorDebugThread::GetAppDomain 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetAppDomain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetAppDomain
helpviewer_keywords:
- GetAppDomain method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetAppDomain method [.NET Framework debugging]
ms.assetid: 415b3d34-8b35-4b60-a318-140646cc83f8
topic_type:
- apiref
ms.openlocfilehash: 416ab80fa08786fb5e95776b164723317fa59ca6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659200"
---
# <a name="icordebugthreadgetappdomain-method"></a><span data-ttu-id="820f0-103">ICorDebugThread::GetAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="820f0-103">ICorDebugThread::GetAppDomain Method</span></span>

<span data-ttu-id="820f0-104">获取一个接口指针，该指针指向此 ICorDebugThread 当前正在执行的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="820f0-104">Gets an interface pointer to the application domain in which this ICorDebugThread is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="820f0-105">语法</span><span class="sxs-lookup"><span data-stu-id="820f0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAppDomain (  
    [out] ICorDebugAppDomain  **ppAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="820f0-106">参数</span><span class="sxs-lookup"><span data-stu-id="820f0-106">Parameters</span></span>  

 `ppAppDomain`  
 <span data-ttu-id="820f0-107">弄指向 ICorDebugAppDomain 对象的指针，该对象表示此线程当前正在执行的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="820f0-107">[out] A pointer to an ICorDebugAppDomain object that represents the application domain in which this thread is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="820f0-108">要求</span><span class="sxs-lookup"><span data-stu-id="820f0-108">Requirements</span></span>  

 <span data-ttu-id="820f0-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="820f0-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="820f0-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="820f0-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="820f0-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="820f0-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="820f0-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="820f0-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
