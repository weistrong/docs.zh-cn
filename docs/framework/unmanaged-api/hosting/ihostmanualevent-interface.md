---
description: 了解详细信息： IHostManualEvent 接口
title: IHostManualEvent 接口
ms.date: 03/30/2017
api_name:
- IHostManualEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostManualEvent
helpviewer_keywords:
- IHostManualEvent interface [.NET Framework hosting]
ms.assetid: 300c2661-b7d1-4c39-b080-9ebdef0fd523
topic_type:
- apiref
ms.openlocfilehash: 1c70935568b9ff4080fd5bcdc372c02d354aa06f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708120"
---
# <a name="ihostmanualevent-interface"></a><span data-ttu-id="9451e-103">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="9451e-103">IHostManualEvent Interface</span></span>

<span data-ttu-id="9451e-104">提供宿主手动重置事件表示形式的实现。</span><span class="sxs-lookup"><span data-stu-id="9451e-104">Provides the host's implementation of a representation of a manual reset event.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9451e-105">方法</span><span class="sxs-lookup"><span data-stu-id="9451e-105">Methods</span></span>  
  
|<span data-ttu-id="9451e-106">方法</span><span class="sxs-lookup"><span data-stu-id="9451e-106">Method</span></span>|<span data-ttu-id="9451e-107">说明</span><span class="sxs-lookup"><span data-stu-id="9451e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9451e-108">Reset 方法</span><span class="sxs-lookup"><span data-stu-id="9451e-108">Reset Method</span></span>](ihostmanualevent-reset-method.md)|<span data-ttu-id="9451e-109">将当前实例重置 `IHostManualEvent` 为非终止状态。</span><span class="sxs-lookup"><span data-stu-id="9451e-109">Resets the current `IHostManualEvent` instance to a non-signaled state.</span></span>|  
|[<span data-ttu-id="9451e-110">Set 方法</span><span class="sxs-lookup"><span data-stu-id="9451e-110">Set Method</span></span>](ihostmanualevent-set-method.md)|<span data-ttu-id="9451e-111">将当前 `IHostManualEvent` 实例设置为终止状态。</span><span class="sxs-lookup"><span data-stu-id="9451e-111">Sets the current `IHostManualEvent` instance to a signaled state.</span></span>|  
|[<span data-ttu-id="9451e-112">Wait 方法</span><span class="sxs-lookup"><span data-stu-id="9451e-112">Wait Method</span></span>](ihostmanualevent-wait-method.md)|<span data-ttu-id="9451e-113">导致当前 `IHostManualEvent` 实例等待，直到其拥有或经过指定的时间量。</span><span class="sxs-lookup"><span data-stu-id="9451e-113">Causes the current `IHostManualEvent` instance to wait until it is owned, or a specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9451e-114">要求</span><span class="sxs-lookup"><span data-stu-id="9451e-114">Requirements</span></span>  

 <span data-ttu-id="9451e-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9451e-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9451e-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9451e-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9451e-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9451e-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9451e-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9451e-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9451e-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="9451e-119">See also</span></span>

- [<span data-ttu-id="9451e-120">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="9451e-120">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="9451e-121">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="9451e-121">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="9451e-122">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="9451e-122">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)
- [<span data-ttu-id="9451e-123">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="9451e-123">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
- [<span data-ttu-id="9451e-124">承载接口</span><span class="sxs-lookup"><span data-stu-id="9451e-124">Hosting Interfaces</span></span>](hosting-interfaces.md)
