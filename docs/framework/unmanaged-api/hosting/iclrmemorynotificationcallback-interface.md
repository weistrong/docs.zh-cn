---
description: 了解详细信息： ICLRMemoryNotificationCallback 接口
title: ICLRMemoryNotificationCallback 接口
ms.date: 03/30/2017
api_name:
- ICLRMemoryNotificationCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMemoryNotificationCallback
helpviewer_keywords:
- ICLRMemoryNotificationCallback interface [.NET Framework hosting]
ms.assetid: 873639e2-4837-4568-83b3-4493e67e4174
topic_type:
- apiref
ms.openlocfilehash: 46e53cdf0b7f797b8945237d47fc3b521b08ddb7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689217"
---
# <a name="iclrmemorynotificationcallback-interface"></a><span data-ttu-id="b52f5-103">ICLRMemoryNotificationCallback 接口</span><span class="sxs-lookup"><span data-stu-id="b52f5-103">ICLRMemoryNotificationCallback Interface</span></span>

<span data-ttu-id="b52f5-104">允许主机使用类似于 Win32 函数的方法来报告内存压力情况 `CreateMemoryResourceNotification` 。</span><span class="sxs-lookup"><span data-stu-id="b52f5-104">Allows the host to report memory pressure conditions using an approach similar to that of the Win32 `CreateMemoryResourceNotification` function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b52f5-105">方法</span><span class="sxs-lookup"><span data-stu-id="b52f5-105">Methods</span></span>  
  
|<span data-ttu-id="b52f5-106">方法</span><span class="sxs-lookup"><span data-stu-id="b52f5-106">Method</span></span>|<span data-ttu-id="b52f5-107">说明</span><span class="sxs-lookup"><span data-stu-id="b52f5-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b52f5-108">OnMemoryNotification 方法</span><span class="sxs-lookup"><span data-stu-id="b52f5-108">OnMemoryNotification Method</span></span>](iclrmemorynotificationcallback-onmemorynotification-method.md)|<span data-ttu-id="b52f5-109"> (CLR) 计算机上的内存负载通知公共语言运行时。</span><span class="sxs-lookup"><span data-stu-id="b52f5-109">Notifies the common language runtime (CLR) of the memory load on the computer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b52f5-110">备注</span><span class="sxs-lookup"><span data-stu-id="b52f5-110">Remarks</span></span>  

 <span data-ttu-id="b52f5-111">主机使用 `ICLRMemoryNotificationCallback` 接口请求 CLR 释放内存资源。</span><span class="sxs-lookup"><span data-stu-id="b52f5-111">The host uses the `ICLRMemoryNotificationCallback` interface to request that the CLR free memory resources.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b52f5-112">要求</span><span class="sxs-lookup"><span data-stu-id="b52f5-112">Requirements</span></span>  

 <span data-ttu-id="b52f5-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b52f5-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b52f5-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b52f5-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b52f5-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b52f5-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b52f5-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b52f5-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b52f5-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="b52f5-117">See also</span></span>

- [<span data-ttu-id="b52f5-118">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="b52f5-118">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
- [<span data-ttu-id="b52f5-119">承载接口</span><span class="sxs-lookup"><span data-stu-id="b52f5-119">Hosting Interfaces</span></span>](hosting-interfaces.md)
