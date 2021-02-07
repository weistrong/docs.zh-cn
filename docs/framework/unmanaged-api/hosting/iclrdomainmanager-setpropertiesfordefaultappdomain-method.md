---
description: 了解详细信息： ICLRDomainManager：： SetPropertiesForDefaultAppDomain 方法
title: ICLRDomainManager::SetPropertiesForDefaultAppDomain 方法
ms.date: 03/30/2017
api_name:
- ICLRDomainManager.SetPropertiesForDefaultAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDomainManager::SetPropertiesForDefaultAppDomain
helpviewer_keywords:
- ICLRDomainManager::SetPropertiesForDefaultAppDomain method [.NET Framework hosting]
- SetPropertiesForDefaultAppDomain method [.NET Framework hosting]
ms.assetid: 43e61c4b-c435-45ec-9ef6-c68403aa4200
ms.openlocfilehash: 08e6c885d5d089fa22c30a4e3cef69480b840031
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689438"
---
# <a name="iclrdomainmanagersetpropertiesfordefaultappdomain-method"></a><span data-ttu-id="fcdfa-103">ICLRDomainManager::SetPropertiesForDefaultAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="fcdfa-103">ICLRDomainManager::SetPropertiesForDefaultAppDomain Method</span></span>

<span data-ttu-id="fcdfa-104">设置将用于初始化默认应用程序域的属性。</span><span class="sxs-lookup"><span data-stu-id="fcdfa-104">Sets properties that will be used to initialize the default application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fcdfa-105">语法</span><span class="sxs-lookup"><span data-stu-id="fcdfa-105">Syntax</span></span>  
  
```cpp  
HRESULT SetPropertiesForDefaultAppDomain(  
    [in] DWORD nProperties,  
    [in] LPCWSTR *pwszPropertyNames,  
    [in] LPCWSTR *pwszPropertyValues  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fcdfa-106">参数</span><span class="sxs-lookup"><span data-stu-id="fcdfa-106">Parameters</span></span>  

 `nProperties`  
 <span data-ttu-id="fcdfa-107">中和中的项数 `pwszPropertyNames` `pwszPropertyValues` 。</span><span class="sxs-lookup"><span data-stu-id="fcdfa-107">[in] The number of entries in `pwszPropertyNames` and `pwszPropertyValues`.</span></span>  
  
 `pwszPropertyNames`  
 <span data-ttu-id="fcdfa-108">中属性名称的数组; 如果没有属性，则为 null。</span><span class="sxs-lookup"><span data-stu-id="fcdfa-108">[in] An array of property names, or null if there are no properties.</span></span> <span data-ttu-id="fcdfa-109">目前，此方法识别的唯一属性名称为 "PARTIAL_TRUST_VISIBLE_ASSEMBLIES"。</span><span class="sxs-lookup"><span data-stu-id="fcdfa-109">Currently, the only property name that is recognized by this method is "PARTIAL_TRUST_VISIBLE_ASSEMBLIES".</span></span>  
  
 `pwszPropertyValues`  
 <span data-ttu-id="fcdfa-110">中属性值的数组; 如果没有属性，则为 null。</span><span class="sxs-lookup"><span data-stu-id="fcdfa-110">[in] An array of property values, or null if there are no properties.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fcdfa-111">返回值</span><span class="sxs-lookup"><span data-stu-id="fcdfa-111">Return Value</span></span>  

 <span data-ttu-id="fcdfa-112">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="fcdfa-112">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="fcdfa-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fcdfa-113">HRESULT</span></span>|<span data-ttu-id="fcdfa-114">说明</span><span class="sxs-lookup"><span data-stu-id="fcdfa-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fcdfa-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="fcdfa-115">S_OK</span></span>|<span data-ttu-id="fcdfa-116">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="fcdfa-116">The method completed successfully.</span></span>|  
|<span data-ttu-id="fcdfa-117">HRESULT_FROM_WIN32 (ERROR_UNKNOWN_PROPERTY) </span><span class="sxs-lookup"><span data-stu-id="fcdfa-117">HRESULT_FROM_WIN32(ERROR_UNKNOWN_PROPERTY)</span></span>|<span data-ttu-id="fcdfa-118">`pwszPropertyNames` 包含此方法无法识别的属性名称。</span><span class="sxs-lookup"><span data-stu-id="fcdfa-118">`pwszPropertyNames` includes a property name that is not recognized by this method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fcdfa-119">备注</span><span class="sxs-lookup"><span data-stu-id="fcdfa-119">Remarks</span></span>  

 <span data-ttu-id="fcdfa-120">"PARTIAL_TRUST_VISIBLE_ASSEMBLIES" 的属性值是一个程序集的列表，这些程序集具有 <xref:System.Security.AllowPartiallyTrustedCallersAttribute> 带有标志的条件性 (APTCA) 特性 <xref:System.Security.PartialTrustVisibilityLevel.NotVisibleByDefault?displayProperty=nameWithType> ，在默认应用程序域中对部分受信任的调用方可见。</span><span class="sxs-lookup"><span data-stu-id="fcdfa-120">The property value for "PARTIAL_TRUST_VISIBLE_ASSEMBLIES" is a list of assemblies that have the conditional <xref:System.Security.AllowPartiallyTrustedCallersAttribute> (APTCA) attribute with the <xref:System.Security.PartialTrustVisibilityLevel.NotVisibleByDefault?displayProperty=nameWithType> flag, which are to be made visible to partially trusted callers in the default application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fcdfa-121">要求</span><span class="sxs-lookup"><span data-stu-id="fcdfa-121">Requirements</span></span>  

 <span data-ttu-id="fcdfa-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fcdfa-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fcdfa-123">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="fcdfa-123">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="fcdfa-124">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fcdfa-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fcdfa-125">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fcdfa-125">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fcdfa-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="fcdfa-126">See also</span></span>

- [<span data-ttu-id="fcdfa-127">承载</span><span class="sxs-lookup"><span data-stu-id="fcdfa-127">Hosting</span></span>](index.md)
- [<span data-ttu-id="fcdfa-128">ICLRDomainManager 接口</span><span class="sxs-lookup"><span data-stu-id="fcdfa-128">ICLRDomainManager Interface</span></span>](iclrdomainmanager-interface.md)
