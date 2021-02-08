---
description: 了解详细信息： ICorThreadpool：： CorCallOrQueueUserWorkItem 方法
title: ICorThreadpool::CorCallOrQueueUserWorkItem 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorCallOrQueueUserWorkItem
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorCallOrQueueUserWorkItem
helpviewer_keywords:
- ICorThreadpool::CorCallOrQueueUserWorkItem method [.NET Framework hosting]
- CorCallOrQueueUserWorkItem method [.NET Framework hosting]
ms.assetid: a2081223-84ca-4331-a8d3-9352f422f3e7
topic_type:
- apiref
ms.openlocfilehash: 630afab4eac94d0361b0c83c962ff6e7d59be42d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789575"
---
# <a name="icorthreadpoolcorcallorqueueuserworkitem-method"></a><span data-ttu-id="3e7ab-103">ICorThreadpool::CorCallOrQueueUserWorkItem 方法</span><span class="sxs-lookup"><span data-stu-id="3e7ab-103">ICorThreadpool::CorCallOrQueueUserWorkItem Method</span></span>

<span data-ttu-id="3e7ab-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="3e7ab-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e7ab-105">语法</span><span class="sxs-lookup"><span data-stu-id="3e7ab-105">Syntax</span></span>  
  
```cpp  
HRESULT CorCallOrQueueUserWorkItem (  
    [in] LPTHREAD_START_ROUTINE Function,  
    [in] PVOID                  Context,  
    [out] BOOL*                 result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="3e7ab-106">要求</span><span class="sxs-lookup"><span data-stu-id="3e7ab-106">Requirements</span></span>  

 <span data-ttu-id="3e7ab-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3e7ab-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3e7ab-108">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="3e7ab-108">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3e7ab-109">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3e7ab-109">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3e7ab-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e7ab-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e7ab-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="3e7ab-111">See also</span></span>

- [<span data-ttu-id="3e7ab-112">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="3e7ab-112">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
