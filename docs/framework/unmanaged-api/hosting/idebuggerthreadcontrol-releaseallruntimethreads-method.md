---
description: 了解详细信息： IDebuggerThreadControl：： ReleaseAllRuntimeThreads 方法
title: IDebuggerThreadControl::ReleaseAllRuntimeThreads 方法
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.ReleaseAllRuntimeThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ReleaseAllRuntimeThreads
helpviewer_keywords:
- ReleaseAllRuntimeThreads method [.NET Framework hosting]
- IDebuggerThreadControl::ReleaseAllRuntimeThreads method [.NET Framework hosting]
ms.assetid: 1a2995ff-5f02-4b49-84dc-3a5f9cfd7d55
topic_type:
- apiref
ms.openlocfilehash: bf551ccc2ae5bde3333dc8e3957099590a494dd3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709723"
---
# <a name="idebuggerthreadcontrolreleaseallruntimethreads-method"></a><span data-ttu-id="939a0-103">IDebuggerThreadControl::ReleaseAllRuntimeThreads 方法</span><span class="sxs-lookup"><span data-stu-id="939a0-103">IDebuggerThreadControl::ReleaseAllRuntimeThreads Method</span></span>

<span data-ttu-id="939a0-104">向宿主通知调试服务将要释放被阻止的所有线程。</span><span class="sxs-lookup"><span data-stu-id="939a0-104">Notifies the host that the debugging services are about to release all threads that are blocked.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="939a0-105">语法</span><span class="sxs-lookup"><span data-stu-id="939a0-105">Syntax</span></span>  
  
```cpp  
HRESULT ReleaseAllRuntimeThreads ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="939a0-106">备注</span><span class="sxs-lookup"><span data-stu-id="939a0-106">Remarks</span></span>  

 <span data-ttu-id="939a0-107">`ReleaseAllRuntimeThreads`永远不会在运行时线程上调用方法。</span><span class="sxs-lookup"><span data-stu-id="939a0-107">The `ReleaseAllRuntimeThreads` method will never be called on a runtime thread.</span></span> <span data-ttu-id="939a0-108">如果主机已阻止运行时线程，则它现在应释放它。</span><span class="sxs-lookup"><span data-stu-id="939a0-108">If the host has a runtime thread blocked, it should release it now.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="939a0-109">要求</span><span class="sxs-lookup"><span data-stu-id="939a0-109">Requirements</span></span>  

 <span data-ttu-id="939a0-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="939a0-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="939a0-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="939a0-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="939a0-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="939a0-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="939a0-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="939a0-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="939a0-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="939a0-114">See also</span></span>

- [<span data-ttu-id="939a0-115">IDebuggerThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="939a0-115">IDebuggerThreadControl Interface</span></span>](idebuggerthreadcontrol-interface.md)
