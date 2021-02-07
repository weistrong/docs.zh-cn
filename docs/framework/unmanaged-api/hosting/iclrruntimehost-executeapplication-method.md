---
description: 了解详细信息： ICLRRuntimeHost：： ExecuteApplication 方法
title: ICLRRuntimeHost::ExecuteApplication 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.ExecuteApplication
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::ExecuteApplication
helpviewer_keywords:
- ICLRRuntimeHost::ExecuteApplication method [.NET Framework hosting]
- ExecuteApplication method [.NET Framework hosting]
ms.assetid: 5f28cc4e-7176-4e00-aa1f-58ae6ee52fe4
topic_type:
- apiref
ms.openlocfilehash: 1511cc3dcf05c3f2243f4080143789e456c39167
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688970"
---
# <a name="iclrruntimehostexecuteapplication-method"></a><span data-ttu-id="62730-103">ICLRRuntimeHost::ExecuteApplication 方法</span><span class="sxs-lookup"><span data-stu-id="62730-103">ICLRRuntimeHost::ExecuteApplication Method</span></span>

<span data-ttu-id="62730-104">在基于清单的 ClickOnce 部署方案中用于指定要在新域中激活的应用程序。</span><span class="sxs-lookup"><span data-stu-id="62730-104">Used in manifest-based ClickOnce deployment scenarios to specify the application to be activated in a new domain.</span></span> <span data-ttu-id="62730-105">有关这些方案的详细信息，请参阅 [ClickOnce 安全和部署](/visualstudio/deployment/clickonce-security-and-deployment)。</span><span class="sxs-lookup"><span data-stu-id="62730-105">For more information about these scenarios, see [ClickOnce Security and Deployment](/visualstudio/deployment/clickonce-security-and-deployment).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62730-106">语法</span><span class="sxs-lookup"><span data-stu-id="62730-106">Syntax</span></span>  
  
```cpp  
HRESULT ExecuteApplication(  
    [in] LPCWSTR   pwzAppFullName,  
    [in] DWORD     dwManifestPaths,  
    [in] LPCWSTR   *ppwzManifestPaths,  
    [in] DWORD     dwActivationData,  
    [in] LPCWSTR   *ppwzActivationData,  
    [out] int      *pReturnValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="62730-107">参数</span><span class="sxs-lookup"><span data-stu-id="62730-107">Parameters</span></span>  

 `pwzAppFullName`  
 <span data-ttu-id="62730-108">中为定义的应用程序的完整名称 <xref:System.ApplicationIdentity> 。</span><span class="sxs-lookup"><span data-stu-id="62730-108">[in] The full name of the application, as defined for <xref:System.ApplicationIdentity>.</span></span>  
  
 `dwManifestPaths`  
 <span data-ttu-id="62730-109">中数组中包含的字符串的数目 `ppwzManifestPaths` 。</span><span class="sxs-lookup"><span data-stu-id="62730-109">[in] The number of strings contained in the `ppwzManifestPaths` array.</span></span>  
  
 `ppwzManifestPaths`  
 <span data-ttu-id="62730-110">[in] 可选。</span><span class="sxs-lookup"><span data-stu-id="62730-110">[in] Optional.</span></span> <span data-ttu-id="62730-111">包含应用程序的清单路径的字符串数组。</span><span class="sxs-lookup"><span data-stu-id="62730-111">A string array that contains manifest paths for the application.</span></span>  
  
 `dwActivationData`  
 <span data-ttu-id="62730-112">中数组中包含的字符串的数目 `ppwzActivationData` 。</span><span class="sxs-lookup"><span data-stu-id="62730-112">[in] The number of strings contained in the `ppwzActivationData` array.</span></span>  
  
 `ppwzActivationData`  
 <span data-ttu-id="62730-113">[in] 可选。</span><span class="sxs-lookup"><span data-stu-id="62730-113">[in] Optional.</span></span> <span data-ttu-id="62730-114">一个字符串数组，其中包含应用程序的激活数据，如通过 Web 部署的应用程序的 URL 的查询字符串部分。</span><span class="sxs-lookup"><span data-stu-id="62730-114">A string array that contains the application's activation data, such as the query string portion of the URL for applications deployed over the Web.</span></span>  
  
 `pReturnValue`  
 <span data-ttu-id="62730-115">弄从应用程序的入口点返回的值。</span><span class="sxs-lookup"><span data-stu-id="62730-115">[out] The value returned from the entry point of the application.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="62730-116">返回值</span><span class="sxs-lookup"><span data-stu-id="62730-116">Return Value</span></span>  
  
|<span data-ttu-id="62730-117">HRESULT</span><span class="sxs-lookup"><span data-stu-id="62730-117">HRESULT</span></span>|<span data-ttu-id="62730-118">说明</span><span class="sxs-lookup"><span data-stu-id="62730-118">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="62730-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="62730-119">S_OK</span></span>|<span data-ttu-id="62730-120">`ExecuteApplication` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="62730-120">`ExecuteApplication` returned successfully.</span></span>|  
|<span data-ttu-id="62730-121">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="62730-121">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="62730-122"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="62730-122">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="62730-123">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="62730-123">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="62730-124">调用超时。</span><span class="sxs-lookup"><span data-stu-id="62730-124">The call timed out.</span></span>|  
|<span data-ttu-id="62730-125">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="62730-125">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="62730-126">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="62730-126">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="62730-127">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="62730-127">HOST_E_ABANDONED</span></span>|<span data-ttu-id="62730-128">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="62730-128">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="62730-129">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="62730-129">E_FAIL</span></span>|<span data-ttu-id="62730-130">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="62730-130">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="62730-131">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="62730-131">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="62730-132">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="62730-132">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="62730-133">备注</span><span class="sxs-lookup"><span data-stu-id="62730-133">Remarks</span></span>  

 <span data-ttu-id="62730-134">`ExecuteApplication` 用于在新创建的应用程序域中激活 ClickOnce 应用程序。</span><span class="sxs-lookup"><span data-stu-id="62730-134">`ExecuteApplication` is used to activate ClickOnce applications in a newly created application domain.</span></span>  
  
 <span data-ttu-id="62730-135">`pReturnValue`Output 参数设置为应用程序返回的值。</span><span class="sxs-lookup"><span data-stu-id="62730-135">The `pReturnValue` output parameter is set to the value returned by the application.</span></span> <span data-ttu-id="62730-136">如果为提供 null 值，则不 `pReturnValue` 会 `ExecuteApplication` 失败，但它不返回值。</span><span class="sxs-lookup"><span data-stu-id="62730-136">If you supply a value of null for `pReturnValue`, `ExecuteApplication` does not fail, but it does not return a value.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="62730-137">请不要在调用方法之前调用 [Start 方法](iclrruntimehost-start-method.md) 方法 `ExecuteApplication` 来激活基于清单的应用程序。</span><span class="sxs-lookup"><span data-stu-id="62730-137">Do not call the [Start Method](iclrruntimehost-start-method.md) method before calling the `ExecuteApplication` method to activate a manifest-based application.</span></span> <span data-ttu-id="62730-138">如果 `Start` 首先调用方法， `ExecuteApplication` 方法调用将失败。</span><span class="sxs-lookup"><span data-stu-id="62730-138">If the `Start` method is called first, the `ExecuteApplication` method call will fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="62730-139">要求</span><span class="sxs-lookup"><span data-stu-id="62730-139">Requirements</span></span>  

 <span data-ttu-id="62730-140">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="62730-140">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="62730-141">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="62730-141">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="62730-142">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="62730-142">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="62730-143">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="62730-143">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62730-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="62730-144">See also</span></span>

- <xref:System.ActivationContext>
- <xref:System.AppDomainManager>
- <xref:System.ApplicationIdentity>
- [<span data-ttu-id="62730-145">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="62730-145">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)
- [<span data-ttu-id="62730-146">SetAppDomainManager 方法</span><span class="sxs-lookup"><span data-stu-id="62730-146">SetAppDomainManager Method</span></span>](ihostcontrol-setappdomainmanager-method.md)
- [<span data-ttu-id="62730-147">演练：在设计器中使用 ClickOnce 部署 API 按需下载程序集</span><span class="sxs-lookup"><span data-stu-id="62730-147">Walkthrough: Downloading Assemblies on Demand with the ClickOnce Deployment API Using the Designer</span></span>](/visualstudio/deployment/walkthrough-downloading-assemblies-on-demand-with-the-clickonce-deployment-api-using-the-designer)
