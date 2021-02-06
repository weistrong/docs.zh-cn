---
description: 了解详细信息： ICLRPolicyManager：： SetDefaultAction 方法
title: ICLRPolicyManager::SetDefaultAction 方法
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager.SetDefaultAction
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager::SetDefaultAction
helpviewer_keywords:
- SetDefaultAction method [.NET Framework hosting]
- ICLRPolicyManager::SetDefaultAction method [.NET Framework hosting]
ms.assetid: f9411e7a-27df-451f-9f6c-d643d6a7a7ce
topic_type:
- apiref
ms.openlocfilehash: cedf29f6217660493b151e06220158e931385d79
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637360"
---
# <a name="iclrpolicymanagersetdefaultaction-method"></a><span data-ttu-id="ea23c-103">ICLRPolicyManager::SetDefaultAction 方法</span><span class="sxs-lookup"><span data-stu-id="ea23c-103">ICLRPolicyManager::SetDefaultAction Method</span></span>

<span data-ttu-id="ea23c-104">指定发生指定操作时公共语言运行时 (CLR) 应执行的策略操作。</span><span class="sxs-lookup"><span data-stu-id="ea23c-104">Specifies the policy action the common language runtime (CLR) should take when the specified operation occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea23c-105">语法</span><span class="sxs-lookup"><span data-stu-id="ea23c-105">Syntax</span></span>  
  
```cpp  
HRESULT SetDefaultAction (  
    [in] EClrOperation operation,  
    [in] EPolicyAction action  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ea23c-106">参数</span><span class="sxs-lookup"><span data-stu-id="ea23c-106">Parameters</span></span>  

 `operation`  
 <span data-ttu-id="ea23c-107">中 [EClrOperation](eclroperation-enumeration.md) 值之一，指示应为其自定义 CLR 行为的操作。</span><span class="sxs-lookup"><span data-stu-id="ea23c-107">[in] One of the [EClrOperation](eclroperation-enumeration.md) values, indicating the action for which CLR behavior should be customized.</span></span>  
  
 `action`  
 <span data-ttu-id="ea23c-108">中 [EPolicyAction](epolicyaction-enumeration.md) 值之一，指示 CLR 在发生时应执行的策略操作 `operation` 。</span><span class="sxs-lookup"><span data-stu-id="ea23c-108">[in] One of the [EPolicyAction](epolicyaction-enumeration.md) values, indicating the policy action the CLR should take when `operation` occurs.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ea23c-109">返回值</span><span class="sxs-lookup"><span data-stu-id="ea23c-109">Return Value</span></span>  
  
|<span data-ttu-id="ea23c-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ea23c-110">HRESULT</span></span>|<span data-ttu-id="ea23c-111">说明</span><span class="sxs-lookup"><span data-stu-id="ea23c-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ea23c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea23c-112">S_OK</span></span>|<span data-ttu-id="ea23c-113">`SetDefaultAction` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ea23c-113">`SetDefaultAction` returned successfully.</span></span>|  
|<span data-ttu-id="ea23c-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ea23c-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ea23c-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ea23c-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ea23c-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ea23c-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ea23c-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ea23c-117">The call timed out.</span></span>|  
|<span data-ttu-id="ea23c-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ea23c-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ea23c-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ea23c-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ea23c-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ea23c-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ea23c-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ea23c-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ea23c-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ea23c-122">E_FAIL</span></span>|<span data-ttu-id="ea23c-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ea23c-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ea23c-124">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ea23c-124">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ea23c-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ea23c-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="ea23c-126">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ea23c-126">E_INVALIDARG</span></span>|<span data-ttu-id="ea23c-127">为指定了无效的 `action` `operation` ，或者为提供的值无效 `operation` 。</span><span class="sxs-lookup"><span data-stu-id="ea23c-127">An invalid `action` was specified for the `operation`, or an invalid value was supplied for `operation`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ea23c-128">备注</span><span class="sxs-lookup"><span data-stu-id="ea23c-128">Remarks</span></span>  

 <span data-ttu-id="ea23c-129">并非所有策略操作值都可以指定为 CLR 操作的默认行为。</span><span class="sxs-lookup"><span data-stu-id="ea23c-129">Not all policy action values can be specified as the default behavior for CLR operations.</span></span> <span data-ttu-id="ea23c-130">`SetDefaultAction` 通常只能用于升级行为。</span><span class="sxs-lookup"><span data-stu-id="ea23c-130">`SetDefaultAction` can typically be used only to escalate behavior.</span></span> <span data-ttu-id="ea23c-131">例如，主机可以指定线程中止进入强制线程中止，但不能指定相反的。</span><span class="sxs-lookup"><span data-stu-id="ea23c-131">For example, a host can specify that thread aborts be turned into rude thread aborts, but cannot specify the opposite.</span></span> <span data-ttu-id="ea23c-132">下表描述了 `action` 每个可能值的有效值 `operation` 。</span><span class="sxs-lookup"><span data-stu-id="ea23c-132">The table below describes the valid `action` values for each possible `operation` value.</span></span>  
  
|<span data-ttu-id="ea23c-133">值 `operation`</span><span class="sxs-lookup"><span data-stu-id="ea23c-133">Value for `operation`</span></span>|<span data-ttu-id="ea23c-134">`action` 的有效值</span><span class="sxs-lookup"><span data-stu-id="ea23c-134">Valid values for `action`</span></span>|  
|---------------------------|-------------------------------|  
|<span data-ttu-id="ea23c-135">OPR_ThreadAbort</span><span class="sxs-lookup"><span data-stu-id="ea23c-135">OPR_ThreadAbort</span></span>|<span data-ttu-id="ea23c-136">- eAbortThread</span><span class="sxs-lookup"><span data-stu-id="ea23c-136">-   eAbortThread</span></span><br /><span data-ttu-id="ea23c-137">- eRudeAbortThread</span><span class="sxs-lookup"><span data-stu-id="ea23c-137">-   eRudeAbortThread</span></span><br /><span data-ttu-id="ea23c-138">- eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="ea23c-138">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="ea23c-139">- eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="ea23c-139">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="ea23c-140">- eExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-140">-   eExitProcess</span></span><br /><span data-ttu-id="ea23c-141">- eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-141">-   eFastExitProcess</span></span><br /><span data-ttu-id="ea23c-142">- eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-142">-   eRudeExitProcess</span></span><br /><span data-ttu-id="ea23c-143">- eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="ea23c-143">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="ea23c-144">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="ea23c-144">OPR_ThreadRudeAbortInNonCriticalRegion</span></span><br /><br /> <span data-ttu-id="ea23c-145">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="ea23c-145">OPR_ThreadRudeAbortInCriticalRegion</span></span>|<span data-ttu-id="ea23c-146">- eRudeAbortThread</span><span class="sxs-lookup"><span data-stu-id="ea23c-146">-   eRudeAbortThread</span></span><br /><span data-ttu-id="ea23c-147">- eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="ea23c-147">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="ea23c-148">- eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="ea23c-148">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="ea23c-149">- eExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-149">-   eExitProcess</span></span><br /><span data-ttu-id="ea23c-150">- eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-150">-   eFastExitProcess</span></span><br /><span data-ttu-id="ea23c-151">- eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-151">-   eRudeExitProcess</span></span><br /><span data-ttu-id="ea23c-152">- eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="ea23c-152">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="ea23c-153">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="ea23c-153">OPR_AppDomainUnload</span></span>|<span data-ttu-id="ea23c-154">- eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="ea23c-154">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="ea23c-155">- eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="ea23c-155">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="ea23c-156">- eExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-156">-   eExitProcess</span></span><br /><span data-ttu-id="ea23c-157">- eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-157">-   eFastExitProcess</span></span><br /><span data-ttu-id="ea23c-158">- eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-158">-   eRudeExitProcess</span></span><br /><span data-ttu-id="ea23c-159">- eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="ea23c-159">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="ea23c-160">OPR_AppDomainRudeUnload</span><span class="sxs-lookup"><span data-stu-id="ea23c-160">OPR_AppDomainRudeUnload</span></span>|<span data-ttu-id="ea23c-161">- eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="ea23c-161">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="ea23c-162">- eExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-162">-   eExitProcess</span></span><br /><span data-ttu-id="ea23c-163">- eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-163">-   eFastExitProcess</span></span><br /><span data-ttu-id="ea23c-164">- eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-164">-   eRudeExitProcess</span></span><br /><span data-ttu-id="ea23c-165">- eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="ea23c-165">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="ea23c-166">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="ea23c-166">OPR_ProcessExit</span></span>|<span data-ttu-id="ea23c-167">- eExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-167">-   eExitProcess</span></span><br /><span data-ttu-id="ea23c-168">- eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-168">-   eFastExitProcess</span></span><br /><span data-ttu-id="ea23c-169">- eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-169">-   eRudeExitProcess</span></span><br /><span data-ttu-id="ea23c-170">- eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="ea23c-170">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="ea23c-171">OPR_FinalizerRun</span><span class="sxs-lookup"><span data-stu-id="ea23c-171">OPR_FinalizerRun</span></span>|<span data-ttu-id="ea23c-172">- eNoAction</span><span class="sxs-lookup"><span data-stu-id="ea23c-172">-   eNoAction</span></span><br /><span data-ttu-id="ea23c-173">- eAbortThread</span><span class="sxs-lookup"><span data-stu-id="ea23c-173">-   eAbortThread</span></span><br /><span data-ttu-id="ea23c-174">- eRudeAbortThread</span><span class="sxs-lookup"><span data-stu-id="ea23c-174">-   eRudeAbortThread</span></span><br /><span data-ttu-id="ea23c-175">- eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="ea23c-175">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="ea23c-176">- eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="ea23c-176">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="ea23c-177">- eExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-177">-   eExitProcess</span></span><br /><span data-ttu-id="ea23c-178">- eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-178">-   eFastExitProcess</span></span><br /><span data-ttu-id="ea23c-179">- eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="ea23c-179">-   eRudeExitProcess</span></span><br /><span data-ttu-id="ea23c-180">- eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="ea23c-180">-   eDisableRuntime</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ea23c-181">要求</span><span class="sxs-lookup"><span data-stu-id="ea23c-181">Requirements</span></span>  

 <span data-ttu-id="ea23c-182">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ea23c-182">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ea23c-183">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ea23c-183">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ea23c-184">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ea23c-184">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ea23c-185">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ea23c-185">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea23c-186">请参阅</span><span class="sxs-lookup"><span data-stu-id="ea23c-186">See also</span></span>

- [<span data-ttu-id="ea23c-187">EClrOperation 枚举</span><span class="sxs-lookup"><span data-stu-id="ea23c-187">EClrOperation Enumeration</span></span>](eclroperation-enumeration.md)
- [<span data-ttu-id="ea23c-188">EPolicyAction 枚举</span><span class="sxs-lookup"><span data-stu-id="ea23c-188">EPolicyAction Enumeration</span></span>](epolicyaction-enumeration.md)
- [<span data-ttu-id="ea23c-189">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="ea23c-189">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
