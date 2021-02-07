---
description: 了解详细信息： ICorThreadpool：： CorQueueUserWorkItem 方法
title: ICorThreadpool::CorQueueUserWorkItem 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorQueueUserWorkItem
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorQueueUserWorkItem
helpviewer_keywords:
- ICorThreadpool::CorQueueUserWorkItem method [.NET Framework hosting]
- CorQueueUserWorkItem method [.NET Framework hosting]
ms.assetid: 29ac7898-a7c7-433e-8f79-cd5237e0bab8
topic_type:
- apiref
ms.openlocfilehash: fc0fc1dc3aa33bf11735fddd2c034af03f269f3b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737731"
---
# <a name="icorthreadpoolcorqueueuserworkitem-method"></a><span data-ttu-id="05e79-103">ICorThreadpool::CorQueueUserWorkItem 方法</span><span class="sxs-lookup"><span data-stu-id="05e79-103">ICorThreadpool::CorQueueUserWorkItem Method</span></span>

<span data-ttu-id="05e79-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="05e79-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05e79-105">语法</span><span class="sxs-lookup"><span data-stu-id="05e79-105">Syntax</span></span>  
  
```cpp  
HRESULT CorQueueUserWorkItem (  
    [in] LPTHREAD_START_ROUTINE Function,  
    [in] PVOID                  Context,  
    [in] BOOL                   executeOnlyOnce,  
    [out] BOOL*                 result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="05e79-106">要求</span><span class="sxs-lookup"><span data-stu-id="05e79-106">Requirements</span></span>  

 <span data-ttu-id="05e79-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="05e79-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="05e79-108">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="05e79-108">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="05e79-109">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="05e79-109">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="05e79-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="05e79-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05e79-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="05e79-111">See also</span></span>

- [<span data-ttu-id="05e79-112">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="05e79-112">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
