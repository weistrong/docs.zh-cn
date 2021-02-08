---
description: 了解详细信息： ICLRTask：： LocksHeld 方法
title: ICLRTask::LocksHeld 方法
ms.date: 03/30/2017
api_name:
- ICLRTask.LocksHeld
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::LocksHeld
helpviewer_keywords:
- LocksHeld method [.NET Framework hosting]
- ICLRTask::LocksHeld method [.NET Framework hosting]
ms.assetid: e88a4dc3-02cc-4703-a474-292b71c40657
topic_type:
- apiref
ms.openlocfilehash: 5dff0b2a80594e03d61d50c6d9fa52bb12bb42f2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799521"
---
# <a name="iclrtasklocksheld-method"></a><span data-ttu-id="44445-103">ICLRTask::LocksHeld 方法</span><span class="sxs-lookup"><span data-stu-id="44445-103">ICLRTask::LocksHeld Method</span></span>

<span data-ttu-id="44445-104">获取任务当前持有的锁的数目。</span><span class="sxs-lookup"><span data-stu-id="44445-104">Gets the number of locks currently held on the task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44445-105">语法</span><span class="sxs-lookup"><span data-stu-id="44445-105">Syntax</span></span>  
  
```cpp  
HRESULT LocksHeld (  
    [out] SIZE_T *pLockCount  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="44445-106">参数</span><span class="sxs-lookup"><span data-stu-id="44445-106">Parameters</span></span>  

 `pLockCount`  
 <span data-ttu-id="44445-107">弄在调用方法时任务中持有的锁的数目。</span><span class="sxs-lookup"><span data-stu-id="44445-107">[out] The number of locks held on the task at the time of the method call.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="44445-108">返回值</span><span class="sxs-lookup"><span data-stu-id="44445-108">Return Value</span></span>  
  
|<span data-ttu-id="44445-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="44445-109">HRESULT</span></span>|<span data-ttu-id="44445-110">说明</span><span class="sxs-lookup"><span data-stu-id="44445-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="44445-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="44445-111">S_OK</span></span>|<span data-ttu-id="44445-112">`LocksHeld` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="44445-112">`LocksHeld` returned successfully.</span></span>|  
|<span data-ttu-id="44445-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="44445-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="44445-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="44445-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="44445-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="44445-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="44445-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="44445-116">The call timed out.</span></span>|  
|<span data-ttu-id="44445-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="44445-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="44445-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="44445-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="44445-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="44445-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="44445-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="44445-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="44445-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="44445-121">E_FAIL</span></span>|<span data-ttu-id="44445-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="44445-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="44445-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="44445-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="44445-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="44445-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="44445-125">要求</span><span class="sxs-lookup"><span data-stu-id="44445-125">Requirements</span></span>  

 <span data-ttu-id="44445-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="44445-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="44445-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="44445-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="44445-128">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="44445-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="44445-129">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="44445-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44445-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="44445-130">See also</span></span>

- [<span data-ttu-id="44445-131">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="44445-131">ICLRTask Interface</span></span>](iclrtask-interface.md)
- [<span data-ttu-id="44445-132">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="44445-132">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)
- [<span data-ttu-id="44445-133">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="44445-133">IHostTask Interface</span></span>](ihosttask-interface.md)
- [<span data-ttu-id="44445-134">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="44445-134">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)
