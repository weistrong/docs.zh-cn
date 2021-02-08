---
description: 了解详细信息： IHostAutoEvent 接口
title: IHostAutoEvent 接口
ms.date: 03/30/2017
api_name:
- IHostAutoEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAutoEvent
helpviewer_keywords:
- IHostAutoEvent interface [.NET Framework hosting]
ms.assetid: 6c1d15c1-a80a-4ee9-b1e4-6e859db6575a
topic_type:
- apiref
ms.openlocfilehash: 4aea282dbe2067d50214b237650ba01fb8bf22a7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789484"
---
# <a name="ihostautoevent-interface"></a><span data-ttu-id="56cdb-103">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="56cdb-103">IHostAutoEvent Interface</span></span>

<span data-ttu-id="56cdb-104">提供宿主自动重置事件的实现的表示形式。</span><span class="sxs-lookup"><span data-stu-id="56cdb-104">Provides a representation of the host's implementation of an auto-reset event.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="56cdb-105">方法</span><span class="sxs-lookup"><span data-stu-id="56cdb-105">Methods</span></span>  
  
|<span data-ttu-id="56cdb-106">方法</span><span class="sxs-lookup"><span data-stu-id="56cdb-106">Method</span></span>|<span data-ttu-id="56cdb-107">说明</span><span class="sxs-lookup"><span data-stu-id="56cdb-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="56cdb-108">Set 方法</span><span class="sxs-lookup"><span data-stu-id="56cdb-108">Set Method</span></span>](ihostautoevent-set-method.md)|<span data-ttu-id="56cdb-109">将当前 `IHostAutoEvent` 实例设置为终止状态。</span><span class="sxs-lookup"><span data-stu-id="56cdb-109">Sets the current `IHostAutoEvent` instance to a signaled state.</span></span>|  
|[<span data-ttu-id="56cdb-110">Wait 方法</span><span class="sxs-lookup"><span data-stu-id="56cdb-110">Wait Method</span></span>](ihostautoevent-wait-method.md)|<span data-ttu-id="56cdb-111">导致当前 `IHostAutoEvent` 实例等待，直到事件拥有或经过指定的时间量。</span><span class="sxs-lookup"><span data-stu-id="56cdb-111">Causes the current `IHostAutoEvent` instance to wait until the event is owned or a specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="56cdb-112">要求</span><span class="sxs-lookup"><span data-stu-id="56cdb-112">Requirements</span></span>  

 <span data-ttu-id="56cdb-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="56cdb-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="56cdb-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="56cdb-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="56cdb-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="56cdb-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="56cdb-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="56cdb-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56cdb-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="56cdb-117">See also</span></span>

- [<span data-ttu-id="56cdb-118">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="56cdb-118">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="56cdb-119">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="56cdb-119">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="56cdb-120">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="56cdb-120">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
- [<span data-ttu-id="56cdb-121">承载接口</span><span class="sxs-lookup"><span data-stu-id="56cdb-121">Hosting Interfaces</span></span>](hosting-interfaces.md)
