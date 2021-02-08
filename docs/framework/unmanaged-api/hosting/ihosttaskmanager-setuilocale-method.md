---
description: 了解详细信息： IHostTaskManager：： SetUILocale 方法
title: IHostTaskManager::SetUILocale 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.SetUILocale
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::SetUILocale
helpviewer_keywords:
- SetUILocale method, IHostTaskManager interface [.NET Framework hosting]
- IHostTaskManager::SetUILocale method [.NET Framework hosting]
ms.assetid: d0c87a9c-ea81-4237-a16b-c22b36ec9dc8
topic_type:
- apiref
ms.openlocfilehash: 0b81f127c6afb64670424a05db6cc57c4918396a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789380"
---
# <a name="ihosttaskmanagersetuilocale-method"></a><span data-ttu-id="ccf91-103">IHostTaskManager::SetUILocale 方法</span><span class="sxs-lookup"><span data-stu-id="ccf91-103">IHostTaskManager::SetUILocale Method</span></span>

<span data-ttu-id="ccf91-104">向宿主通知公共语言运行时 (CLR) 已更改当前正在执行的任务的用户界面 (UI) 区域设置或区域性。</span><span class="sxs-lookup"><span data-stu-id="ccf91-104">Notifies the host that the common language runtime (CLR) has changed the user interface (UI) locale, or culture, on the currently executing task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ccf91-105">语法</span><span class="sxs-lookup"><span data-stu-id="ccf91-105">Syntax</span></span>  
  
```cpp  
HRESULT SetUILocale (  
    [in] LCID lcid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ccf91-106">参数</span><span class="sxs-lookup"><span data-stu-id="ccf91-106">Parameters</span></span>  

 `lcid`  
 <span data-ttu-id="ccf91-107">中映射到新分配的地理区域和语言的区域设置标识符值。</span><span class="sxs-lookup"><span data-stu-id="ccf91-107">[in] The locale identifier value that maps to the newly assigned geographical culture and language.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ccf91-108">返回值</span><span class="sxs-lookup"><span data-stu-id="ccf91-108">Return Value</span></span>  
  
|<span data-ttu-id="ccf91-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ccf91-109">HRESULT</span></span>|<span data-ttu-id="ccf91-110">说明</span><span class="sxs-lookup"><span data-stu-id="ccf91-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ccf91-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccf91-111">S_OK</span></span>|<span data-ttu-id="ccf91-112">`SetUILocale` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ccf91-112">`SetUILocale` returned successfully.</span></span>|  
|<span data-ttu-id="ccf91-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ccf91-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ccf91-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ccf91-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ccf91-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ccf91-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ccf91-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ccf91-116">The call timed out.</span></span>|  
|<span data-ttu-id="ccf91-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ccf91-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ccf91-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ccf91-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ccf91-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ccf91-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ccf91-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ccf91-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ccf91-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ccf91-121">E_FAIL</span></span>|<span data-ttu-id="ccf91-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ccf91-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ccf91-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ccf91-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ccf91-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ccf91-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="ccf91-125">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="ccf91-125">E_NOTIMPL</span></span>|<span data-ttu-id="ccf91-126">宿主不允许托管用户代码更改 UI 区域性。</span><span class="sxs-lookup"><span data-stu-id="ccf91-126">The host does not allow managed user code to change the UI culture.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ccf91-127">备注</span><span class="sxs-lookup"><span data-stu-id="ccf91-127">Remarks</span></span>  

 <span data-ttu-id="ccf91-128">`SetUILocale`当 <xref:System.Threading.Thread.CurrentUICulture%2A?displayProperty=nameWithType> 托管代码更改属性的值时，运行时调用。</span><span class="sxs-lookup"><span data-stu-id="ccf91-128">The runtime calls `SetUILocale` when the value of the <xref:System.Threading.Thread.CurrentUICulture%2A?displayProperty=nameWithType> property is changed by managed code.</span></span> <span data-ttu-id="ccf91-129">此方法为主机提供了对区域设置同步所需的任何机制的机会。</span><span class="sxs-lookup"><span data-stu-id="ccf91-129">This method provides an opportunity for the host to execute any mechanisms it might have for synchronization of locales.</span></span> <span data-ttu-id="ccf91-130">如果主机不允许从托管代码更改 UI 区域设置，或未实现同步区域设置的机制，则它应从此方法返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="ccf91-130">If a host does not allow the UI locale to be changed from managed code, or does not implement a mechanism to synchronize locales, it should return E_NOTIMPL from this method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ccf91-131">要求</span><span class="sxs-lookup"><span data-stu-id="ccf91-131">Requirements</span></span>  

 <span data-ttu-id="ccf91-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ccf91-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ccf91-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ccf91-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ccf91-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ccf91-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ccf91-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ccf91-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ccf91-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="ccf91-136">See also</span></span>

- [<span data-ttu-id="ccf91-137">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="ccf91-137">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="ccf91-138">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="ccf91-138">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="ccf91-139">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="ccf91-139">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="ccf91-140">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="ccf91-140">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
- [<span data-ttu-id="ccf91-141">SetLocale 方法</span><span class="sxs-lookup"><span data-stu-id="ccf91-141">SetLocale Method</span></span>](ihosttaskmanager-setlocale-method.md)
