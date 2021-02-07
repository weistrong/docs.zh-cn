---
description: 了解详细信息： ICorThreadpool：： CorCreateTimer 方法
title: ICorThreadpool::CorCreateTimer 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorCreateTimer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorCreateTimer
helpviewer_keywords:
- CorCreateTimer method [.NET Framework hosting]
- ICorThreadpool::CorCreateTimer method [.NET Framework hosting]
ms.assetid: 0d56ef25-30f1-4499-8a1f-76e7654ec614
topic_type:
- apiref
ms.openlocfilehash: dc4258493181430a7e803f3b995e6b32ed2cd8b2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737755"
---
# <a name="icorthreadpoolcorcreatetimer-method"></a><span data-ttu-id="24422-103">ICorThreadpool::CorCreateTimer 方法</span><span class="sxs-lookup"><span data-stu-id="24422-103">ICorThreadpool::CorCreateTimer Method</span></span>

<span data-ttu-id="24422-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="24422-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24422-105">语法</span><span class="sxs-lookup"><span data-stu-id="24422-105">Syntax</span></span>  
  
```cpp  
HRESULT CorCreateTimer (  
    [in]  HANDLE*             phNewTimer,  
    [in]  WAITORTIMERCALLBACK Callback,  
    [in]  PVOID               Parameter,  
    [in]  DWORD               DueTime,  
    [in]  DWORD               Period,  
    [out] BOOL*               result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="24422-106">要求</span><span class="sxs-lookup"><span data-stu-id="24422-106">Requirements</span></span>  

 <span data-ttu-id="24422-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="24422-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24422-108">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="24422-108">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="24422-109">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="24422-109">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="24422-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="24422-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24422-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="24422-111">See also</span></span>

- [<span data-ttu-id="24422-112">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="24422-112">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
