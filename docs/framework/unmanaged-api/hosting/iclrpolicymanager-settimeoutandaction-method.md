---
description: 了解详细信息： ICLRPolicyManager：： SetTimeoutAndAction 方法
title: ICLRPolicyManager::SetTimeoutAndAction 方法
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager.SetTimeoutAndAction
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager::SetTimeoutAndAction
helpviewer_keywords:
- ICLRPolicyManager::SetTimeoutAndAction method [.NET Framework hosting]
- SetTimeoutAndAction method [.NET Framework hosting]
ms.assetid: 60454f91-d855-4ddf-bb6d-60a02f5eabab
topic_type:
- apiref
ms.openlocfilehash: c91d43cce381bef804b30e9e1dcb50574ddcd1b4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716557"
---
# <a name="iclrpolicymanagersettimeoutandaction-method"></a><span data-ttu-id="ba1c1-103">ICLRPolicyManager::SetTimeoutAndAction 方法</span><span class="sxs-lookup"><span data-stu-id="ba1c1-103">ICLRPolicyManager::SetTimeoutAndAction Method</span></span>

<span data-ttu-id="ba1c1-104">设置指定操作的超时值，并指定操作发生时公共语言运行时 (CLR) 应执行的策略操作。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-104">Sets a timeout value for the specified operation, and specifies the policy action the common language runtime (CLR) should take when the operation occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ba1c1-105">语法</span><span class="sxs-lookup"><span data-stu-id="ba1c1-105">Syntax</span></span>  
  
```cpp  
HRESULT SetTimeoutAndAction (  
    [in] EClrOperation operation,  
    [in] DWORD dwMilliseconds,  
    [in] EPolicyAction action  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ba1c1-106">参数</span><span class="sxs-lookup"><span data-stu-id="ba1c1-106">Parameters</span></span>  

 `operation`  
 <span data-ttu-id="ba1c1-107">中 [EClrOperation](eclroperation-enumeration.md) 值之一，指示要设置超时和策略的操作 `action` 。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-107">[in] One of the [EClrOperation](eclroperation-enumeration.md) values, indicating the operation for which to set the timeout and policy `action`.</span></span> <span data-ttu-id="ba1c1-108">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="ba1c1-108">The following values are supported:</span></span>  
  
- <span data-ttu-id="ba1c1-109">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="ba1c1-109">OPR_AppDomainUnload</span></span>  
  
- <span data-ttu-id="ba1c1-110">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="ba1c1-110">OPR_ProcessExit</span></span>  
  
- <span data-ttu-id="ba1c1-111">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="ba1c1-111">OPR_ThreadRudeAbortInCriticalRegion</span></span>  
  
- <span data-ttu-id="ba1c1-112">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="ba1c1-112">OPR_ThreadRudeAbortInNonCriticalRegion</span></span>  
  
 `dwMilliseconds`  
 <span data-ttu-id="ba1c1-113">中新的超时值（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-113">[in] The new timeout value, in milliseconds.</span></span> <span data-ttu-id="ba1c1-114">如果值为 "无限" `operation` ，则永远不会超时。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-114">A value of INFINITE causes `operation` never to time out.</span></span>  
  
 `action`  
 <span data-ttu-id="ba1c1-115">中 [EPolicyAction](epolicyaction-enumeration.md) 值之一，指示发生时 CLR 应执行的策略操作 `operation` 。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-115">[in] One of the [EPolicyAction](epolicyaction-enumeration.md) values, indicating the policy action that the CLR should take when `operation` occurs.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ba1c1-116">返回值</span><span class="sxs-lookup"><span data-stu-id="ba1c1-116">Return Value</span></span>  
  
|<span data-ttu-id="ba1c1-117">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ba1c1-117">HRESULT</span></span>|<span data-ttu-id="ba1c1-118">说明</span><span class="sxs-lookup"><span data-stu-id="ba1c1-118">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ba1c1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba1c1-119">S_OK</span></span>|<span data-ttu-id="ba1c1-120">`SetTimeoutAndAction` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-120">`SetTimeoutAndAction` returned successfully.</span></span>|  
|<span data-ttu-id="ba1c1-121">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ba1c1-121">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ba1c1-122">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-122">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ba1c1-123">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ba1c1-123">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ba1c1-124">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-124">The call timed out.</span></span>|  
|<span data-ttu-id="ba1c1-125">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ba1c1-125">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ba1c1-126">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-126">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ba1c1-127">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ba1c1-127">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ba1c1-128">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-128">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ba1c1-129">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ba1c1-129">E_FAIL</span></span>|<span data-ttu-id="ba1c1-130">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-130">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ba1c1-131">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-131">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ba1c1-132">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-132">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="ba1c1-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ba1c1-133">E_INVALIDARG</span></span>|<span data-ttu-id="ba1c1-134">无法为指定的设置超时 `operation` ，或者为提供的值无效 `action` 。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-134">A timeout cannot be set for the specified `operation`, or an invalid value was supplied for `action`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ba1c1-135">备注</span><span class="sxs-lookup"><span data-stu-id="ba1c1-135">Remarks</span></span>  

 <span data-ttu-id="ba1c1-136">`SetTimeoutAndAction` 封装了 [ICLRPolicyManager：： SetTimeout](iclrpolicymanager-settimeout-method.md) 和 [ICLRPolicyManager：： SetActionOnTimeout](iclrpolicymanager-setactionontimeout-method.md) 方法的功能，可调用这些方法来代替对这两个方法的顺序调用。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-136">`SetTimeoutAndAction` encapsulates the capabilities of the [ICLRPolicyManager::SetTimeout](iclrpolicymanager-settimeout-method.md) and [ICLRPolicyManager::SetActionOnTimeout](iclrpolicymanager-setactionontimeout-method.md) methods, and can be called in place of sequential calls to these two methods.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="ba1c1-137">并非所有策略操作值都可以指定为 CLR 操作的超时行为。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-137">Not all policy action values can be specified as the timeout behavior for CLR operations.</span></span> <span data-ttu-id="ba1c1-138">有关有效值，请参阅主题的 "备注" 部分。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-138">See the Remarks sections of the topics for these two methods for valid values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ba1c1-139">要求</span><span class="sxs-lookup"><span data-stu-id="ba1c1-139">Requirements</span></span>  

 <span data-ttu-id="ba1c1-140">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ba1c1-140">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ba1c1-141">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ba1c1-141">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ba1c1-142">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ba1c1-142">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ba1c1-143">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ba1c1-143">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ba1c1-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="ba1c1-144">See also</span></span>

- [<span data-ttu-id="ba1c1-145">EClrOperation 枚举</span><span class="sxs-lookup"><span data-stu-id="ba1c1-145">EClrOperation Enumeration</span></span>](eclroperation-enumeration.md)
- [<span data-ttu-id="ba1c1-146">EPolicyAction 枚举</span><span class="sxs-lookup"><span data-stu-id="ba1c1-146">EPolicyAction Enumeration</span></span>](epolicyaction-enumeration.md)
- [<span data-ttu-id="ba1c1-147">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="ba1c1-147">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
- [<span data-ttu-id="ba1c1-148">SetActionOnTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="ba1c1-148">SetActionOnTimeout Method</span></span>](iclrpolicymanager-setactionontimeout-method.md)
- [<span data-ttu-id="ba1c1-149">ICLRPolicyManager：： SetTimeoutAndAction</span><span class="sxs-lookup"><span data-stu-id="ba1c1-149">ICLRPolicyManager::SetTimeoutAndAction</span></span>](iclrpolicymanager-settimeoutandaction-method.md)
