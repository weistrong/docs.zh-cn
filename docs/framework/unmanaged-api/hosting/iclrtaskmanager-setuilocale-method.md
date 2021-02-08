---
description: 了解详细信息： ICLRTaskManager：： SetUILocale 方法
title: ICLRTaskManager::SetUILocale 方法
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.SetUILocale
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::SetUILocale
helpviewer_keywords:
- ICLRTaskManager::SetUILocale method [.NET Framework hosting]
- SetUILocale method, ICLRTaskManager interface [.NET Framework hosting]
ms.assetid: 03adaa9a-2beb-49b3-b2c4-6b4fc3f10715
topic_type:
- apiref
ms.openlocfilehash: f4fcc916c520489bd1e39f6a44bc1bb971df4bba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799455"
---
# <a name="iclrtaskmanagersetuilocale-method"></a><span data-ttu-id="da9c5-103">ICLRTaskManager::SetUILocale 方法</span><span class="sxs-lookup"><span data-stu-id="da9c5-103">ICLRTaskManager::SetUILocale Method</span></span>

<span data-ttu-id="da9c5-104">通知公共语言运行时 (CLR) 宿主已修改当前正在执行的任务的用户界面 (UI) 区域设置或区域性）。</span><span class="sxs-lookup"><span data-stu-id="da9c5-104">Notifies the common language runtime (CLR) that the host has modified the user interface (UI) locale, or culture, on the currently executing task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da9c5-105">语法</span><span class="sxs-lookup"><span data-stu-id="da9c5-105">Syntax</span></span>  
  
```cpp  
HRESULT SetUILocale (  
    [in] LCID lcid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="da9c5-106">参数</span><span class="sxs-lookup"><span data-stu-id="da9c5-106">Parameters</span></span>  

 `lcid`  
 <span data-ttu-id="da9c5-107">中区域设置标识符值，用于映射到新分配的用户界面的地理区域和语言。</span><span class="sxs-lookup"><span data-stu-id="da9c5-107">[in] The locale identifier value that maps to the newly assigned geographical culture and language for the user interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="da9c5-108">返回值</span><span class="sxs-lookup"><span data-stu-id="da9c5-108">Return Value</span></span>  
  
|<span data-ttu-id="da9c5-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="da9c5-109">HRESULT</span></span>|<span data-ttu-id="da9c5-110">说明</span><span class="sxs-lookup"><span data-stu-id="da9c5-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="da9c5-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="da9c5-111">S_OK</span></span>|<span data-ttu-id="da9c5-112">`SetUILocale` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="da9c5-112">`SetUILocale` returned successfully.</span></span>|  
|<span data-ttu-id="da9c5-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="da9c5-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="da9c5-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="da9c5-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="da9c5-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="da9c5-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="da9c5-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="da9c5-116">The call timed out.</span></span>|  
|<span data-ttu-id="da9c5-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="da9c5-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="da9c5-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="da9c5-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="da9c5-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="da9c5-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="da9c5-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="da9c5-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="da9c5-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="da9c5-121">E_FAIL</span></span>|<span data-ttu-id="da9c5-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="da9c5-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="da9c5-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="da9c5-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="da9c5-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="da9c5-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="da9c5-125">备注</span><span class="sxs-lookup"><span data-stu-id="da9c5-125">Remarks</span></span>  

 <span data-ttu-id="da9c5-126">`SetUILocale` 为宿主提供对区域设置同步所需的任何机制的机会。</span><span class="sxs-lookup"><span data-stu-id="da9c5-126">`SetUILocale` provides an opportunity for the host to execute any mechanisms it might have for the synchronization of locales.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="da9c5-127">要求</span><span class="sxs-lookup"><span data-stu-id="da9c5-127">Requirements</span></span>  

 <span data-ttu-id="da9c5-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="da9c5-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="da9c5-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="da9c5-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="da9c5-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="da9c5-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="da9c5-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="da9c5-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da9c5-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="da9c5-132">See also</span></span>

- [<span data-ttu-id="da9c5-133">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="da9c5-133">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="da9c5-134">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="da9c5-134">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="da9c5-135">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="da9c5-135">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="da9c5-136">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="da9c5-136">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
