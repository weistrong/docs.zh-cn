---
description: 了解详细信息： IObjectHandle：：解包方法
title: IObjectHandle::Unwrap 方法
ms.date: 03/30/2017
api_name:
- IObjectHandle.Unwrap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- Unwrap
helpviewer_keywords:
- Unwrap method [.NET Framework hosting]
- IObjectHandle::Unwrap method [.NET Framework hosting]
ms.assetid: 794c6f8e-ed58-416b-b756-e864f2c958f7
topic_type:
- apiref
ms.openlocfilehash: 3f791eaf52abd045d495fe15e868423e464fd27e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728322"
---
# <a name="iobjecthandleunwrap-method"></a><span data-ttu-id="635e3-103">IObjectHandle::Unwrap 方法</span><span class="sxs-lookup"><span data-stu-id="635e3-103">IObjectHandle::Unwrap Method</span></span>

<span data-ttu-id="635e3-104">从间接寻址将按值封送对象解包。</span><span class="sxs-lookup"><span data-stu-id="635e3-104">Unwraps a marshal-by-value object from indirection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="635e3-105">语法</span><span class="sxs-lookup"><span data-stu-id="635e3-105">Syntax</span></span>  
  
```cpp  
HRESULT Unwrap (  
    [out, retval] VARIANT *ppv  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="635e3-106">参数</span><span class="sxs-lookup"><span data-stu-id="635e3-106">Parameters</span></span>  

 `ppv`  
 <span data-ttu-id="635e3-107">弄指向要解包的对象的指针。</span><span class="sxs-lookup"><span data-stu-id="635e3-107">[out] A pointer to the object to be unwrapped.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="635e3-108">要求</span><span class="sxs-lookup"><span data-stu-id="635e3-108">Requirements</span></span>  

 <span data-ttu-id="635e3-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="635e3-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="635e3-110">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="635e3-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="635e3-111">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="635e3-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="635e3-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="635e3-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
