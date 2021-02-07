---
description: 了解详细信息： IHostPolicyManager：： OnFailure 方法
title: IHostPolicyManager::OnFailure 方法
ms.date: 03/30/2017
api_name:
- IHostPolicyManager.OnFailure
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostPolicyManager::OnFailure
helpviewer_keywords:
- OnFailure method [.NET Framework hosting]
- IHostPolicyManager::OnFailure method [.NET Framework hosting]
ms.assetid: 77d3f31e-9a53-4349-9c02-610a71736d42
topic_type:
- apiref
ms.openlocfilehash: 9fb359d4ba1b1b89e029a0772a0f67a49b2b380b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671836"
---
# <a name="ihostpolicymanageronfailure-method"></a><span data-ttu-id="56c22-103">IHostPolicyManager::OnFailure 方法</span><span class="sxs-lookup"><span data-stu-id="56c22-103">IHostPolicyManager::OnFailure Method</span></span>

<span data-ttu-id="56c22-104">向宿主通知公共语言运行时 (CLR) 将要使用 [ICLRPolicyManager：： SetActionOnFailure](iclrpolicymanager-setactiononfailure-method.md) 方法调用指定的操作，以响应资源分配或回收失败。</span><span class="sxs-lookup"><span data-stu-id="56c22-104">Notifies the host that the common language runtime (CLR) is about to take the action specified by a call to the [ICLRPolicyManager::SetActionOnFailure](iclrpolicymanager-setactiononfailure-method.md) method in response to a resource allocation or reclamation failure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="56c22-105">语法</span><span class="sxs-lookup"><span data-stu-id="56c22-105">Syntax</span></span>  
  
```cpp  
HRESULT OnFailure(  
    [in] EClrFailure   failure,  
    [in] EPolicyAction action  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="56c22-106">参数</span><span class="sxs-lookup"><span data-stu-id="56c22-106">Parameters</span></span>  

 `failure`  
 <span data-ttu-id="56c22-107">中 [EClrFailure](eclrfailure-enumeration.md) 值之一，指示 CLR 响应的失败类型。</span><span class="sxs-lookup"><span data-stu-id="56c22-107">[in] One of the [EClrFailure](eclrfailure-enumeration.md) values, indicating the kind of failure to which the CLR is responding.</span></span>  
  
 `action`  
 <span data-ttu-id="56c22-108">中 [EPolicyAction](epolicyaction-enumeration.md) 值之一，指示 CLR 响应的操作 `failure` 。</span><span class="sxs-lookup"><span data-stu-id="56c22-108">[in] One of the [EPolicyAction](epolicyaction-enumeration.md) values, indicating the action the CLR is taking in response to `failure`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="56c22-109">返回值</span><span class="sxs-lookup"><span data-stu-id="56c22-109">Return Value</span></span>  
  
|<span data-ttu-id="56c22-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="56c22-110">HRESULT</span></span>|<span data-ttu-id="56c22-111">说明</span><span class="sxs-lookup"><span data-stu-id="56c22-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="56c22-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="56c22-112">S_OK</span></span>|<span data-ttu-id="56c22-113">`OnFailure` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="56c22-113">`OnFailure` returned successfully.</span></span>|  
|<span data-ttu-id="56c22-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="56c22-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="56c22-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="56c22-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="56c22-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="56c22-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="56c22-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="56c22-117">The call timed out.</span></span>|  
|<span data-ttu-id="56c22-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="56c22-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="56c22-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="56c22-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="56c22-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="56c22-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="56c22-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="56c22-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="56c22-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="56c22-122">E_FAIL</span></span>|<span data-ttu-id="56c22-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="56c22-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="56c22-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="56c22-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="56c22-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="56c22-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="56c22-126">要求</span><span class="sxs-lookup"><span data-stu-id="56c22-126">Requirements</span></span>  

 <span data-ttu-id="56c22-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="56c22-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="56c22-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="56c22-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="56c22-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="56c22-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="56c22-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="56c22-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56c22-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="56c22-131">See also</span></span>

- [<span data-ttu-id="56c22-132">EClrFailure 枚举</span><span class="sxs-lookup"><span data-stu-id="56c22-132">EClrFailure Enumeration</span></span>](eclrfailure-enumeration.md)
- [<span data-ttu-id="56c22-133">EPolicyAction 枚举</span><span class="sxs-lookup"><span data-stu-id="56c22-133">EPolicyAction Enumeration</span></span>](epolicyaction-enumeration.md)
- [<span data-ttu-id="56c22-134">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="56c22-134">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
- [<span data-ttu-id="56c22-135">IHostPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="56c22-135">IHostPolicyManager Interface</span></span>](ihostpolicymanager-interface.md)
