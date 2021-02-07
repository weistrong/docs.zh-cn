---
description: 了解详细信息： IGCHostControl：： RequestVirtualMemLimit 方法
title: IGCHostControl::RequestVirtualMemLimit 方法
ms.date: 03/30/2017
api_name:
- IGCHostControl.RequestVirtualMemLimit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- RequestVirtualMemLimit
helpviewer_keywords:
- IGCHostControl::RequestVirtualMemLimit method [.NET Framework hosting]
- RequestVirtualMemLimit method [.NET Framework hosting]
ms.assetid: f4984a8c-4c0e-4460-9aa1-d022b3621228
topic_type:
- apiref
ms.openlocfilehash: b0ee22671b63be0ed0d23ebb103a6a5a7ca9f2b9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709381"
---
# <a name="igchostcontrolrequestvirtualmemlimit-method"></a><span data-ttu-id="088e1-103">IGCHostControl::RequestVirtualMemLimit 方法</span><span class="sxs-lookup"><span data-stu-id="088e1-103">IGCHostControl::RequestVirtualMemLimit Method</span></span>

<span data-ttu-id="088e1-104">请求主机更改虚拟内存的限制。</span><span class="sxs-lookup"><span data-stu-id="088e1-104">Requests the host to change the limits of virtual memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="088e1-105">语法</span><span class="sxs-lookup"><span data-stu-id="088e1-105">Syntax</span></span>  
  
```cpp  
HRESULT RequestVirtualMemLimit (  
    [in] SIZE_T       sztMaxVirtualMemMB,  
    [in, out] SIZE_T* psztNewMaxVirtualMemMB  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="088e1-106">参数</span><span class="sxs-lookup"><span data-stu-id="088e1-106">Parameters</span></span>  

 `sztMaxVirtualMemMB`  
 <span data-ttu-id="088e1-107">中要分配的请求的内存大小。</span><span class="sxs-lookup"><span data-stu-id="088e1-107">[in] The requested size of memory to be allocated.</span></span>  
  
 `psztNewMaxVirtualMemMB`  
 <span data-ttu-id="088e1-108">[in，out]一个指针，指向所分配的内存的实际大小。</span><span class="sxs-lookup"><span data-stu-id="088e1-108">[in, out] A pointer to the actual size of memory allocated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="088e1-109">要求</span><span class="sxs-lookup"><span data-stu-id="088e1-109">Requirements</span></span>  

 <span data-ttu-id="088e1-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="088e1-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="088e1-111">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="088e1-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="088e1-112">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="088e1-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="088e1-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="088e1-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="088e1-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="088e1-114">See also</span></span>

- [<span data-ttu-id="088e1-115">IGCHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="088e1-115">IGCHostControl Interface</span></span>](igchostcontrol-interface.md)
