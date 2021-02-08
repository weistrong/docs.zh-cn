---
description: 了解详细信息： ICorThreadpool：： CorSetMaxThreads 方法
title: ICorThreadpool::CorSetMaxThreads 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorSetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSetMaxThreads
helpviewer_keywords:
- ICorThreadpool::CorSetMaxThreads method [.NET Framework hosting]
- CorSetMaxThreads method [.NET Framework hosting]
ms.assetid: 4a846238-df4e-4060-ba3b-5173f6a51e85
topic_type:
- apiref
ms.openlocfilehash: 5eb55604b55da58ffb4b5b2806aa3e340274a6b2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789536"
---
# <a name="icorthreadpoolcorsetmaxthreads-method"></a><span data-ttu-id="20c1c-103">ICorThreadpool::CorSetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="20c1c-103">ICorThreadpool::CorSetMaxThreads Method</span></span>

<span data-ttu-id="20c1c-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="20c1c-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20c1c-105">语法</span><span class="sxs-lookup"><span data-stu-id="20c1c-105">Syntax</span></span>  
  
```cpp  
HRESULT CorSetMaxThreads (  
    [in] DWORD MaxWorkerThreads,  
    [in] DWORD MaxIOCompletionThreads  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="20c1c-106">要求</span><span class="sxs-lookup"><span data-stu-id="20c1c-106">Requirements</span></span>  

 <span data-ttu-id="20c1c-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="20c1c-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20c1c-108">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="20c1c-108">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="20c1c-109">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="20c1c-109">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="20c1c-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20c1c-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20c1c-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="20c1c-111">See also</span></span>

- [<span data-ttu-id="20c1c-112">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="20c1c-112">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
