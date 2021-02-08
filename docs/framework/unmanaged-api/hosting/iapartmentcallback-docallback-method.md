---
description: 了解详细信息： IApartmentCallback：:D oCallback 方法
title: IApartmentCallback::DoCallback 方法
ms.date: 03/30/2017
api_name:
- IApartmentCallback.DoCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- DoCallback
helpviewer_keywords:
- IApartmentCallback::DoCallback method [.NET Framework hosting]
- DoCallback method [.NET Framework hosting]
ms.assetid: 8edad30c-30ff-4bee-813c-75525a82fc93
topic_type:
- apiref
ms.openlocfilehash: 65b7f496f953f08e099bf13ef8212c7d6e1026ff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785095"
---
# <a name="iapartmentcallbackdocallback-method"></a><span data-ttu-id="5f135-103">IApartmentCallback::DoCallback 方法</span><span class="sxs-lookup"><span data-stu-id="5f135-103">IApartmentCallback::DoCallback Method</span></span>

<span data-ttu-id="5f135-104">在单元内执行指定的函数。</span><span class="sxs-lookup"><span data-stu-id="5f135-104">Executes the specified function within an apartment.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f135-105">语法</span><span class="sxs-lookup"><span data-stu-id="5f135-105">Syntax</span></span>  
  
```cpp  
HRESULT _stdcall DoCallback(  
    [in] SIZE_T pFunc,  
    [in] SIZE_T pData  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5f135-106">参数</span><span class="sxs-lookup"><span data-stu-id="5f135-106">Parameters</span></span>  

 `pFunc`  
 <span data-ttu-id="5f135-107">中指向要在单元中执行的函数的指针。</span><span class="sxs-lookup"><span data-stu-id="5f135-107">[in] A pointer to the function to be executed within the apartment.</span></span>  
  
 `pData`  
 <span data-ttu-id="5f135-108">中指向函数的自变量的指针。</span><span class="sxs-lookup"><span data-stu-id="5f135-108">[in] A pointer to the function's argument.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f135-109">要求</span><span class="sxs-lookup"><span data-stu-id="5f135-109">Requirements</span></span>  

 <span data-ttu-id="5f135-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f135-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f135-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5f135-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5f135-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5f135-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5f135-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f135-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f135-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f135-114">See also</span></span>

- [<span data-ttu-id="5f135-115">IApartmentCallback 接口</span><span class="sxs-lookup"><span data-stu-id="5f135-115">IApartmentCallback Interface</span></span>](iapartmentcallback-interface.md)
