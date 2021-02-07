---
description: 了解详细信息： ICorThreadpool：： CorChangeTimer 方法
title: ICorThreadpool::CorChangeTimer 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorChangeTimer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorChangeTimer
helpviewer_keywords:
- CorChangeTimer method [.NET Framework hosting]
- ICorThreadpool::CorChangeTimer method [.NET Framework hosting]
ms.assetid: 82b03a59-5a87-43ed-9b75-e04b256e1a46
topic_type:
- apiref
ms.openlocfilehash: 259974d7c04f0bf0b4cc6b93234b35ab2c96e2ae
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671992"
---
# <a name="icorthreadpoolcorchangetimer-method"></a><span data-ttu-id="956e4-103">ICorThreadpool::CorChangeTimer 方法</span><span class="sxs-lookup"><span data-stu-id="956e4-103">ICorThreadpool::CorChangeTimer Method</span></span>

<span data-ttu-id="956e4-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="956e4-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="956e4-105">语法</span><span class="sxs-lookup"><span data-stu-id="956e4-105">Syntax</span></span>  
  
```cpp  
HRESULT CorChangeTimer (  
    [in]  HANDLE Timer,
    [in]  ULONG  DueTime,
    [in]  ULONG  Period,  
    [out] BOOL*  result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="956e4-106">要求</span><span class="sxs-lookup"><span data-stu-id="956e4-106">Requirements</span></span>  

 <span data-ttu-id="956e4-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="956e4-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="956e4-108">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="956e4-108">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="956e4-109">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="956e4-109">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="956e4-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="956e4-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="956e4-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="956e4-111">See also</span></span>

- [<span data-ttu-id="956e4-112">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="956e4-112">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
