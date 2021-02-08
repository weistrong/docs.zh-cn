---
description: 了解详细信息： ICLRHostBindingPolicyManager：： EvaluatePolicy 方法
title: ICLRHostBindingPolicyManager::EvaluatePolicy 方法
ms.date: 03/30/2017
api_name:
- ICLRHostBindingPolicyManager.EvaluatePolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostBindingPolicyManager::EvaluatePolicy
helpviewer_keywords:
- ICLRHostBindingPolicyManager::EvaluatePolicy method [.NET Framework hosting]
- EvaluatePolicy method [.NET Framework hosting]
ms.assetid: 3a3a9446-7a4e-4836-9b27-5c536c15993d
topic_type:
- apiref
ms.openlocfilehash: e92126a8c12d03ee21e4867754b1a418ef11d463
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789965"
---
# <a name="iclrhostbindingpolicymanagerevaluatepolicy-method"></a><span data-ttu-id="515cd-103">ICLRHostBindingPolicyManager::EvaluatePolicy 方法</span><span class="sxs-lookup"><span data-stu-id="515cd-103">ICLRHostBindingPolicyManager::EvaluatePolicy Method</span></span>

<span data-ttu-id="515cd-104">代表主机计算绑定策略。</span><span class="sxs-lookup"><span data-stu-id="515cd-104">Evaluates binding policy on behalf of the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="515cd-105">语法</span><span class="sxs-lookup"><span data-stu-id="515cd-105">Syntax</span></span>  
  
```cpp  
HRESULT EvaluatePolicy (  
    [in] LPCWSTR     pwzReferenceIdentity,  
    [in] BYTE       *pbApplicationPolicy,  
    [in] DWORD       cbAppPolicySize,  
    [out, size_is(*pcchPostPolicyReferenceIdentity)] LPWSTR pwzPostPolicyReferenceIdentity,  
    [in, out] DWORD *pcchPostPolicyReferenceIdentity,  
    [out] DWORD     *pdwPoliciesApplied  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="515cd-106">参数</span><span class="sxs-lookup"><span data-stu-id="515cd-106">Parameters</span></span>  

 `pwzReferenceIdentity`  
 <span data-ttu-id="515cd-107">中在策略计算之前对程序集的引用。</span><span class="sxs-lookup"><span data-stu-id="515cd-107">[in] A reference to the assembly before the policy evaluation.</span></span>  
  
 `pbApplicationPolicy`  
 <span data-ttu-id="515cd-108">中指向包含策略数据的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="515cd-108">[in] A pointer to a buffer that contains the policy data.</span></span>  
  
 `cbAppPolicySize`  
 <span data-ttu-id="515cd-109">中缓冲区的大小 `pbApplicationPolicy` 。</span><span class="sxs-lookup"><span data-stu-id="515cd-109">[in] The size of the `pbApplicationPolicy` buffer.</span></span>  
  
 `pwzPostPolicyReferenceIdentity`  
 <span data-ttu-id="515cd-110">弄对新策略数据进行计算后对程序集的引用。</span><span class="sxs-lookup"><span data-stu-id="515cd-110">[out] A reference to the assembly after the evaluation of the new policy data.</span></span>  
  
 `pcchPostPolicyReferenceIdentity`  
 <span data-ttu-id="515cd-111">[in，out]一个指针，指向对新策略数据进行计算后的程序集标识引用缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="515cd-111">[in, out] A pointer to the size of the assembly identity reference buffer after the evaluation of the new policy data.</span></span>  
  
 `pdwPoliciesApplied`  
 <span data-ttu-id="515cd-112">弄指向 [EBindPolicyLevels](ebindpolicylevels-enumeration.md) 值的逻辑或组合的指针，指示已应用的策略。</span><span class="sxs-lookup"><span data-stu-id="515cd-112">[out] A pointer to a logical OR combination of [EBindPolicyLevels](ebindpolicylevels-enumeration.md) values, indicating which policies have been applied.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="515cd-113">返回值</span><span class="sxs-lookup"><span data-stu-id="515cd-113">Return Value</span></span>  
  
|<span data-ttu-id="515cd-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="515cd-114">HRESULT</span></span>|<span data-ttu-id="515cd-115">说明</span><span class="sxs-lookup"><span data-stu-id="515cd-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="515cd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="515cd-116">S_OK</span></span>|<span data-ttu-id="515cd-117">评估已成功完成。</span><span class="sxs-lookup"><span data-stu-id="515cd-117">The evaluation completed successfully.</span></span>|  
|<span data-ttu-id="515cd-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="515cd-118">E_INVALIDARG</span></span>|<span data-ttu-id="515cd-119">`pwzReferenceIdentity`或 `pbApplicationPolicy` 为空引用。</span><span class="sxs-lookup"><span data-stu-id="515cd-119">Either `pwzReferenceIdentity` or `pbApplicationPolicy` is a null reference.</span></span>|  
|<span data-ttu-id="515cd-120">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="515cd-120">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="515cd-121">`cbAppPolicySize` 太小。</span><span class="sxs-lookup"><span data-stu-id="515cd-121">`cbAppPolicySize` is too small.</span></span>|  
|<span data-ttu-id="515cd-122">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="515cd-122">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="515cd-123"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="515cd-123">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="515cd-124">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="515cd-124">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="515cd-125">调用超时。</span><span class="sxs-lookup"><span data-stu-id="515cd-125">The call timed out.</span></span>|  
|<span data-ttu-id="515cd-126">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="515cd-126">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="515cd-127">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="515cd-127">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="515cd-128">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="515cd-128">HOST_E_ABANDONED</span></span>|<span data-ttu-id="515cd-129">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="515cd-129">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="515cd-130">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="515cd-130">E_FAIL</span></span>|<span data-ttu-id="515cd-131">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="515cd-131">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="515cd-132">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="515cd-132">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="515cd-133">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="515cd-133">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="515cd-134">备注</span><span class="sxs-lookup"><span data-stu-id="515cd-134">Remarks</span></span>  

 <span data-ttu-id="515cd-135">此 `EvaluatePolicy` 方法允许主机影响绑定策略，以维护特定于主机的程序集版本要求。</span><span class="sxs-lookup"><span data-stu-id="515cd-135">The `EvaluatePolicy` method allows the host to influence binding policy to maintain host-specific assembly versioning requirements.</span></span> <span data-ttu-id="515cd-136">策略引擎本身仍保留在 CLR 内。</span><span class="sxs-lookup"><span data-stu-id="515cd-136">The policy engine itself remains inside the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="515cd-137">要求</span><span class="sxs-lookup"><span data-stu-id="515cd-137">Requirements</span></span>  

 <span data-ttu-id="515cd-138">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="515cd-138">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="515cd-139">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="515cd-139">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="515cd-140">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="515cd-140">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="515cd-141">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="515cd-141">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="515cd-142">请参阅</span><span class="sxs-lookup"><span data-stu-id="515cd-142">See also</span></span>

- [<span data-ttu-id="515cd-143">ICLRHostBindingPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="515cd-143">ICLRHostBindingPolicyManager Interface</span></span>](iclrhostbindingpolicymanager-interface.md)
