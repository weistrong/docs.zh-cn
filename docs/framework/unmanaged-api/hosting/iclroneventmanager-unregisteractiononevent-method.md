---
description: 了解详细信息： ICLROnEventManager：： UnregisterActionOnEvent 方法
title: ICLROnEventManager::UnregisterActionOnEvent 方法
ms.date: 03/30/2017
api_name:
- ICLROnEventManager.UnregisterActionOnEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLROnEventManager::UnregisterActionOnEvent
helpviewer_keywords:
- UnRegisterActionOnEvent method [.NET Framework hosting]
- ICLROnEventManager::UnRegisterActionOnEvent method [.NET Framework hosting]
ms.assetid: 4c02ec37-cdf0-46b2-890e-235092741236
topic_type:
- apiref
ms.openlocfilehash: 8131c58669ff7be0fdc2b2e063c70d3b370921e8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789809"
---
# <a name="iclroneventmanagerunregisteractiononevent-method"></a><span data-ttu-id="844da-103">ICLROnEventManager::UnregisterActionOnEvent 方法</span><span class="sxs-lookup"><span data-stu-id="844da-103">ICLROnEventManager::UnregisterActionOnEvent Method</span></span>

<span data-ttu-id="844da-104">为指定的事件注销先前注册的回调指针。</span><span class="sxs-lookup"><span data-stu-id="844da-104">Unregisters a previously registered callback pointer for the specified event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="844da-105">语法</span><span class="sxs-lookup"><span data-stu-id="844da-105">Syntax</span></span>  
  
```cpp  
HRESULT UnregisterActionOnEvent (  
    [in] EClrEvent event,  
    [in] IActionOnCLREvent *pAction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="844da-106">参数</span><span class="sxs-lookup"><span data-stu-id="844da-106">Parameters</span></span>  

 `event`  
 <span data-ttu-id="844da-107">中 [EClrEvent](eclrevent-enumeration.md) 值之一，指示要撤消注册的回调指针的事件 `pAction` 。</span><span class="sxs-lookup"><span data-stu-id="844da-107">[in] One of the [EClrEvent](eclrevent-enumeration.md) values, indicating the event for which to unregister the callback pointer described by `pAction`.</span></span>  
  
 `pAction`  
 <span data-ttu-id="844da-108">中指向作为参数传递给[RegisterActionOnEvent](iclroneventmanager-registeractiononevent-method.md)方法的[IActionOnCLREvent](iactiononclrevent-interface.md)对象的指针。</span><span class="sxs-lookup"><span data-stu-id="844da-108">[in] A pointer to an [IActionOnCLREvent](iactiononclrevent-interface.md) object that was passed as a parameter to the [RegisterActionOnEvent](iclroneventmanager-registeractiononevent-method.md) method.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="844da-109">返回值</span><span class="sxs-lookup"><span data-stu-id="844da-109">Return Value</span></span>  
  
|<span data-ttu-id="844da-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="844da-110">HRESULT</span></span>|<span data-ttu-id="844da-111">说明</span><span class="sxs-lookup"><span data-stu-id="844da-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="844da-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="844da-112">S_OK</span></span>|<span data-ttu-id="844da-113">`UnregisterActionOnEvent` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="844da-113">`UnregisterActionOnEvent` returned successfully.</span></span>|  
|<span data-ttu-id="844da-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="844da-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="844da-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="844da-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="844da-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="844da-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="844da-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="844da-117">The call timed out.</span></span>|  
|<span data-ttu-id="844da-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="844da-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="844da-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="844da-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="844da-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="844da-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="844da-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="844da-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="844da-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="844da-122">E_FAIL</span></span>|<span data-ttu-id="844da-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="844da-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="844da-124">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="844da-124">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="844da-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="844da-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="844da-126">要求</span><span class="sxs-lookup"><span data-stu-id="844da-126">Requirements</span></span>  

 <span data-ttu-id="844da-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="844da-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="844da-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="844da-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="844da-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="844da-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="844da-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="844da-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="844da-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="844da-131">See also</span></span>

- [<span data-ttu-id="844da-132">EClrEvent 枚举</span><span class="sxs-lookup"><span data-stu-id="844da-132">EClrEvent Enumeration</span></span>](eclrevent-enumeration.md)
- [<span data-ttu-id="844da-133">IActionOnCLREvent 接口</span><span class="sxs-lookup"><span data-stu-id="844da-133">IActionOnCLREvent Interface</span></span>](iactiononclrevent-interface.md)
- [<span data-ttu-id="844da-134">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="844da-134">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="844da-135">ICLROnEventManager 接口</span><span class="sxs-lookup"><span data-stu-id="844da-135">ICLROnEventManager Interface</span></span>](iclroneventmanager-interface.md)
