---
description: 了解详细信息： ICorThreadpool：： CorUnregisterWait 方法
title: ICorThreadpool::CorUnregisterWait 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorUnregisterWait
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorUnregisterWait
helpviewer_keywords:
- CorUnregisterWait method [.NET Framework hosting]
- ICorThreadpool::CorUnregisterWait method [.NET Framework hosting]
ms.assetid: 42c933f1-30a8-4011-bdea-e117f3c3265e
topic_type:
- apiref
ms.openlocfilehash: 61b6c7a1fa8459ddd173d2857cff982f353afc31
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789523"
---
# <a name="icorthreadpoolcorunregisterwait-method"></a><span data-ttu-id="641cd-103">ICorThreadpool::CorUnregisterWait 方法</span><span class="sxs-lookup"><span data-stu-id="641cd-103">ICorThreadpool::CorUnregisterWait Method</span></span>

<span data-ttu-id="641cd-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="641cd-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="641cd-105">语法</span><span class="sxs-lookup"><span data-stu-id="641cd-105">Syntax</span></span>  
  
```cpp  
HRESULT CorUnregisterWait (  
    [in] HANDLE hWaitObject,  
    [in] HANDLE CompletionEvent,  
    [out] BOOL* result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="641cd-106">要求</span><span class="sxs-lookup"><span data-stu-id="641cd-106">Requirements</span></span>  

 <span data-ttu-id="641cd-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="641cd-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="641cd-108">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="641cd-108">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="641cd-109">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="641cd-109">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="641cd-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="641cd-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="641cd-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="641cd-111">See also</span></span>

- [<span data-ttu-id="641cd-112">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="641cd-112">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
