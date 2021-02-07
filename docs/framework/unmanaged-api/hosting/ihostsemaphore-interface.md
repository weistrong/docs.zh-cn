---
description: 了解详细信息： IHostSemaphore 接口
title: IHostSemaphore 接口
ms.date: 03/30/2017
api_name:
- IHostSemaphore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSemaphore
helpviewer_keywords:
- IHostSemaphore interface [.NET Framework hosting]
ms.assetid: c0765321-656c-441e-bab5-58176292be1e
topic_type:
- apiref
ms.openlocfilehash: 682f1f70925310e93f88f1dc314052e801a5e87b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671342"
---
# <a name="ihostsemaphore-interface"></a><span data-ttu-id="aa8e7-103">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="aa8e7-103">IHostSemaphore Interface</span></span>

<span data-ttu-id="aa8e7-104">表示线程的信号量的主机实现。</span><span class="sxs-lookup"><span data-stu-id="aa8e7-104">Represents the host's implementation of a semaphore for threading.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="aa8e7-105">方法</span><span class="sxs-lookup"><span data-stu-id="aa8e7-105">Methods</span></span>  
  
|<span data-ttu-id="aa8e7-106">方法</span><span class="sxs-lookup"><span data-stu-id="aa8e7-106">Method</span></span>|<span data-ttu-id="aa8e7-107">说明</span><span class="sxs-lookup"><span data-stu-id="aa8e7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="aa8e7-108">ReleaseSemaphore 方法</span><span class="sxs-lookup"><span data-stu-id="aa8e7-108">ReleaseSemaphore Method</span></span>](ihostsemaphore-releasesemaphore-method.md)|<span data-ttu-id="aa8e7-109">`IHostSemaphore`按指定量增加当前实例的计数。</span><span class="sxs-lookup"><span data-stu-id="aa8e7-109">Increases the count of the current `IHostSemaphore` instance by the specified amount.</span></span>|  
|[<span data-ttu-id="aa8e7-110">Wait 方法</span><span class="sxs-lookup"><span data-stu-id="aa8e7-110">Wait Method</span></span>](ihostsemaphore-wait-method.md)|<span data-ttu-id="aa8e7-111">使当前 `IHostSemaphore` 实例等待，直到其拥有或经过指定的时间量。</span><span class="sxs-lookup"><span data-stu-id="aa8e7-111">Causes the current `IHostSemaphore` instance to wait until it is owned or the specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="aa8e7-112">要求</span><span class="sxs-lookup"><span data-stu-id="aa8e7-112">Requirements</span></span>  

 <span data-ttu-id="aa8e7-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="aa8e7-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aa8e7-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="aa8e7-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="aa8e7-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="aa8e7-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="aa8e7-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aa8e7-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa8e7-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="aa8e7-117">See also</span></span>

- [<span data-ttu-id="aa8e7-118">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="aa8e7-118">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="aa8e7-119">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="aa8e7-119">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="aa8e7-120">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="aa8e7-120">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="aa8e7-121">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="aa8e7-121">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
- [<span data-ttu-id="aa8e7-122">承载接口</span><span class="sxs-lookup"><span data-stu-id="aa8e7-122">Hosting Interfaces</span></span>](hosting-interfaces.md)
