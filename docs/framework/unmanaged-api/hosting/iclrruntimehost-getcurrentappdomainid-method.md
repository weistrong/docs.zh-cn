---
description: 了解详细信息： ICLRRuntimeHost：： GetCurrentAppDomainId 方法
title: ICLRRuntimeHost::GetCurrentAppDomainId 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.GetCurrentAppDomainId
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::GetCurrentAppDomainId
helpviewer_keywords:
- ICLRRuntimeHost::GetCurrentAppDomainId method [.NET Framework hosting]
- GetCurrentAppDomainId method [.NET Framework hosting]
ms.assetid: 33800475-7815-4976-8aca-a1038761a2ef
topic_type:
- apiref
ms.openlocfilehash: 88d5288e2e8ee7d8d1f5430261e21052334240be
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799717"
---
# <a name="iclrruntimehostgetcurrentappdomainid-method"></a><span data-ttu-id="350f3-103">ICLRRuntimeHost::GetCurrentAppDomainId 方法</span><span class="sxs-lookup"><span data-stu-id="350f3-103">ICLRRuntimeHost::GetCurrentAppDomainId Method</span></span>

<span data-ttu-id="350f3-104">获取当前正在执行的的数值标识符 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="350f3-104">Gets the numeric identifier of the <xref:System.AppDomain> that is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="350f3-105">语法</span><span class="sxs-lookup"><span data-stu-id="350f3-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentAppDomainId(  
    [out] DWORD* pdwAppDomainId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="350f3-106">参数</span><span class="sxs-lookup"><span data-stu-id="350f3-106">Parameters</span></span>  

 `pdwAppDomainId`  
 <span data-ttu-id="350f3-107">弄当前正在执行的的数值标识符 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="350f3-107">[out] The numeric identifier of the <xref:System.AppDomain> that is currently executing.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="350f3-108">返回值</span><span class="sxs-lookup"><span data-stu-id="350f3-108">Return Value</span></span>  
  
|<span data-ttu-id="350f3-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="350f3-109">HRESULT</span></span>|<span data-ttu-id="350f3-110">说明</span><span class="sxs-lookup"><span data-stu-id="350f3-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="350f3-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="350f3-111">S_OK</span></span>|<span data-ttu-id="350f3-112">`GetCurrentAppDomainId` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="350f3-112">`GetCurrentAppDomainId` returned successfully.</span></span>|  
|<span data-ttu-id="350f3-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="350f3-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="350f3-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="350f3-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="350f3-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="350f3-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="350f3-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="350f3-116">The call timed out.</span></span>|  
|<span data-ttu-id="350f3-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="350f3-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="350f3-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="350f3-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="350f3-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="350f3-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="350f3-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="350f3-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="350f3-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="350f3-121">E_FAIL</span></span>|<span data-ttu-id="350f3-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="350f3-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="350f3-123">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="350f3-123">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="350f3-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="350f3-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="350f3-125">备注</span><span class="sxs-lookup"><span data-stu-id="350f3-125">Remarks</span></span>  

 <span data-ttu-id="350f3-126">`pdwAppDomainId`参数设置为 <xref:System.AppDomain.Id%2A> 当前线程正在其中执行的的属性的值 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="350f3-126">The `pdwAppDomainId` parameter is set to the value of the <xref:System.AppDomain.Id%2A> property of the <xref:System.AppDomain> in which the current thread is executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="350f3-127">要求</span><span class="sxs-lookup"><span data-stu-id="350f3-127">Requirements</span></span>  

 <span data-ttu-id="350f3-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="350f3-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="350f3-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="350f3-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="350f3-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="350f3-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="350f3-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="350f3-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="350f3-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="350f3-132">See also</span></span>

- <xref:System.AppDomain>
- <xref:System.AppDomainManager>
- [<span data-ttu-id="350f3-133">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="350f3-133">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)
