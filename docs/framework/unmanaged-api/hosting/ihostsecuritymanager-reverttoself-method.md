---
description: 了解详细信息： IHostSecurityManager：： RevertToSelf 方法
title: IHostSecurityManager::RevertToSelf 方法
ms.date: 03/30/2017
api_name:
- IHostSecurityManager.RevertToSelf
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager::RevertToSelf
helpviewer_keywords:
- RevertToSelf method [.NET Framework hosting]
- IHostSecurityManager::RevertToSelf method [.NET Framework hosting]
ms.assetid: 189f28f8-f9a1-4192-aedc-91084e4f8b99
topic_type:
- apiref
ms.openlocfilehash: f3488653bcb498c7521de0e368b33bc444967f21
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671498"
---
# <a name="ihostsecuritymanagerreverttoself-method"></a><span data-ttu-id="6e25b-103">IHostSecurityManager::RevertToSelf 方法</span><span class="sxs-lookup"><span data-stu-id="6e25b-103">IHostSecurityManager::RevertToSelf Method</span></span>

<span data-ttu-id="6e25b-104">终止当前用户标识的模拟并返回原始线程标记。</span><span class="sxs-lookup"><span data-stu-id="6e25b-104">Terminates impersonation of the current user identity and returns the original thread token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e25b-105">语法</span><span class="sxs-lookup"><span data-stu-id="6e25b-105">Syntax</span></span>  
  
```cpp  
HRESULT RevertToSelf ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="6e25b-106">返回值</span><span class="sxs-lookup"><span data-stu-id="6e25b-106">Return Value</span></span>  
  
|<span data-ttu-id="6e25b-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6e25b-107">HRESULT</span></span>|<span data-ttu-id="6e25b-108">说明</span><span class="sxs-lookup"><span data-stu-id="6e25b-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6e25b-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e25b-109">S_OK</span></span>|<span data-ttu-id="6e25b-110">`RevertToSelf` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="6e25b-110">`RevertToSelf` returned successfully.</span></span>|  
|<span data-ttu-id="6e25b-111">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="6e25b-111">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="6e25b-112"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="6e25b-112">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="6e25b-113">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6e25b-113">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="6e25b-114">调用超时。</span><span class="sxs-lookup"><span data-stu-id="6e25b-114">The call timed out.</span></span>|  
|<span data-ttu-id="6e25b-115">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="6e25b-115">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="6e25b-116">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="6e25b-116">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="6e25b-117">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="6e25b-117">HOST_E_ABANDONED</span></span>|<span data-ttu-id="6e25b-118">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="6e25b-118">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="6e25b-119">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="6e25b-119">E_FAIL</span></span>|<span data-ttu-id="6e25b-120">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="6e25b-120">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="6e25b-121">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="6e25b-121">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="6e25b-122">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="6e25b-122">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6e25b-123">备注</span><span class="sxs-lookup"><span data-stu-id="6e25b-123">Remarks</span></span>  

 <span data-ttu-id="6e25b-124">`RevertToSelf` 调用 [ImpersonateLoggedOnUser](ihostsecuritymanager-impersonateloggedonuser-method.md) 方法后，将调用以返回到原始线程标记。</span><span class="sxs-lookup"><span data-stu-id="6e25b-124">`RevertToSelf` is called to return to the original thread token, after an earlier call to the [ImpersonateLoggedOnUser](ihostsecuritymanager-impersonateloggedonuser-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6e25b-125">要求</span><span class="sxs-lookup"><span data-stu-id="6e25b-125">Requirements</span></span>  

 <span data-ttu-id="6e25b-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6e25b-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6e25b-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6e25b-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6e25b-128">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6e25b-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6e25b-129">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6e25b-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e25b-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="6e25b-130">See also</span></span>

- [<span data-ttu-id="6e25b-131">IHostSecurityContext 接口</span><span class="sxs-lookup"><span data-stu-id="6e25b-131">IHostSecurityContext Interface</span></span>](ihostsecuritycontext-interface.md)
- [<span data-ttu-id="6e25b-132">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="6e25b-132">IHostSecurityManager Interface</span></span>](ihostsecuritymanager-interface.md)
- [<span data-ttu-id="6e25b-133">ImpersonateLoggedOnUser 方法</span><span class="sxs-lookup"><span data-stu-id="6e25b-133">ImpersonateLoggedOnUser Method</span></span>](ihostsecuritymanager-impersonateloggedonuser-method.md)
