---
description: 了解详细信息： IHostPolicyManager：： OnTimeout 方法
title: IHostPolicyManager::OnTimeout 方法
ms.date: 03/30/2017
api_name:
- IHostPolicyManager.OnTimeout
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostPolicyManager::OnTimeout
helpviewer_keywords:
- IHostPolicyManager::OnTimeout method [.NET Framework hosting]
- OnTimeout method [.NET Framework hosting]
ms.assetid: 0a313b51-5e4d-4714-a86b-af75cf3902e6
topic_type:
- apiref
ms.openlocfilehash: 3a4b1dcf632a0a67c541cacf7c872b3f994e8a07
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671810"
---
# <a name="ihostpolicymanagerontimeout-method"></a><span data-ttu-id="0c0d0-103">IHostPolicyManager::OnTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="0c0d0-103">IHostPolicyManager::OnTimeout Method</span></span>

<span data-ttu-id="0c0d0-104">向宿主通知公共语言运行时 (CLR) 将要使用 [ICLRPolicyManager：： SetActionOnTimeout](iclrpolicymanager-setactionontimeout-method.md) 方法调用指定的操作，以响应超时。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-104">Notifies the host that the common language runtime (CLR) is about to take the action specified by a call to the [ICLRPolicyManager::SetActionOnTimeout](iclrpolicymanager-setactionontimeout-method.md) method in response to a timeout.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c0d0-105">语法</span><span class="sxs-lookup"><span data-stu-id="0c0d0-105">Syntax</span></span>  
  
```cpp  
HRESULT OnTimeout (  
    [in] EClrOperation  operation,
    [in] EPolicyAction  action  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0c0d0-106">参数</span><span class="sxs-lookup"><span data-stu-id="0c0d0-106">Parameters</span></span>  

 `operation`  
 <span data-ttu-id="0c0d0-107">中 [EClrOperation](eclroperation-enumeration.md) 值之一，指示已超时的操作的类型。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-107">[in] One of the [EClrOperation](eclroperation-enumeration.md) values, indicating the kind of operation that timed out.</span></span>  
  
 `action`  
 <span data-ttu-id="0c0d0-108">中 [EPolicyAction](epolicyaction-enumeration.md) 值之一，指示 CLR 响应超时所采取的操作。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-108">[in] One of the [EPolicyAction](epolicyaction-enumeration.md) values, indicating the action the CLR is taking in response to the timeout.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0c0d0-109">返回值</span><span class="sxs-lookup"><span data-stu-id="0c0d0-109">Return Value</span></span>  
  
|<span data-ttu-id="0c0d0-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0c0d0-110">HRESULT</span></span>|<span data-ttu-id="0c0d0-111">说明</span><span class="sxs-lookup"><span data-stu-id="0c0d0-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0c0d0-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c0d0-112">S_OK</span></span>|<span data-ttu-id="0c0d0-113">`OnTimeout` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-113">`OnTimeout` returned successfully.</span></span>|  
|<span data-ttu-id="0c0d0-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0c0d0-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="0c0d0-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="0c0d0-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0c0d0-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="0c0d0-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-117">The call timed out.</span></span>|  
|<span data-ttu-id="0c0d0-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="0c0d0-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="0c0d0-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="0c0d0-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="0c0d0-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="0c0d0-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="0c0d0-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0c0d0-122">E_FAIL</span></span>|<span data-ttu-id="0c0d0-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="0c0d0-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="0c0d0-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0c0d0-126">要求</span><span class="sxs-lookup"><span data-stu-id="0c0d0-126">Requirements</span></span>  

 <span data-ttu-id="0c0d0-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0c0d0-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c0d0-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="0c0d0-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0c0d0-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0c0d0-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0c0d0-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c0d0-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c0d0-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="0c0d0-131">See also</span></span>

- [<span data-ttu-id="0c0d0-132">EClrOperation 枚举</span><span class="sxs-lookup"><span data-stu-id="0c0d0-132">EClrOperation Enumeration</span></span>](eclroperation-enumeration.md)
- [<span data-ttu-id="0c0d0-133">EPolicyAction 枚举</span><span class="sxs-lookup"><span data-stu-id="0c0d0-133">EPolicyAction Enumeration</span></span>](epolicyaction-enumeration.md)
- [<span data-ttu-id="0c0d0-134">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="0c0d0-134">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
- [<span data-ttu-id="0c0d0-135">IHostPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="0c0d0-135">IHostPolicyManager Interface</span></span>](ihostpolicymanager-interface.md)
