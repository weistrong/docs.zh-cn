---
description: 了解详细信息： IHostGCManager 接口
title: IHostGCManager 接口
ms.date: 03/30/2017
api_name:
- IHostGCManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostGCManager
helpviewer_keywords:
- IHostGCManager interface [.NET Framework hosting]
ms.assetid: 820330a4-244c-4f67-ab5e-f24b0b3c2080
topic_type:
- apiref
ms.openlocfilehash: da229c04eb5f5a27c34c133b5c88183d00f47c40
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708653"
---
# <a name="ihostgcmanager-interface"></a><span data-ttu-id="f1bd5-103">IHostGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="f1bd5-103">IHostGCManager Interface</span></span>

<span data-ttu-id="f1bd5-104">提供一些方法，这些方法用来通知由公共语言运行时 (CLR) 实现的垃圾回收机制中的事件宿主。</span><span class="sxs-lookup"><span data-stu-id="f1bd5-104">Provides methods that notify the host of events in the garbage collection mechanism implemented by the common language runtime (CLR).</span></span>  
  
## <a name="members"></a><span data-ttu-id="f1bd5-105">成员</span><span class="sxs-lookup"><span data-stu-id="f1bd5-105">Members</span></span>  
  
|<span data-ttu-id="f1bd5-106">成员</span><span class="sxs-lookup"><span data-stu-id="f1bd5-106">Member</span></span>|<span data-ttu-id="f1bd5-107">说明</span><span class="sxs-lookup"><span data-stu-id="f1bd5-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f1bd5-108">SuspensionEnding 方法</span><span class="sxs-lookup"><span data-stu-id="f1bd5-108">SuspensionEnding Method</span></span>](ihostgcmanager-suspensionending-method.md)|<span data-ttu-id="f1bd5-109">通知宿主 CLR 正在继续执行已挂起垃圾回收的线程上的任务。</span><span class="sxs-lookup"><span data-stu-id="f1bd5-109">Notifies the host that the CLR is resuming execution of tasks on threads that had been suspended for a garbage collection.</span></span>|  
|[<span data-ttu-id="f1bd5-110">SuspensionStarting 方法</span><span class="sxs-lookup"><span data-stu-id="f1bd5-110">SuspensionStarting Method</span></span>](ihostgcmanager-suspensionstarting-method.md)|<span data-ttu-id="f1bd5-111">通知宿主 CLR 正在暂停执行任务，以执行垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="f1bd5-111">Notifies the host that the CLR is suspending execution of tasks, to perform a garbage collection.</span></span>|  
|[<span data-ttu-id="f1bd5-112">ThreadIsBlockingForSuspension 方法</span><span class="sxs-lookup"><span data-stu-id="f1bd5-112">ThreadIsBlockingForSuspension Method</span></span>](ihostgcmanager-threadisblockingforsuspension-method.md)|<span data-ttu-id="f1bd5-113">通知宿主从中发出方法调用的线程将要阻止垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="f1bd5-113">Notifies the host that the thread from which the method call was made is about to block for a garbage collection.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f1bd5-114">要求</span><span class="sxs-lookup"><span data-stu-id="f1bd5-114">Requirements</span></span>  

 <span data-ttu-id="f1bd5-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f1bd5-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f1bd5-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f1bd5-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f1bd5-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f1bd5-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f1bd5-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f1bd5-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1bd5-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="f1bd5-119">See also</span></span>

- [<span data-ttu-id="f1bd5-120">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="f1bd5-120">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="f1bd5-121">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="f1bd5-121">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="f1bd5-122">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="f1bd5-122">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="f1bd5-123">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="f1bd5-123">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="f1bd5-124">承载接口</span><span class="sxs-lookup"><span data-stu-id="f1bd5-124">Hosting Interfaces</span></span>](hosting-interfaces.md)
