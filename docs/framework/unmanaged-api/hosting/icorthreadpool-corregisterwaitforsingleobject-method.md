---
description: 了解详细信息： ICorThreadpool：： CorRegisterWaitForSingleObject 方法
title: ICorThreadpool::CorRegisterWaitForSingleObject 方法
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorRegisterWaitForSingleObject
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRegisterWaitForSingleObject
helpviewer_keywords:
- ICorThreadpool::CorRegisterWaitForSingleObject method [.NET Framework hosting]
- CorRegisterWaitForSingleObject method [.NET Framework hosting]
ms.assetid: cade1feb-71d2-43ed-85ca-7b2e9da12994
topic_type:
- apiref
ms.openlocfilehash: fdbb41f78f7aeb4a426de48e2da7616cfaecaa6e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789549"
---
# <a name="icorthreadpoolcorregisterwaitforsingleobject-method"></a><span data-ttu-id="6f73f-103">ICorThreadpool::CorRegisterWaitForSingleObject 方法</span><span class="sxs-lookup"><span data-stu-id="6f73f-103">ICorThreadpool::CorRegisterWaitForSingleObject Method</span></span>

<span data-ttu-id="6f73f-104">此方法支持 .NET Framework 基础结构，但不适合直接在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="6f73f-104">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6f73f-105">语法</span><span class="sxs-lookup"><span data-stu-id="6f73f-105">Syntax</span></span>  
  
```cpp  
HRESULT CorRegisterWaitForSingleObject (  
    [in]  HANDLE*             phNewWaitObject,  
    [in]  HANDLE              hWaitObject,  
    [in]  WAITORTIMERCALLBACK Callback,  
    [in]  PVOID               Context,  
    [in]  ULONG               timeout,  
    [in]  BOOL                executeOnlyOnce,  
    [out] BOOL*               result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="6f73f-106">要求</span><span class="sxs-lookup"><span data-stu-id="6f73f-106">Requirements</span></span>  

 <span data-ttu-id="6f73f-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6f73f-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6f73f-108">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6f73f-108">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6f73f-109">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6f73f-109">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6f73f-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6f73f-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f73f-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="6f73f-111">See also</span></span>

- [<span data-ttu-id="6f73f-112">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="6f73f-112">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)
