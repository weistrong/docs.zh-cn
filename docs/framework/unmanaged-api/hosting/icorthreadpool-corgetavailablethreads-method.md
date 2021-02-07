---
description: 了解详细信息： ICorThreadpool：： CorGetAvailableThreads 方法
title: ICorThreadpool::CorGetAvailableThreads 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorGetAvailableThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorGetAvailableThreads
helpviewer_keywords:
- CorGetAvailableThreads method [.NET Framework hosting]
- ICorThreadpool::CorGetAvailableThreads method [.NET Framework hosting]
ms.assetid: 0b09b750-0b86-4ba4-9621-041857cfe8ba
topic_type:
- apiref
ms.openlocfilehash: ca6b476a00ce781e10c0708f5132b398b4c85398
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760571"
---
# <a name="icorthreadpoolcorgetavailablethreads-method"></a><span data-ttu-id="9c9de-103">ICorThreadpool::CorGetAvailableThreads 方法</span><span class="sxs-lookup"><span data-stu-id="9c9de-103">ICorThreadpool::CorGetAvailableThreads Method</span></span>

<span data-ttu-id="9c9de-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="9c9de-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c9de-105">语法</span><span class="sxs-lookup"><span data-stu-id="9c9de-105">Syntax</span></span>  
  
```cpp  
HRESULT CorGetAvailableThreads (  
    [out] DWORD *AvailableWorkerThreads,  
    [out] DWORD *AvailableIOCompletionThreads  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="9c9de-106">要求</span><span class="sxs-lookup"><span data-stu-id="9c9de-106">Requirements</span></span>  

 <span data-ttu-id="9c9de-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9c9de-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9c9de-108">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9c9de-108">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9c9de-109">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9c9de-109">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9c9de-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9c9de-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c9de-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="9c9de-111">See also</span></span>

- [<span data-ttu-id="9c9de-112">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="9c9de-112">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
