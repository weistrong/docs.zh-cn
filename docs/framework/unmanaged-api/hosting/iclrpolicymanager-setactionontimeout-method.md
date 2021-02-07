---
description: 了解详细信息： ICLRPolicyManager：： SetActionOnTimeout 方法
title: ICLRPolicyManager::SetActionOnTimeout 方法
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager.SetActionOnTimeout
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager::SetActionOnTimeout
helpviewer_keywords:
- SetActionOnTimeout method [.NET Framework hosting]
- ICLRPolicyManager::SetActionOnTimeout method [.NET Framework hosting]
ms.assetid: 38439fa1-2b99-4fa8-a6ec-08afc0f83b9c
topic_type:
- apiref
ms.openlocfilehash: d682acd49bdc4fa0f8c58a1300e2215816fe2718
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689022"
---
# <a name="iclrpolicymanagersetactionontimeout-method"></a><span data-ttu-id="41d1a-103">ICLRPolicyManager::SetActionOnTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="41d1a-103">ICLRPolicyManager::SetActionOnTimeout Method</span></span>

<span data-ttu-id="41d1a-104">指定在指定操作超时时公共语言运行时 (CLR) 应执行的策略操作。</span><span class="sxs-lookup"><span data-stu-id="41d1a-104">Specifies the policy action the common language runtime (CLR) should take when the specified operation times out.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41d1a-105">语法</span><span class="sxs-lookup"><span data-stu-id="41d1a-105">Syntax</span></span>  
  
```cpp  
HRESULT SetActionOnTimeout (  
    [in] EClrOperation operation,  
    [in] EPolicyAction action  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="41d1a-106">参数</span><span class="sxs-lookup"><span data-stu-id="41d1a-106">Parameters</span></span>  

 `operation`  
 <span data-ttu-id="41d1a-107">中 [EClrOperation](eclroperation-enumeration.md) 值之一，指示要为其指定超时操作的操作。</span><span class="sxs-lookup"><span data-stu-id="41d1a-107">[in] One of the [EClrOperation](eclroperation-enumeration.md) values, indicating the operation for which to specify the timeout action.</span></span> <span data-ttu-id="41d1a-108">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="41d1a-108">The following values are supported:</span></span>  
  
- <span data-ttu-id="41d1a-109">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="41d1a-109">OPR_AppDomainUnload</span></span>  
  
- <span data-ttu-id="41d1a-110">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="41d1a-110">OPR_ProcessExit</span></span>  
  
- <span data-ttu-id="41d1a-111">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="41d1a-111">OPR_ThreadRudeAbortInCriticalRegion</span></span>  
  
- <span data-ttu-id="41d1a-112">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="41d1a-112">OPR_ThreadRudeAbortInNonCriticalRegion</span></span>  
  
 `action`  
 <span data-ttu-id="41d1a-113">中 [EPolicyAction](epolicyaction-enumeration.md) 值之一，指示操作超时时要执行的策略操作。</span><span class="sxs-lookup"><span data-stu-id="41d1a-113">[in] One of the [EPolicyAction](epolicyaction-enumeration.md) values, indicating the policy action to be taken when the operation times out.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="41d1a-114">返回值</span><span class="sxs-lookup"><span data-stu-id="41d1a-114">Return Value</span></span>  
  
|<span data-ttu-id="41d1a-115">HRESULT</span><span class="sxs-lookup"><span data-stu-id="41d1a-115">HRESULT</span></span>|<span data-ttu-id="41d1a-116">说明</span><span class="sxs-lookup"><span data-stu-id="41d1a-116">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="41d1a-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="41d1a-117">S_OK</span></span>|<span data-ttu-id="41d1a-118">`SetActionOnTimeout` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="41d1a-118">`SetActionOnTimeout` returned successfully.</span></span>|  
|<span data-ttu-id="41d1a-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="41d1a-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="41d1a-120">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="41d1a-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="41d1a-121">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="41d1a-121">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="41d1a-122">调用超时。</span><span class="sxs-lookup"><span data-stu-id="41d1a-122">The call timed out.</span></span>|  
|<span data-ttu-id="41d1a-123">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="41d1a-123">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="41d1a-124">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="41d1a-124">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="41d1a-125">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="41d1a-125">HOST_E_ABANDONED</span></span>|<span data-ttu-id="41d1a-126">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="41d1a-126">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="41d1a-127">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="41d1a-127">E_FAIL</span></span>|<span data-ttu-id="41d1a-128">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="41d1a-128">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="41d1a-129">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="41d1a-129">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="41d1a-130">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="41d1a-130">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="41d1a-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="41d1a-131">E_INVALIDARG</span></span>|<span data-ttu-id="41d1a-132">无法为指定的设置超时 `operation` ，或者为提供的值无效 `operation` 。</span><span class="sxs-lookup"><span data-stu-id="41d1a-132">A timeout cannot be set for the specified `operation`, or an invalid value was supplied for `operation`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="41d1a-133">备注</span><span class="sxs-lookup"><span data-stu-id="41d1a-133">Remarks</span></span>  

 <span data-ttu-id="41d1a-134">超时值可以是 CLR 设置的默认超时值，也可以是主机在 [ICLRPolicyManager：： SetTimeout](iclrpolicymanager-settimeout-method.md) 方法的调用中指定的值。</span><span class="sxs-lookup"><span data-stu-id="41d1a-134">The timeout value can be either the default timeout set by the CLR, or a value specified by the host in a call to the [ICLRPolicyManager::SetTimeout](iclrpolicymanager-settimeout-method.md) method.</span></span>  
  
 <span data-ttu-id="41d1a-135">并非所有策略操作值都可以指定为 CLR 操作的超时行为。</span><span class="sxs-lookup"><span data-stu-id="41d1a-135">Not all policy action values can be specified as the timeout behavior for CLR operations.</span></span> <span data-ttu-id="41d1a-136">`SetActionOnTimeout` 通常仅用于升级行为。</span><span class="sxs-lookup"><span data-stu-id="41d1a-136">`SetActionOnTimeout` is typically used only to escalate behavior.</span></span> <span data-ttu-id="41d1a-137">例如，主机可以指定线程中止进入强制线程中止，但不能指定相反的。</span><span class="sxs-lookup"><span data-stu-id="41d1a-137">For example, a host can specify that thread aborts be turned into rude thread aborts, but cannot specify the opposite.</span></span> <span data-ttu-id="41d1a-138">下表描述了有效值的有效值 `action` `operation` 。</span><span class="sxs-lookup"><span data-stu-id="41d1a-138">The table below describes the valid `action` values for valid `operation` values.</span></span>  
  
|<span data-ttu-id="41d1a-139">值 `operation`</span><span class="sxs-lookup"><span data-stu-id="41d1a-139">Value for `operation`</span></span>|<span data-ttu-id="41d1a-140">`action` 的有效值</span><span class="sxs-lookup"><span data-stu-id="41d1a-140">Valid values for `action`</span></span>|  
|---------------------------|-------------------------------|  
|<span data-ttu-id="41d1a-141">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="41d1a-141">OPR_ThreadRudeAbortInNonCriticalRegion</span></span><br /><br /> <span data-ttu-id="41d1a-142">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="41d1a-142">OPR_ThreadRudeAbortInCriticalRegion</span></span>|<span data-ttu-id="41d1a-143">- eRudeAbortThread</span><span class="sxs-lookup"><span data-stu-id="41d1a-143">-   eRudeAbortThread</span></span><br /><span data-ttu-id="41d1a-144">- eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="41d1a-144">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="41d1a-145">- eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="41d1a-145">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="41d1a-146">- eExitProcess</span><span class="sxs-lookup"><span data-stu-id="41d1a-146">-   eExitProcess</span></span><br /><span data-ttu-id="41d1a-147">- eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="41d1a-147">-   eFastExitProcess</span></span><br /><span data-ttu-id="41d1a-148">- eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="41d1a-148">-   eRudeExitProcess</span></span><br /><span data-ttu-id="41d1a-149">- eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="41d1a-149">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="41d1a-150">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="41d1a-150">OPR_AppDomainUnload</span></span>|<span data-ttu-id="41d1a-151">- eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="41d1a-151">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="41d1a-152">- eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="41d1a-152">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="41d1a-153">- eExitProcess</span><span class="sxs-lookup"><span data-stu-id="41d1a-153">-   eExitProcess</span></span><br /><span data-ttu-id="41d1a-154">- eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="41d1a-154">-   eFastExitProcess</span></span><br /><span data-ttu-id="41d1a-155">- eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="41d1a-155">-   eRudeExitProcess</span></span><br /><span data-ttu-id="41d1a-156">- eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="41d1a-156">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="41d1a-157">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="41d1a-157">OPR_ProcessExit</span></span>|<span data-ttu-id="41d1a-158">- eExitProcess</span><span class="sxs-lookup"><span data-stu-id="41d1a-158">-   eExitProcess</span></span><br /><span data-ttu-id="41d1a-159">- eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="41d1a-159">-   eFastExitProcess</span></span><br /><span data-ttu-id="41d1a-160">- eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="41d1a-160">-   eRudeExitProcess</span></span><br /><span data-ttu-id="41d1a-161">- eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="41d1a-161">-   eDisableRuntime</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="41d1a-162">要求</span><span class="sxs-lookup"><span data-stu-id="41d1a-162">Requirements</span></span>  

 <span data-ttu-id="41d1a-163">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="41d1a-163">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="41d1a-164">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="41d1a-164">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="41d1a-165">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="41d1a-165">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="41d1a-166">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="41d1a-166">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41d1a-167">请参阅</span><span class="sxs-lookup"><span data-stu-id="41d1a-167">See also</span></span>

- [<span data-ttu-id="41d1a-168">EClrOperation 枚举</span><span class="sxs-lookup"><span data-stu-id="41d1a-168">EClrOperation Enumeration</span></span>](eclroperation-enumeration.md)
- [<span data-ttu-id="41d1a-169">EPolicyAction 枚举</span><span class="sxs-lookup"><span data-stu-id="41d1a-169">EPolicyAction Enumeration</span></span>](epolicyaction-enumeration.md)
- [<span data-ttu-id="41d1a-170">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="41d1a-170">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="41d1a-171">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="41d1a-171">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
