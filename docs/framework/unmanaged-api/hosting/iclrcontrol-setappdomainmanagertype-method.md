---
description: 了解详细信息： ICLRControl：： SetAppDomainManagerType 方法
title: ICLRControl::SetAppDomainManagerType 方法
ms.date: 03/30/2017
api_name:
- ICLRControl.SetAppDomainManagerType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRControl::SetAppDomainManagerType
helpviewer_keywords:
- SetAppDomainManagerType method, ICLRControl interface [.NET Framework hosting]
- ICLRControl::SetAppDomainManagerType method [.NET Framework hosting]
ms.assetid: ec57828b-2aad-496d-a35a-e45d4bd7fe77
topic_type:
- apiref
ms.openlocfilehash: 20d45a0ab14904c778a6ea821fcd63f85b6b0921
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716661"
---
# <a name="iclrcontrolsetappdomainmanagertype-method"></a><span data-ttu-id="2ddc5-103">ICLRControl::SetAppDomainManagerType 方法</span><span class="sxs-lookup"><span data-stu-id="2ddc5-103">ICLRControl::SetAppDomainManagerType Method</span></span>

<span data-ttu-id="2ddc5-104">将派生自的类型设置 <xref:System.AppDomainManager> 为应用程序域管理器的类型。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-104">Sets a type derived from <xref:System.AppDomainManager> as the type for application domain managers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2ddc5-105">语法</span><span class="sxs-lookup"><span data-stu-id="2ddc5-105">Syntax</span></span>  
  
```cpp  
HRESULT SetAppDomainManagerType (  
    [in] LPCWSTR pwzAppDomainManagerAssembly,  
    [in] LPCWSTR pwzAppDomainManagerType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2ddc5-106">参数</span><span class="sxs-lookup"><span data-stu-id="2ddc5-106">Parameters</span></span>  

 `pwzAppDomainManagerAssembly`  
 <span data-ttu-id="2ddc5-107">中在其中实现从派生的请求类型的程序集的名称 <xref:System.AppDomainManager> 。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-107">[in] The name of the assembly in which the requested type derived from <xref:System.AppDomainManager> is implemented.</span></span>  
  
 `pwzAppDomainManagerType`  
 <span data-ttu-id="2ddc5-108">中在实现的功能的参数中实现的类型的名称 `pwzAppDomainManagerAssembly` <xref:System.AppDomainManager> 。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-108">[in] The name of the type implemented in the `pwzAppDomainManagerAssembly` parameter that implements the capabilities of <xref:System.AppDomainManager>.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2ddc5-109">返回值</span><span class="sxs-lookup"><span data-stu-id="2ddc5-109">Return Value</span></span>  
  
|<span data-ttu-id="2ddc5-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2ddc5-110">HRESULT</span></span>|<span data-ttu-id="2ddc5-111">说明</span><span class="sxs-lookup"><span data-stu-id="2ddc5-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2ddc5-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ddc5-112">S_OK</span></span>|<span data-ttu-id="2ddc5-113">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-113">The method returned successfully.</span></span>|  
|<span data-ttu-id="2ddc5-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="2ddc5-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="2ddc5-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="2ddc5-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2ddc5-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="2ddc5-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-117">The call timed out.</span></span>|  
|<span data-ttu-id="2ddc5-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="2ddc5-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="2ddc5-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="2ddc5-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="2ddc5-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="2ddc5-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="2ddc5-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="2ddc5-122">E_FAIL</span></span>|<span data-ttu-id="2ddc5-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="2ddc5-124">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-124">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="2ddc5-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2ddc5-126">要求</span><span class="sxs-lookup"><span data-stu-id="2ddc5-126">Requirements</span></span>  

 <span data-ttu-id="2ddc5-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2ddc5-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2ddc5-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="2ddc5-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2ddc5-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2ddc5-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2ddc5-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2ddc5-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2ddc5-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="2ddc5-131">See also</span></span>

- [<span data-ttu-id="2ddc5-132">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="2ddc5-132">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="2ddc5-133">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="2ddc5-133">IHostControl Interface</span></span>](ihostcontrol-interface.md)
