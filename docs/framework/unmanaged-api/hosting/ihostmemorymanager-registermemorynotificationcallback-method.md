---
description: 了解详细信息： IHostMemoryManager：： RegisterMemoryNotificationCallback 方法
title: IHostMemoryManager::RegisterMemoryNotificationCallback 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.RegisterMemoryNotificationCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::RegisterMemoryNotificationCallback
helpviewer_keywords:
- IHostMemoryManager::RegisterMemoryNotificationCallback method [.NET Framework hosting]
- RegisterMemoryNotificationCallback method [.NET Framework hosting]
ms.assetid: 65d301f6-4dbb-4b5f-8eff-82540e2b6465
topic_type:
- apiref
ms.openlocfilehash: 26a7468aba4f473eebff78a8c67eeb5b3e866e9c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707756"
---
# <a name="ihostmemorymanagerregistermemorynotificationcallback-method"></a><span data-ttu-id="447e5-103">IHostMemoryManager::RegisterMemoryNotificationCallback 方法</span><span class="sxs-lookup"><span data-stu-id="447e5-103">IHostMemoryManager::RegisterMemoryNotificationCallback Method</span></span>

<span data-ttu-id="447e5-104">注册指向主机调用的回调函数的指针，以通知公共语言运行时 (计算机上当前内存负载的 CLR) 。</span><span class="sxs-lookup"><span data-stu-id="447e5-104">Registers a pointer to a callback function that the host invokes to notify the common language runtime (CLR) of the current memory load on the computer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="447e5-105">语法</span><span class="sxs-lookup"><span data-stu-id="447e5-105">Syntax</span></span>  
  
```cpp  
HRESULT RegisterMemoryNotificationCallback (  
    [in] ICLRMemoryNotificationCallback* pCallback  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="447e5-106">参数</span><span class="sxs-lookup"><span data-stu-id="447e5-106">Parameters</span></span>  

 `pCallback`  
 <span data-ttu-id="447e5-107">中一个接口指针，该指针指向由 CLR 实现的 [ICLRMemoryNotificationCallback](iclrmemorynotificationcallback-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="447e5-107">[in] An interface pointer to an [ICLRMemoryNotificationCallback](iclrmemorynotificationcallback-interface.md) instance that is implemented by the CLR.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="447e5-108">返回值</span><span class="sxs-lookup"><span data-stu-id="447e5-108">Return Value</span></span>  
  
|<span data-ttu-id="447e5-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="447e5-109">HRESULT</span></span>|<span data-ttu-id="447e5-110">说明</span><span class="sxs-lookup"><span data-stu-id="447e5-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="447e5-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="447e5-111">S_OK</span></span>|<span data-ttu-id="447e5-112">`RegisterMemoryNotificationCallback` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="447e5-112">`RegisterMemoryNotificationCallback` returned successfully.</span></span>|  
|<span data-ttu-id="447e5-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="447e5-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="447e5-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="447e5-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="447e5-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="447e5-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="447e5-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="447e5-116">The call timed out.</span></span>|  
|<span data-ttu-id="447e5-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="447e5-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="447e5-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="447e5-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="447e5-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="447e5-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="447e5-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="447e5-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="447e5-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="447e5-121">E_FAIL</span></span>|<span data-ttu-id="447e5-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="447e5-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="447e5-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="447e5-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="447e5-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="447e5-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="447e5-125">备注</span><span class="sxs-lookup"><span data-stu-id="447e5-125">Remarks</span></span>  

 <span data-ttu-id="447e5-126">由于 `ICLRMemoryNotificationCallback` 接口仅定义了一个 ([ICLRMemoryNotificationCallback：： OnMemoryNotification](iclrmemorynotificationcallback-onmemorynotification-method.md)) 的方法，并且由于 `pCallback` 是一个指向 `ICLRMemoryNotificationCallback` CLR 提供的实例的指针，因此注册对于回调函数本身是有效的。</span><span class="sxs-lookup"><span data-stu-id="447e5-126">Because the `ICLRMemoryNotificationCallback` interface defines only one method ([ICLRMemoryNotificationCallback::OnMemoryNotification](iclrmemorynotificationcallback-onmemorynotification-method.md)), and because `pCallback` is a pointer to an `ICLRMemoryNotificationCallback` instance provided by the CLR, the registration is effectively for the callback function itself.</span></span> <span data-ttu-id="447e5-127">宿主调用 `OnMemoryNotification` 以报告内存压力条件，而不是使用标准的 Win32 `CreateMemoryResourceNotification` 函数。</span><span class="sxs-lookup"><span data-stu-id="447e5-127">The host invokes `OnMemoryNotification` to report memory pressure conditions, rather than using the standard Win32 `CreateMemoryResourceNotification` function.</span></span> <span data-ttu-id="447e5-128">有关详细信息，请参阅 Windows 平台文档。</span><span class="sxs-lookup"><span data-stu-id="447e5-128">For more information, see the Windows Platform documentation.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="447e5-129">对 `OnMemoryNotification` 从不阻止的的调用。</span><span class="sxs-lookup"><span data-stu-id="447e5-129">Calls to `OnMemoryNotification` never block.</span></span> <span data-ttu-id="447e5-130">它们始终立即返回。</span><span class="sxs-lookup"><span data-stu-id="447e5-130">They always return immediately.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="447e5-131">要求</span><span class="sxs-lookup"><span data-stu-id="447e5-131">Requirements</span></span>  

 <span data-ttu-id="447e5-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="447e5-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="447e5-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="447e5-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="447e5-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="447e5-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="447e5-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="447e5-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="447e5-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="447e5-136">See also</span></span>

- [<span data-ttu-id="447e5-137">ICLRMemoryNotificationCallback 接口</span><span class="sxs-lookup"><span data-stu-id="447e5-137">ICLRMemoryNotificationCallback Interface</span></span>](iclrmemorynotificationcallback-interface.md)
- [<span data-ttu-id="447e5-138">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="447e5-138">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
