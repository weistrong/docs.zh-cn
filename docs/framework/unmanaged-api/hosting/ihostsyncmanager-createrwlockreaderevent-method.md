---
description: 了解详细信息： IHostSyncManager：： CreateRWLockReaderEvent 方法
title: IHostSyncManager::CreateRWLockReaderEvent 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateRWLockReaderEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateRWLockReaderEvent
helpviewer_keywords:
- CreateRWLockReaderEvent method [.NET Framework hosting]
- IHostSyncManager::CreateRWLockReaderEvent method [.NET Framework hosting]
ms.assetid: 68c4ea19-c47c-45c6-b420-d3a2ba1c2d50
topic_type:
- apiref
ms.openlocfilehash: be20757924aa45d2a44edab9bf921026aa0247a5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784764"
---
# <a name="ihostsyncmanagercreaterwlockreaderevent-method"></a><span data-ttu-id="17675-103">IHostSyncManager::CreateRWLockReaderEvent 方法</span><span class="sxs-lookup"><span data-stu-id="17675-103">IHostSyncManager::CreateRWLockReaderEvent Method</span></span>

<span data-ttu-id="17675-104">创建手动重置的事件对象，以便实现读取器锁。</span><span class="sxs-lookup"><span data-stu-id="17675-104">Creates a manual-reset event object for the implementation of a reader lock.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="17675-105">语法</span><span class="sxs-lookup"><span data-stu-id="17675-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateRWLockReaderEvent (  
    [in]  BOOL bInitialState,  
    [in]  SIZE_T cookie,  
    [out] IHostManualEvent **ppEvent  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="17675-106">参数</span><span class="sxs-lookup"><span data-stu-id="17675-106">Parameters</span></span>  

 `bInitialState`  
 <span data-ttu-id="17675-107">[in] `true` ，如果 `ppEvent` 应收到信号，则为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="17675-107">[in] `true`, if `ppEvent` should be signaled; otherwise, `false`.</span></span>  
  
 `cookie`  
 <span data-ttu-id="17675-108">中与读取器锁关联的 cookie。</span><span class="sxs-lookup"><span data-stu-id="17675-108">[in] A cookie to associate with the reader lock.</span></span>  
  
 `ppEvent`  
 <span data-ttu-id="17675-109">弄指向 [IHostManualEvent](ihostmanualevent-interface.md) 实例的地址的指针; 如果无法创建事件对象，则为 null。</span><span class="sxs-lookup"><span data-stu-id="17675-109">[out] A pointer to the address of an [IHostManualEvent](ihostmanualevent-interface.md) instance, or null if the event object could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="17675-110">返回值</span><span class="sxs-lookup"><span data-stu-id="17675-110">Return Value</span></span>  
  
|<span data-ttu-id="17675-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="17675-111">HRESULT</span></span>|<span data-ttu-id="17675-112">说明</span><span class="sxs-lookup"><span data-stu-id="17675-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="17675-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="17675-113">S_OK</span></span>|<span data-ttu-id="17675-114">`CreateRWLockReaderEvent` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="17675-114">`CreateRWLockReaderEvent` returned successfully.</span></span>|  
|<span data-ttu-id="17675-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="17675-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="17675-116"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="17675-116">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="17675-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="17675-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="17675-118">调用超时。</span><span class="sxs-lookup"><span data-stu-id="17675-118">The call timed out.</span></span>|  
|<span data-ttu-id="17675-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="17675-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="17675-120">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="17675-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="17675-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="17675-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="17675-122">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="17675-122">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="17675-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="17675-123">E_FAIL</span></span>|<span data-ttu-id="17675-124">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="17675-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="17675-125">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="17675-125">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="17675-126">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="17675-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="17675-127">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="17675-127">E_OUTOFMEMORY</span></span>|<span data-ttu-id="17675-128">没有足够的内存可用于创建请求的事件对象。</span><span class="sxs-lookup"><span data-stu-id="17675-128">Not enough memory was available to create the requested event object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="17675-129">备注</span><span class="sxs-lookup"><span data-stu-id="17675-129">Remarks</span></span>  

 <span data-ttu-id="17675-130">CLR 调用 `CreateRWLockReaderEvent` 来获取对要 `IHostManualEvent` 在其实现读取器锁实现中使用的实例的引用。</span><span class="sxs-lookup"><span data-stu-id="17675-130">The CLR calls `CreateRWLockReaderEvent` to get a reference to an `IHostManualEvent` instance to use in its implementation of a reader lock.</span></span> <span data-ttu-id="17675-131">主机可以使用 cookie 来确定哪些任务正在等待读取器锁（通过查询 [ICLRSyncManager](iclrsyncmanager-interface.md) 接口）。</span><span class="sxs-lookup"><span data-stu-id="17675-131">The host can use the cookie to determine which tasks are waiting on the reader lock by querying the [ICLRSyncManager](iclrsyncmanager-interface.md) interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="17675-132">要求</span><span class="sxs-lookup"><span data-stu-id="17675-132">Requirements</span></span>  

 <span data-ttu-id="17675-133">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="17675-133">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="17675-134">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="17675-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="17675-135">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="17675-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="17675-136">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="17675-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="17675-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="17675-137">See also</span></span>

- [<span data-ttu-id="17675-138">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="17675-138">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)
- [<span data-ttu-id="17675-139">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="17675-139">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)
- [<span data-ttu-id="17675-140">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="17675-140">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)
- [<span data-ttu-id="17675-141">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="17675-141">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
