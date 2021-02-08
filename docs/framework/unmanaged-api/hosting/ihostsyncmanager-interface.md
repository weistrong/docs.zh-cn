---
description: 了解详细信息： IHostSyncManager 接口
title: IHostSyncManager 接口
ms.date: 03/30/2017
api_name:
- IHostSyncManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager
helpviewer_keywords:
- IHostSyncManager interface [.NET Framework hosting]
ms.assetid: 2e081a37-6a28-4c93-b7ab-1c96a464637c
topic_type:
- apiref
ms.openlocfilehash: c3bd2928315567605d320c772de8ff824ad3cd09
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784725"
---
# <a name="ihostsyncmanager-interface"></a><span data-ttu-id="de847-103">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="de847-103">IHostSyncManager Interface</span></span>

<span data-ttu-id="de847-104">提供一些方法，使公共语言运行时 (CLR) 通过调用主机而不是使用 Win32 同步函数来创建同步基元。</span><span class="sxs-lookup"><span data-stu-id="de847-104">Provides methods that allow the common language runtime (CLR) to create synchronization primitives by calling the host instead of using the Win32 synchronization functions.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="de847-105">方法</span><span class="sxs-lookup"><span data-stu-id="de847-105">Methods</span></span>  
  
|<span data-ttu-id="de847-106">方法</span><span class="sxs-lookup"><span data-stu-id="de847-106">Method</span></span>|<span data-ttu-id="de847-107">说明</span><span class="sxs-lookup"><span data-stu-id="de847-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="de847-108">CreateAutoEvent 方法</span><span class="sxs-lookup"><span data-stu-id="de847-108">CreateAutoEvent Method</span></span>](ihostsyncmanager-createautoevent-method.md)|<span data-ttu-id="de847-109">创建自动重置事件对象。</span><span class="sxs-lookup"><span data-stu-id="de847-109">Creates an auto-reset event object.</span></span>|  
|[<span data-ttu-id="de847-110">CreateCrst 方法</span><span class="sxs-lookup"><span data-stu-id="de847-110">CreateCrst Method</span></span>](ihostsyncmanager-createcrst-method.md)|<span data-ttu-id="de847-111">创建用于同步的临界区对象。</span><span class="sxs-lookup"><span data-stu-id="de847-111">Creates a critical section object for synchronization.</span></span>|  
|[<span data-ttu-id="de847-112">CreateCrstWithSpinCount 方法</span><span class="sxs-lookup"><span data-stu-id="de847-112">CreateCrstWithSpinCount Method</span></span>](ihostsyncmanager-createcrstwithspincount-method.md)|<span data-ttu-id="de847-113">使用自旋计数为同步创建一个临界区对象。</span><span class="sxs-lookup"><span data-stu-id="de847-113">Creates a critical section object with spin count for synchronization.</span></span>|  
|[<span data-ttu-id="de847-114">CreateManualEvent 方法</span><span class="sxs-lookup"><span data-stu-id="de847-114">CreateManualEvent Method</span></span>](ihostsyncmanager-createmanualevent-method.md)|<span data-ttu-id="de847-115">创建手动重置的事件对象。</span><span class="sxs-lookup"><span data-stu-id="de847-115">Creates a manual-reset event object.</span></span>|  
|[<span data-ttu-id="de847-116">CreateMonitorEvent 方法</span><span class="sxs-lookup"><span data-stu-id="de847-116">CreateMonitorEvent Method</span></span>](ihostsyncmanager-createmonitorevent-method.md)|<span data-ttu-id="de847-117">创建监视的自动重置事件对象。</span><span class="sxs-lookup"><span data-stu-id="de847-117">Creates a monitored auto-reset event object.</span></span>|  
|[<span data-ttu-id="de847-118">CreateRWLockReaderEvent 方法</span><span class="sxs-lookup"><span data-stu-id="de847-118">CreateRWLockReaderEvent Method</span></span>](ihostsyncmanager-createrwlockreaderevent-method.md)|<span data-ttu-id="de847-119">创建手动重置的事件对象，以便实现读取器锁。</span><span class="sxs-lookup"><span data-stu-id="de847-119">Creates a manual-reset event object for the implementation of a reader lock.</span></span>|  
|[<span data-ttu-id="de847-120">CreateRWLockWriterEvent 方法</span><span class="sxs-lookup"><span data-stu-id="de847-120">CreateRWLockWriterEvent Method</span></span>](ihostsyncmanager-createrwlockwriterevent-method.md)|<span data-ttu-id="de847-121">创建自动重置事件对象，以便实现编写器锁。</span><span class="sxs-lookup"><span data-stu-id="de847-121">Creates an auto-reset event object for the implementation of a writer lock.</span></span>|  
|[<span data-ttu-id="de847-122">CreateSemaphore 方法</span><span class="sxs-lookup"><span data-stu-id="de847-122">CreateSemaphore Method</span></span>](ihostsyncmanager-createsemaphore-method.md)|<span data-ttu-id="de847-123">为 CLR 创建一个 [IHostSemaphore](ihostsemaphore-interface.md) 对象，以用作等待事件的信号量。</span><span class="sxs-lookup"><span data-stu-id="de847-123">Creates an [IHostSemaphore](ihostsemaphore-interface.md) object for the CLR to use as a semaphore for wait events.</span></span>|  
|[<span data-ttu-id="de847-124">SetCLRSyncManager 方法</span><span class="sxs-lookup"><span data-stu-id="de847-124">SetCLRSyncManager Method</span></span>](ihostsyncmanager-setclrsyncmanager-method.md)|<span data-ttu-id="de847-125">设置要与当前实例关联的 [ICLRSyncManager](iclrsyncmanager-interface.md) 实例 `IHostSyncManager` 。</span><span class="sxs-lookup"><span data-stu-id="de847-125">Sets the [ICLRSyncManager](iclrsyncmanager-interface.md) instance to associate with the current `IHostSyncManager` instance.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="de847-126">备注</span><span class="sxs-lookup"><span data-stu-id="de847-126">Remarks</span></span>  

 <span data-ttu-id="de847-127">CLR `IHostSyncManager` 通过使用 IID_IHostSyncManager 的调用 [IHostControl：： GetHostManager](ihostcontrol-gethostmanager-method.md) 方法来发现主机的实现 `IID` 。</span><span class="sxs-lookup"><span data-stu-id="de847-127">The CLR discovers the host's implementation of `IHostSyncManager` by calling the [IHostControl::GetHostManager](ihostcontrol-gethostmanager-method.md) method with an `IID` of IID_IHostSyncManager.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="de847-128">要求</span><span class="sxs-lookup"><span data-stu-id="de847-128">Requirements</span></span>  

 <span data-ttu-id="de847-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="de847-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="de847-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="de847-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="de847-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="de847-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="de847-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="de847-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de847-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="de847-133">See also</span></span>

- [<span data-ttu-id="de847-134">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="de847-134">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="de847-135">承载接口</span><span class="sxs-lookup"><span data-stu-id="de847-135">Hosting Interfaces</span></span>](hosting-interfaces.md)
