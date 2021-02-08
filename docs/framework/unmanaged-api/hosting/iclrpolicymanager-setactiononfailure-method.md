---
description: 了解详细信息： ICLRPolicyManager：： SetActionOnFailure 方法
title: ICLRPolicyManager::SetActionOnFailure 方法
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager.SetActionOnFailure
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager::SetActionOnFailure
helpviewer_keywords:
- SetActionOnFailure method [.NET Framework hosting]
- ICLRPolicyManager::SetActionOnFailure method [.NET Framework hosting]
ms.assetid: 4664033f-db97-4388-b988-2ec470796e58
topic_type:
- apiref
ms.openlocfilehash: 67d3ca5d7924caf0a768b4de53b4b24f1c72fa27
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789796"
---
# <a name="iclrpolicymanagersetactiononfailure-method"></a><span data-ttu-id="19f6a-103">ICLRPolicyManager::SetActionOnFailure 方法</span><span class="sxs-lookup"><span data-stu-id="19f6a-103">ICLRPolicyManager::SetActionOnFailure Method</span></span>

<span data-ttu-id="19f6a-104">指定发生指定的故障时公共语言运行时 (CLR) 应执行的策略操作。</span><span class="sxs-lookup"><span data-stu-id="19f6a-104">Specifies the policy action the common language runtime (CLR) should take when the specified failure occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19f6a-105">语法</span><span class="sxs-lookup"><span data-stu-id="19f6a-105">Syntax</span></span>  
  
```cpp  
HRESULT SetActionOnFailure (  
    [in] EClrFailure   failure,  
    [in] EPolicyAction action  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="19f6a-106">参数</span><span class="sxs-lookup"><span data-stu-id="19f6a-106">Parameters</span></span>  

 `failure`  
 <span data-ttu-id="19f6a-107">中 [EClrFailure](eclrfailure-enumeration.md) 值之一，指示要采取措施的故障类型。</span><span class="sxs-lookup"><span data-stu-id="19f6a-107">[in] One of the [EClrFailure](eclrfailure-enumeration.md) values, indicating the type of failure for which to take action.</span></span>  
  
 `action`  
 <span data-ttu-id="19f6a-108">中 [EPolicyAction](epolicyaction-enumeration.md) 值之一，指示发生失败时要执行的操作。</span><span class="sxs-lookup"><span data-stu-id="19f6a-108">[in] One of the [EPolicyAction](epolicyaction-enumeration.md) values, indicating the action to be taken when a failure occurs.</span></span> <span data-ttu-id="19f6a-109">有关支持的值的列表，请参阅 "备注" 部分。</span><span class="sxs-lookup"><span data-stu-id="19f6a-109">For a list of supported values, see the Remarks section.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="19f6a-110">返回值</span><span class="sxs-lookup"><span data-stu-id="19f6a-110">Return Value</span></span>  
  
|<span data-ttu-id="19f6a-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="19f6a-111">HRESULT</span></span>|<span data-ttu-id="19f6a-112">说明</span><span class="sxs-lookup"><span data-stu-id="19f6a-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="19f6a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="19f6a-113">S_OK</span></span>|<span data-ttu-id="19f6a-114">`SetActionOnFailure` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="19f6a-114">`SetActionOnFailure` returned successfully.</span></span>|  
|<span data-ttu-id="19f6a-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="19f6a-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="19f6a-116">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="19f6a-116">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="19f6a-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="19f6a-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="19f6a-118">调用超时。</span><span class="sxs-lookup"><span data-stu-id="19f6a-118">The call timed out.</span></span>|  
|<span data-ttu-id="19f6a-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="19f6a-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="19f6a-120">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="19f6a-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="19f6a-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="19f6a-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="19f6a-122">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="19f6a-122">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="19f6a-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="19f6a-123">E_FAIL</span></span>|<span data-ttu-id="19f6a-124">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="19f6a-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="19f6a-125">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="19f6a-125">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="19f6a-126">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="19f6a-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="19f6a-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="19f6a-127">E_INVALIDARG</span></span>|<span data-ttu-id="19f6a-128">无法为指定的操作设置策略操作，或者为该操作指定了无效的策略操作。</span><span class="sxs-lookup"><span data-stu-id="19f6a-128">A policy action cannot be set for the specified operation, or an invalid policy action was specified for the operation.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="19f6a-129">备注</span><span class="sxs-lookup"><span data-stu-id="19f6a-129">Remarks</span></span>  

 <span data-ttu-id="19f6a-130">默认情况下，CLR 在无法分配内存等资源时引发异常。</span><span class="sxs-lookup"><span data-stu-id="19f6a-130">By default, the CLR throws an exception when it fails to allocate a resource such as memory.</span></span> <span data-ttu-id="19f6a-131">`SetActionOnFailure` 允许主机通过指定在失败时要执行的策略操作来重写此行为。</span><span class="sxs-lookup"><span data-stu-id="19f6a-131">`SetActionOnFailure` allows the host to override this behavior by specifying the policy action to take upon failure.</span></span> <span data-ttu-id="19f6a-132">下表显示了支持的 [EClrFailure](eclrfailure-enumeration.md) 和 [EPolicyAction](epolicyaction-enumeration.md) 值的组合。</span><span class="sxs-lookup"><span data-stu-id="19f6a-132">The following table shows the combinations of [EClrFailure](eclrfailure-enumeration.md) and [EPolicyAction](epolicyaction-enumeration.md) values that are supported.</span></span> <span data-ttu-id="19f6a-133"> ([EClrFailure](eclrfailure-enumeration.md) 值中省略 FAIL_ 前缀。 ) </span><span class="sxs-lookup"><span data-stu-id="19f6a-133">(The FAIL_ prefix is omitted from [EClrFailure](eclrfailure-enumeration.md) values.)</span></span>  
  
||<span data-ttu-id="19f6a-134">NonCriticalResource</span><span class="sxs-lookup"><span data-stu-id="19f6a-134">NonCriticalResource</span></span>|<span data-ttu-id="19f6a-135">CriticalResource</span><span class="sxs-lookup"><span data-stu-id="19f6a-135">CriticalResource</span></span>|<span data-ttu-id="19f6a-136">FatalRuntime</span><span class="sxs-lookup"><span data-stu-id="19f6a-136">FatalRuntime</span></span>|<span data-ttu-id="19f6a-137">OrphanedLock</span><span class="sxs-lookup"><span data-stu-id="19f6a-137">OrphanedLock</span></span>|<span data-ttu-id="19f6a-138">StackOverflow</span><span class="sxs-lookup"><span data-stu-id="19f6a-138">StackOverflow</span></span>|<span data-ttu-id="19f6a-139">AccessViolation</span><span class="sxs-lookup"><span data-stu-id="19f6a-139">AccessViolation</span></span>|<span data-ttu-id="19f6a-140">CodeContract</span><span class="sxs-lookup"><span data-stu-id="19f6a-140">CodeContract</span></span>|  
|-|-------------------------|----------------------|------------------|------------------|-------------------|---------------------|------------------|  
|`eNoAction`|<span data-ttu-id="19f6a-141">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-141">X</span></span>|<span data-ttu-id="19f6a-142">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-142">X</span></span>||||<span data-ttu-id="19f6a-143">不适用</span><span class="sxs-lookup"><span data-stu-id="19f6a-143">N/A</span></span>||  
|<span data-ttu-id="19f6a-144">eThrowException</span><span class="sxs-lookup"><span data-stu-id="19f6a-144">eThrowException</span></span>|<span data-ttu-id="19f6a-145">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-145">X</span></span>|<span data-ttu-id="19f6a-146">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-146">X</span></span>||||<span data-ttu-id="19f6a-147">不适用</span><span class="sxs-lookup"><span data-stu-id="19f6a-147">N/A</span></span>||  
|`eAbortThread`|<span data-ttu-id="19f6a-148">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-148">X</span></span>|<span data-ttu-id="19f6a-149">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-149">X</span></span>||||<span data-ttu-id="19f6a-150">不适用</span><span class="sxs-lookup"><span data-stu-id="19f6a-150">N/A</span></span>|<span data-ttu-id="19f6a-151">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-151">X</span></span>|  
|`eRudeAbortThread`|<span data-ttu-id="19f6a-152">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-152">X</span></span>|<span data-ttu-id="19f6a-153">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-153">X</span></span>||||<span data-ttu-id="19f6a-154">不适用</span><span class="sxs-lookup"><span data-stu-id="19f6a-154">N/A</span></span>|<span data-ttu-id="19f6a-155">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-155">X</span></span>|  
|`eUnloadAppDomain`|<span data-ttu-id="19f6a-156">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-156">X</span></span>|<span data-ttu-id="19f6a-157">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-157">X</span></span>||<span data-ttu-id="19f6a-158">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-158">X</span></span>||<span data-ttu-id="19f6a-159">不适用</span><span class="sxs-lookup"><span data-stu-id="19f6a-159">N/A</span></span>|<span data-ttu-id="19f6a-160">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-160">X</span></span>|  
|`eRudeUnloadAppDomain`|<span data-ttu-id="19f6a-161">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-161">X</span></span>|<span data-ttu-id="19f6a-162">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-162">X</span></span>||<span data-ttu-id="19f6a-163">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-163">X</span></span>|<span data-ttu-id="19f6a-164">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-164">X</span></span>|<span data-ttu-id="19f6a-165">不适用</span><span class="sxs-lookup"><span data-stu-id="19f6a-165">N/A</span></span>|<span data-ttu-id="19f6a-166">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-166">X</span></span>|  
|`eExitProcess`|<span data-ttu-id="19f6a-167">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-167">X</span></span>|<span data-ttu-id="19f6a-168">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-168">X</span></span>||<span data-ttu-id="19f6a-169">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-169">X</span></span>|<span data-ttu-id="19f6a-170">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-170">X</span></span>|<span data-ttu-id="19f6a-171">不适用</span><span class="sxs-lookup"><span data-stu-id="19f6a-171">N/A</span></span>|<span data-ttu-id="19f6a-172">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-172">X</span></span>|  
|<span data-ttu-id="19f6a-173">eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="19f6a-173">eFastExitProcess</span></span>|<span data-ttu-id="19f6a-174">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-174">X</span></span>|<span data-ttu-id="19f6a-175">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-175">X</span></span>||<span data-ttu-id="19f6a-176">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-176">X</span></span>|<span data-ttu-id="19f6a-177">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-177">X</span></span>|<span data-ttu-id="19f6a-178">不适用</span><span class="sxs-lookup"><span data-stu-id="19f6a-178">N/A</span></span>||  
|`eRudeExitProcess`|<span data-ttu-id="19f6a-179">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-179">X</span></span>|<span data-ttu-id="19f6a-180">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-180">X</span></span>|<span data-ttu-id="19f6a-181">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-181">X</span></span>|<span data-ttu-id="19f6a-182">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-182">X</span></span>|<span data-ttu-id="19f6a-183">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-183">X</span></span>|<span data-ttu-id="19f6a-184">不适用</span><span class="sxs-lookup"><span data-stu-id="19f6a-184">N/A</span></span>||  
|`eDisableRuntime`|<span data-ttu-id="19f6a-185">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-185">X</span></span>|<span data-ttu-id="19f6a-186">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-186">X</span></span>|<span data-ttu-id="19f6a-187">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-187">X</span></span>|<span data-ttu-id="19f6a-188">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-188">X</span></span>|<span data-ttu-id="19f6a-189">X</span><span class="sxs-lookup"><span data-stu-id="19f6a-189">X</span></span>|<span data-ttu-id="19f6a-190">不适用</span><span class="sxs-lookup"><span data-stu-id="19f6a-190">N/A</span></span>||  
  
## <a name="requirements"></a><span data-ttu-id="19f6a-191">要求</span><span class="sxs-lookup"><span data-stu-id="19f6a-191">Requirements</span></span>  

 <span data-ttu-id="19f6a-192">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="19f6a-192">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="19f6a-193">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="19f6a-193">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="19f6a-194">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="19f6a-194">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="19f6a-195">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="19f6a-195">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19f6a-196">请参阅</span><span class="sxs-lookup"><span data-stu-id="19f6a-196">See also</span></span>

- [<span data-ttu-id="19f6a-197">EClrFailure 枚举</span><span class="sxs-lookup"><span data-stu-id="19f6a-197">EClrFailure Enumeration</span></span>](eclrfailure-enumeration.md)
- [<span data-ttu-id="19f6a-198">EPolicyAction 枚举</span><span class="sxs-lookup"><span data-stu-id="19f6a-198">EPolicyAction Enumeration</span></span>](epolicyaction-enumeration.md)
- [<span data-ttu-id="19f6a-199">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="19f6a-199">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="19f6a-200">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="19f6a-200">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
