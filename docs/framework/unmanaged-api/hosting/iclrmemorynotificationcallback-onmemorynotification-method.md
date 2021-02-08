---
description: 了解详细信息： ICLRMemoryNotificationCallback：： OnMemoryNotification 方法
title: ICLRMemoryNotificationCallback::OnMemoryNotification 方法
ms.date: 03/30/2017
api_name:
- ICLRMemoryNotificationCallback.OnMemoryNotification
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMemoryNotificationCallback::OnMemoryNotification
helpviewer_keywords:
- ICLRMemoryNotificationCallback::OnMemoryNotification method [.NET Framework hosting]
- OnMemoryNotification method [.NET Framework hosting]
ms.assetid: 5612a44d-56cc-4f34-af31-8c9809ba9431
topic_type:
- apiref
ms.openlocfilehash: 92041c433fa82bb63afda7968eb8c6e1fa72acb3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789899"
---
# <a name="iclrmemorynotificationcallbackonmemorynotification-method"></a><span data-ttu-id="bcf1c-103">ICLRMemoryNotificationCallback::OnMemoryNotification 方法</span><span class="sxs-lookup"><span data-stu-id="bcf1c-103">ICLRMemoryNotificationCallback::OnMemoryNotification Method</span></span>

<span data-ttu-id="bcf1c-104"> (CLR) 计算机上的内存负载通知公共语言运行时。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-104">Notifies the common language runtime (CLR) of the memory load on the computer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bcf1c-105">语法</span><span class="sxs-lookup"><span data-stu-id="bcf1c-105">Syntax</span></span>  
  
```cpp  
HRESULT OnMemoryNotification (  
    [in] EMemoryAvailable eMemoryAvailable  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bcf1c-106">参数</span><span class="sxs-lookup"><span data-stu-id="bcf1c-106">Parameters</span></span>  

 `eMemoryAvailable`  
 <span data-ttu-id="bcf1c-107">中 [EMemoryAvailable](ememoryavailable-enumeration.md) 值之一，指示计算机当前遇到的内存压力。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-107">[in] One of the [EMemoryAvailable](ememoryavailable-enumeration.md) values, indicating the memory pressure the computer is currently experiencing.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bcf1c-108">返回值</span><span class="sxs-lookup"><span data-stu-id="bcf1c-108">Return Value</span></span>  
  
|<span data-ttu-id="bcf1c-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bcf1c-109">HRESULT</span></span>|<span data-ttu-id="bcf1c-110">说明</span><span class="sxs-lookup"><span data-stu-id="bcf1c-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bcf1c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="bcf1c-111">S_OK</span></span>|<span data-ttu-id="bcf1c-112">`OnMemoryNotification` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-112">`OnMemoryNotification` returned successfully.</span></span>|  
|<span data-ttu-id="bcf1c-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bcf1c-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bcf1c-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bcf1c-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bcf1c-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bcf1c-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-116">The call timed out.</span></span>|  
|<span data-ttu-id="bcf1c-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bcf1c-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bcf1c-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bcf1c-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bcf1c-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bcf1c-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="bcf1c-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bcf1c-121">E_FAIL</span></span>|<span data-ttu-id="bcf1c-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bcf1c-123">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-123">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bcf1c-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bcf1c-125">备注</span><span class="sxs-lookup"><span data-stu-id="bcf1c-125">Remarks</span></span>  

 <span data-ttu-id="bcf1c-126">CLR `OnMemoryNotification` 使用对 [IHostMemoryManager：： RegisterMemoryNotificationCallback](ihostmemorymanager-registermemorynotificationcallback-method.md) 方法的调用向注册回调。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-126">The CLR registers a callback to `OnMemoryNotification` by using a call to the [IHostMemoryManager::RegisterMemoryNotificationCallback](ihostmemorymanager-registermemorynotificationcallback-method.md) method.</span></span> <span data-ttu-id="bcf1c-127">当主机报告内存资源不足时，运行时将使用在回调中返回的信息来释放额外内存。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-127">The runtime uses the information returned in the callback to free additional memory when the host reports that memory resources are running low.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="bcf1c-128">对 `OnMemoryNotification` 从不阻止的的调用。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-128">Calls to `OnMemoryNotification` never block.</span></span> <span data-ttu-id="bcf1c-129">它们始终立即返回。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-129">They always return immediately.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bcf1c-130">要求</span><span class="sxs-lookup"><span data-stu-id="bcf1c-130">Requirements</span></span>  

 <span data-ttu-id="bcf1c-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bcf1c-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bcf1c-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="bcf1c-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bcf1c-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bcf1c-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bcf1c-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bcf1c-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bcf1c-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="bcf1c-135">See also</span></span>

- [<span data-ttu-id="bcf1c-136">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="bcf1c-136">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
- [<span data-ttu-id="bcf1c-137">RegisterMemoryNotificationCallback 方法</span><span class="sxs-lookup"><span data-stu-id="bcf1c-137">RegisterMemoryNotificationCallback Method</span></span>](ihostmemorymanager-registermemorynotificationcallback-method.md)
- [<span data-ttu-id="bcf1c-138">ICLRMemoryNotificationCallback 接口</span><span class="sxs-lookup"><span data-stu-id="bcf1c-138">ICLRMemoryNotificationCallback Interface</span></span>](iclrmemorynotificationcallback-interface.md)
