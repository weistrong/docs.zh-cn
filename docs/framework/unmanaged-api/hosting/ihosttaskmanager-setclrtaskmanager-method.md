---
description: 了解详细信息： IHostTaskManager：： SetCLRTaskManager 方法
title: IHostTaskManager::SetCLRTaskManager 方法
ms.date: 03/30/2017
api_name:
- IHostTaskManager.SetCLRTaskManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::SetCLRTaskManager
helpviewer_keywords:
- IHostTaskManager::SetCLRTaskManager method [.NET Framework hosting]
- SetCLRTaskManager method [.NET Framework hosting]
ms.assetid: ec90ee83-bd4b-408b-9274-62a923ab86a1
topic_type:
- apiref
ms.openlocfilehash: 438a5b56afd42eceafb484bdf0020efbad86d052
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99680866"
---
# <a name="ihosttaskmanagersetclrtaskmanager-method"></a><span data-ttu-id="d841b-103">IHostTaskManager::SetCLRTaskManager 方法</span><span class="sxs-lookup"><span data-stu-id="d841b-103">IHostTaskManager::SetCLRTaskManager Method</span></span>

<span data-ttu-id="d841b-104">向宿主提供一个接口指针，该指针指向由公共语言运行时 (CLR) 实现的 [ICLRTaskManager](iclrtaskmanager-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="d841b-104">Provides the host with an interface pointer to an [ICLRTaskManager](iclrtaskmanager-interface.md) instance implemented by the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d841b-105">语法</span><span class="sxs-lookup"><span data-stu-id="d841b-105">Syntax</span></span>  
  
```cpp  
HRESULT SetCLRTaskManager (  
    [in] ICLRTaskManager *pManager  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d841b-106">参数</span><span class="sxs-lookup"><span data-stu-id="d841b-106">Parameters</span></span>  

 `pManager`  
 <span data-ttu-id="d841b-107">中指向 `ICLRTaskManager` 由公共语言运行时实现的实例的指针。</span><span class="sxs-lookup"><span data-stu-id="d841b-107">[in] A pointer to an `ICLRTaskManager` instance implemented by the common language runtime.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d841b-108">返回值</span><span class="sxs-lookup"><span data-stu-id="d841b-108">Return Value</span></span>  
  
|<span data-ttu-id="d841b-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d841b-109">HRESULT</span></span>|<span data-ttu-id="d841b-110">说明</span><span class="sxs-lookup"><span data-stu-id="d841b-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d841b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="d841b-111">S_OK</span></span>|<span data-ttu-id="d841b-112">`SetCLRTaskManager` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="d841b-112">`SetCLRTaskManager` returned successfully.</span></span>|  
|<span data-ttu-id="d841b-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d841b-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d841b-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="d841b-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d841b-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d841b-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="d841b-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="d841b-116">The call timed out.</span></span>|  
|<span data-ttu-id="d841b-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="d841b-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="d841b-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="d841b-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="d841b-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="d841b-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="d841b-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="d841b-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="d841b-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d841b-121">E_FAIL</span></span>|<span data-ttu-id="d841b-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="d841b-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d841b-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="d841b-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d841b-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="d841b-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d841b-125">备注</span><span class="sxs-lookup"><span data-stu-id="d841b-125">Remarks</span></span>  

 <span data-ttu-id="d841b-126">运行时调用 `SetCLRTaskManager` 来向宿主提供指向实例的接口指针 `ICLRTaskManager` 。</span><span class="sxs-lookup"><span data-stu-id="d841b-126">The runtime calls `SetCLRTaskManager` to provide the host with an interface pointer to an `ICLRTaskManager` instance.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d841b-127">要求</span><span class="sxs-lookup"><span data-stu-id="d841b-127">Requirements</span></span>  

 <span data-ttu-id="d841b-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d841b-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d841b-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="d841b-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d841b-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d841b-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d841b-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d841b-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d841b-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="d841b-132">See also</span></span>

- [<span data-ttu-id="d841b-133">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="d841b-133">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="d841b-134">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="d841b-134">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="d841b-135">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="d841b-135">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="d841b-136">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="d841b-136">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
