---
description: 了解详细信息： ICLRSyncManager 接口
title: ICLRSyncManager 接口
ms.date: 03/30/2017
api_name:
- ICLRSyncManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager
helpviewer_keywords:
- ICLRSyncManager interface [.NET Framework hosting]
ms.assetid: a49f9d80-1c76-4ddd-8c49-34f913a5c596
topic_type:
- apiref
ms.openlocfilehash: 188d1c913d75666aea09b17244012401d377fa10
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784997"
---
# <a name="iclrsyncmanager-interface"></a><span data-ttu-id="52d1a-103">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="52d1a-103">ICLRSyncManager Interface</span></span>

<span data-ttu-id="52d1a-104">定义一些方法，这些方法允许宿主获取有关所请求任务的信息，并检测其同步实现中的死锁。</span><span class="sxs-lookup"><span data-stu-id="52d1a-104">Defines methods that allow the host to get information about requested tasks and to detect deadlocks in its synchronization implementation.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="52d1a-105">方法</span><span class="sxs-lookup"><span data-stu-id="52d1a-105">Methods</span></span>  
  
|<span data-ttu-id="52d1a-106">方法</span><span class="sxs-lookup"><span data-stu-id="52d1a-106">Method</span></span>|<span data-ttu-id="52d1a-107">说明</span><span class="sxs-lookup"><span data-stu-id="52d1a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="52d1a-108">CreateRWLockOwnerIterator 方法</span><span class="sxs-lookup"><span data-stu-id="52d1a-108">CreateRWLockOwnerIterator Method</span></span>](iclrsyncmanager-createrwlockowneriterator-method.md)|<span data-ttu-id="52d1a-109">请求公共语言运行时 (CLR) 为主机创建迭代器，以用于确定等待读取器-编写器锁的任务集。</span><span class="sxs-lookup"><span data-stu-id="52d1a-109">Requests that the common language runtime (CLR) create an iterator for the host to use to determine the set of tasks waiting on a reader-writer lock.</span></span>|  
|[<span data-ttu-id="52d1a-110">DeleteRWLockOwnerIterator 方法</span><span class="sxs-lookup"><span data-stu-id="52d1a-110">DeleteRWLockOwnerIterator Method</span></span>](iclrsyncmanager-deleterwlockowneriterator-method.md)|<span data-ttu-id="52d1a-111">请求 CLR 销毁通过调用创建的迭代器 `CreateRWLockOwnerIterator` 。</span><span class="sxs-lookup"><span data-stu-id="52d1a-111">Requests that the CLR destroy an iterator that was created by a call to `CreateRWLockOwnerIterator`.</span></span>|  
|[<span data-ttu-id="52d1a-112">GetMonitorOwner 方法</span><span class="sxs-lookup"><span data-stu-id="52d1a-112">GetMonitorOwner Method</span></span>](iclrsyncmanager-getmonitorowner-method.md)|<span data-ttu-id="52d1a-113">获取拥有指定监视器的任务。</span><span class="sxs-lookup"><span data-stu-id="52d1a-113">Gets the task that owns the specified monitor.</span></span>|  
|[<span data-ttu-id="52d1a-114">GetRWLockOwnerNext 方法</span><span class="sxs-lookup"><span data-stu-id="52d1a-114">GetRWLockOwnerNext Method</span></span>](iclrsyncmanager-getrwlockownernext-method.md)|<span data-ttu-id="52d1a-115">获取正在等待当前读取器-编写器锁的下一个任务。</span><span class="sxs-lookup"><span data-stu-id="52d1a-115">Gets the next task that is waiting on the current reader-writer lock.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="52d1a-116">要求</span><span class="sxs-lookup"><span data-stu-id="52d1a-116">Requirements</span></span>  

 <span data-ttu-id="52d1a-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="52d1a-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="52d1a-118">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="52d1a-118">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="52d1a-119">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="52d1a-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="52d1a-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="52d1a-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="52d1a-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="52d1a-121">See also</span></span>

- <xref:System.Threading.Thread>
- [<span data-ttu-id="52d1a-122">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="52d1a-122">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
- <span data-ttu-id="52d1a-123">[托管和非托管线程处理](/previous-versions/dotnet/netframework-4.0/5s8ee185(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="52d1a-123">[Managed and Unmanaged Threading](/previous-versions/dotnet/netframework-4.0/5s8ee185(v=vs.100))</span></span>
- [<span data-ttu-id="52d1a-124">承载接口</span><span class="sxs-lookup"><span data-stu-id="52d1a-124">Hosting Interfaces</span></span>](hosting-interfaces.md)
