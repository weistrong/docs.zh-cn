---
description: 了解详细信息： ICLROnEventManager：： RegisterActionOnEvent 方法
title: ICLROnEventManager::RegisterActionOnEvent 方法
ms.date: 03/30/2017
api_name:
- ICLROnEventManager.RegisterActionOnEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLROnEventManager::RegisterActionOnEvent
helpviewer_keywords:
- ICLROnEventManager::RegisterActionOnEvent method [.NET Framework hosting]
- RegisterActionOnEvent method [.NET Framework hosting]
ms.assetid: b944cf49-918d-4c4e-993b-77d097a52550
topic_type:
- apiref
ms.openlocfilehash: b13209aed6a169185b42c6b9520f21f59f6be3bb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637425"
---
# <a name="iclroneventmanagerregisteractiononevent-method"></a><span data-ttu-id="238c2-103">ICLROnEventManager::RegisterActionOnEvent 方法</span><span class="sxs-lookup"><span data-stu-id="238c2-103">ICLROnEventManager::RegisterActionOnEvent Method</span></span>

<span data-ttu-id="238c2-104">为指定事件注册回调指针。</span><span class="sxs-lookup"><span data-stu-id="238c2-104">Registers a callback pointer for the specified event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="238c2-105">语法</span><span class="sxs-lookup"><span data-stu-id="238c2-105">Syntax</span></span>  
  
```cpp  
HRESULT RegisterActionOnEvent (  
    [in] EClrEvent event,  
    [in] IActionOnCLREvent *pAction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="238c2-106">参数</span><span class="sxs-lookup"><span data-stu-id="238c2-106">Parameters</span></span>  

 `event`  
 <span data-ttu-id="238c2-107">中 [EClrEvent](eclrevent-enumeration.md) 值之一，指示要为其注册所描述的回调指针的事件 `pAction` 。</span><span class="sxs-lookup"><span data-stu-id="238c2-107">[in] One of the [EClrEvent](eclrevent-enumeration.md) values, indicating the event for which to register the callback pointer described by `pAction`.</span></span>  
  
 `pAction`  
 <span data-ttu-id="238c2-108">中指向 [IActionOnCLREvent](iactiononclrevent-interface.md) 对象的指针，当注册的事件激发时，将调用该对象。</span><span class="sxs-lookup"><span data-stu-id="238c2-108">[in] A pointer to an [IActionOnCLREvent](iactiononclrevent-interface.md) object that is called when the registered event fires.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="238c2-109">返回值</span><span class="sxs-lookup"><span data-stu-id="238c2-109">Return Value</span></span>  
  
|<span data-ttu-id="238c2-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="238c2-110">HRESULT</span></span>|<span data-ttu-id="238c2-111">说明</span><span class="sxs-lookup"><span data-stu-id="238c2-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="238c2-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="238c2-112">S_OK</span></span>|<span data-ttu-id="238c2-113">`RegisterActionOnEvent` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="238c2-113">`RegisterActionOnEvent` returned successfully.</span></span>|  
|<span data-ttu-id="238c2-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="238c2-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="238c2-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="238c2-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="238c2-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="238c2-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="238c2-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="238c2-117">The call timed out.</span></span>|  
|<span data-ttu-id="238c2-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="238c2-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="238c2-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="238c2-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="238c2-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="238c2-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="238c2-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="238c2-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="238c2-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="238c2-122">E_FAIL</span></span>|<span data-ttu-id="238c2-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="238c2-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="238c2-124">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="238c2-124">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="238c2-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="238c2-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="238c2-126">备注</span><span class="sxs-lookup"><span data-stu-id="238c2-126">Remarks</span></span>  

 <span data-ttu-id="238c2-127">宿主可以为描述的两个事件类型中的一个或两个注册回调 `EClrEvent` 。</span><span class="sxs-lookup"><span data-stu-id="238c2-127">The host can register callbacks for either or both of the two event types described by `EClrEvent`.</span></span> <span data-ttu-id="238c2-128">宿主 `ICLROnEventManager` 通过调用 [ICLRControl：： GetCLRManager](iclrcontrol-getclrmanager-method.md) 方法获取接口。</span><span class="sxs-lookup"><span data-stu-id="238c2-128">The host gets the `ICLROnEventManager` interface by calling the [ICLRControl::GetCLRManager](iclrcontrol-getclrmanager-method.md) method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="238c2-129">注册的事件 `RegisterActionOnEvent` 可以从不同的线程激发一次，以发出卸载或禁用 CLR 的信号。</span><span class="sxs-lookup"><span data-stu-id="238c2-129">The events that `RegisterActionOnEvent` registers can be fired more than once and from different threads to signal an unload or the disabling of the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="238c2-130">要求</span><span class="sxs-lookup"><span data-stu-id="238c2-130">Requirements</span></span>  

 <span data-ttu-id="238c2-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="238c2-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="238c2-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="238c2-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="238c2-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="238c2-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="238c2-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="238c2-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="238c2-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="238c2-135">See also</span></span>

- [<span data-ttu-id="238c2-136">EClrEvent 枚举</span><span class="sxs-lookup"><span data-stu-id="238c2-136">EClrEvent Enumeration</span></span>](eclrevent-enumeration.md)
- [<span data-ttu-id="238c2-137">IActionOnCLREvent 接口</span><span class="sxs-lookup"><span data-stu-id="238c2-137">IActionOnCLREvent Interface</span></span>](iactiononclrevent-interface.md)
- [<span data-ttu-id="238c2-138">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="238c2-138">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="238c2-139">ICLROnEventManager 接口</span><span class="sxs-lookup"><span data-stu-id="238c2-139">ICLROnEventManager Interface</span></span>](iclroneventmanager-interface.md)
