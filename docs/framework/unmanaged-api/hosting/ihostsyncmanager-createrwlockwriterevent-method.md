---
description: 了解详细信息： IHostSyncManager：： CreateRWLockWriterEvent 方法
title: IHostSyncManager::CreateRWLockWriterEvent 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateRWLockWriterEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateRWLockWriterEvent
helpviewer_keywords:
- CreateRWLockWriterEvent method [.NET Framework hosting]
- IHostSyncManager::CreateRWLockWriterEvent method [.NET Framework hosting]
ms.assetid: 70e488c2-cf53-4dc0-ba52-74372d215c41
topic_type:
- apiref
ms.openlocfilehash: 509f18ff49966e5da3a25e39258d33caf69249a0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784751"
---
# <a name="ihostsyncmanagercreaterwlockwriterevent-method"></a><span data-ttu-id="fe50a-103">IHostSyncManager::CreateRWLockWriterEvent 方法</span><span class="sxs-lookup"><span data-stu-id="fe50a-103">IHostSyncManager::CreateRWLockWriterEvent Method</span></span>

<span data-ttu-id="fe50a-104">创建自动重置事件对象，以便实现编写器锁。</span><span class="sxs-lookup"><span data-stu-id="fe50a-104">Creates an auto-reset event object for the implementation of a writer lock.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe50a-105">语法</span><span class="sxs-lookup"><span data-stu-id="fe50a-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateRWLockWriterEvent (  
    [in]  SIZE_T cookie,  
    [out] IHostAutoEvent **ppEvent  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fe50a-106">参数</span><span class="sxs-lookup"><span data-stu-id="fe50a-106">Parameters</span></span>  

 `cookie`  
 <span data-ttu-id="fe50a-107">中与自动重置事件关联的 cookie。</span><span class="sxs-lookup"><span data-stu-id="fe50a-107">[in] A cookie to associate with the auto-reset event.</span></span>  
  
 `ppEvent`  
 <span data-ttu-id="fe50a-108">弄指向 [IHostAutoEvent](ihostautoevent-interface.md) 实例的地址的指针; 如果无法创建事件对象，则为 null。</span><span class="sxs-lookup"><span data-stu-id="fe50a-108">[out] A pointer to the address of an [IHostAutoEvent](ihostautoevent-interface.md) instance, or null if the event object could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fe50a-109">返回值</span><span class="sxs-lookup"><span data-stu-id="fe50a-109">Return Value</span></span>  
  
|<span data-ttu-id="fe50a-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fe50a-110">HRESULT</span></span>|<span data-ttu-id="fe50a-111">说明</span><span class="sxs-lookup"><span data-stu-id="fe50a-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fe50a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe50a-112">S_OK</span></span>|<span data-ttu-id="fe50a-113">`CreateRWLockWriterEvent` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="fe50a-113">`CreateRWLockWriterEvent` returned successfully.</span></span>|  
|<span data-ttu-id="fe50a-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="fe50a-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="fe50a-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="fe50a-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="fe50a-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="fe50a-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="fe50a-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="fe50a-117">The call timed out.</span></span>|  
|<span data-ttu-id="fe50a-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="fe50a-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="fe50a-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="fe50a-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="fe50a-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="fe50a-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="fe50a-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="fe50a-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="fe50a-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="fe50a-122">E_FAIL</span></span>|<span data-ttu-id="fe50a-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="fe50a-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="fe50a-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="fe50a-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="fe50a-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="fe50a-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="fe50a-126">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="fe50a-126">E_OUTOFMEMORY</span></span>|<span data-ttu-id="fe50a-127">没有足够的内存可用于创建请求的事件对象。</span><span class="sxs-lookup"><span data-stu-id="fe50a-127">Not enough memory was available to create the requested event object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fe50a-128">备注</span><span class="sxs-lookup"><span data-stu-id="fe50a-128">Remarks</span></span>  

 <span data-ttu-id="fe50a-129">CLR 调用 `CreateRWLockWriterEvent` 方法来获取对实例的引用 `IHostAutoEvent` ，以便在它的编写器锁实现中使用。</span><span class="sxs-lookup"><span data-stu-id="fe50a-129">The CLR calls the `CreateRWLockWriterEvent` method to get a reference to an `IHostAutoEvent` instance to use in its implementation of a writer lock.</span></span> <span data-ttu-id="fe50a-130">主机可以通过调用 [ICLRSyncManager](iclrsyncmanager-interface.md) 接口的迭代方法，使用指定的 cookie 来确定哪些任务正在等待锁定。</span><span class="sxs-lookup"><span data-stu-id="fe50a-130">The host can use the specified cookie to determine which tasks are waiting on the lock by calling the iteration methods of the [ICLRSyncManager](iclrsyncmanager-interface.md) interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe50a-131">要求</span><span class="sxs-lookup"><span data-stu-id="fe50a-131">Requirements</span></span>  

 <span data-ttu-id="fe50a-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fe50a-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe50a-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="fe50a-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fe50a-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fe50a-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fe50a-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe50a-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe50a-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="fe50a-136">See also</span></span>

- [<span data-ttu-id="fe50a-137">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="fe50a-137">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="fe50a-138">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="fe50a-138">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="fe50a-139">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="fe50a-139">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="fe50a-140">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="fe50a-140">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
