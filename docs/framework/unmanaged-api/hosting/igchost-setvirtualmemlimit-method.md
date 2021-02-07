---
description: 了解详细信息： IGCHost：： SetVirtualMemLimit 方法
title: IGCHost::SetVirtualMemLimit 方法
ms.date: 03/30/2017
api_name:
- IGCHost.SetVirtualMemLimit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetVirtualMemLimit
helpviewer_keywords:
- IGCHost::SetVirtualMemLimit method [.NET Framework hosting]
- SetVirtualMemLimit method [.NET Framework hosting]
ms.assetid: c7e7c2d0-e58c-4650-b40c-47b2be2cda45
topic_type:
- apiref
ms.openlocfilehash: 62cd9e2d84e51f0544e464bdbf49c50af8086546
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709433"
---
# <a name="igchostsetvirtualmemlimit-method"></a><span data-ttu-id="bd94f-103">IGCHost::SetVirtualMemLimit 方法</span><span class="sxs-lookup"><span data-stu-id="bd94f-103">IGCHost::SetVirtualMemLimit Method</span></span>

<span data-ttu-id="bd94f-104">设置运行时的虚拟内存的最大大小。</span><span class="sxs-lookup"><span data-stu-id="bd94f-104">Sets the maximum size of the runtime's virtual memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd94f-105">语法</span><span class="sxs-lookup"><span data-stu-id="bd94f-105">Syntax</span></span>  
  
```cpp  
HRESULT SetVirtualMemLimit (  
    [in] SIZE_T sztMaxVirtualMemMB  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bd94f-106">参数</span><span class="sxs-lookup"><span data-stu-id="bd94f-106">Parameters</span></span>  

 `sztMaxVirtualMemMB`  
 <span data-ttu-id="bd94f-107">中运行时虚拟内存的最大大小（以 mb 为单位）。</span><span class="sxs-lookup"><span data-stu-id="bd94f-107">[in] The maximum size, in megabytes, of the runtime's virtual memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bd94f-108">备注</span><span class="sxs-lookup"><span data-stu-id="bd94f-108">Remarks</span></span>  

 <span data-ttu-id="bd94f-109">可以动态更改运行时的虚拟内存的最大大小。</span><span class="sxs-lookup"><span data-stu-id="bd94f-109">The maximum size of the runtime's virtual memory can be changed dynamically.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bd94f-110">要求</span><span class="sxs-lookup"><span data-stu-id="bd94f-110">Requirements</span></span>  

 <span data-ttu-id="bd94f-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bd94f-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bd94f-112">**标头：** GCHost，GCHost</span><span class="sxs-lookup"><span data-stu-id="bd94f-112">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="bd94f-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bd94f-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bd94f-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bd94f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd94f-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="bd94f-115">See also</span></span>

- [<span data-ttu-id="bd94f-116">IGCHost 接口</span><span class="sxs-lookup"><span data-stu-id="bd94f-116">IGCHost Interface</span></span>](igchost-interface.md)
