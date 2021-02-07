---
description: 了解详细信息： ICLRAppDomainResourceMonitor：： GetCurrentCpuTime 方法
title: ICLRAppDomainResourceMonitor::GetCurrentCpuTime 方法
ms.date: 03/30/2017
api_name:
- ICLRAppDomainResourceMonitor.GetCurrentCpuTime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAppDomainResourceMonitor::GetCurrentCpuTime
helpviewer_keywords:
- ICLRAppDomainResourceMonitor::GetCurrentCpuTime method [.NET Framework hosting]
- GetCurrentCpuTime method [.NET Framework hosting]
ms.assetid: ebc9cc33-fcd6-4cae-9ecb-ea21c51874e6
topic_type:
- apiref
ms.openlocfilehash: ce36bf4ab88f953834d3ff12404bcaadcb42812d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753923"
---
# <a name="iclrappdomainresourcemonitorgetcurrentcputime-method"></a><span data-ttu-id="085ca-103">ICLRAppDomainResourceMonitor::GetCurrentCpuTime 方法</span><span class="sxs-lookup"><span data-stu-id="085ca-103">ICLRAppDomainResourceMonitor::GetCurrentCpuTime Method</span></span>

<span data-ttu-id="085ca-104">获取自应用程序域创建以来在当前应用程序域中执行时所有线程已使用的总处理器时间。</span><span class="sxs-lookup"><span data-stu-id="085ca-104">Gets the total processor time that has been used by all threads while executing in the current application domain, since the application domain was created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="085ca-105">语法</span><span class="sxs-lookup"><span data-stu-id="085ca-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentCpuTime([in]  DWORD dwAppDomainId,  
                          [out] ULONGLONG* pMilliseconds);  
```  
  
## <a name="parameters"></a><span data-ttu-id="085ca-106">参数</span><span class="sxs-lookup"><span data-stu-id="085ca-106">Parameters</span></span>  

 `dwAppDomainId`  
 <span data-ttu-id="085ca-107">中请求的应用程序域的 ID。</span><span class="sxs-lookup"><span data-stu-id="085ca-107">[in] The ID of the requested application domain.</span></span>  
  
 `pMilliseconds`  
 <span data-ttu-id="085ca-108">弄一个指针，指向自创建应用程序域后，所有线程在当前应用程序域中执行时所使用的总处理器时间。</span><span class="sxs-lookup"><span data-stu-id="085ca-108">[out] A pointer to the total processor time that has been used by all threads while executing in the current application domain since the application domain was created.</span></span> <span data-ttu-id="085ca-109">此参数可以为 `null`。</span><span class="sxs-lookup"><span data-stu-id="085ca-109">This parameter can be `null`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="085ca-110">返回值</span><span class="sxs-lookup"><span data-stu-id="085ca-110">Return Value</span></span>  
  
|<span data-ttu-id="085ca-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="085ca-111">HRESULT</span></span>|<span data-ttu-id="085ca-112">说明</span><span class="sxs-lookup"><span data-stu-id="085ca-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="085ca-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="085ca-113">S_OK</span></span>|<span data-ttu-id="085ca-114">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="085ca-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="085ca-115">COR_E_APPDOMAINUNLOADED</span><span class="sxs-lookup"><span data-stu-id="085ca-115">COR_E_APPDOMAINUNLOADED</span></span>|<span data-ttu-id="085ca-116">应用程序域已卸载或不存在。</span><span class="sxs-lookup"><span data-stu-id="085ca-116">The application domain has been unloaded or does not exist.</span></span>|  
|<span data-ttu-id="085ca-117">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="085ca-117">E_FAIL</span></span>|<span data-ttu-id="085ca-118">未启用应用程序域资源监视。</span><span class="sxs-lookup"><span data-stu-id="085ca-118">Application domain resource monitoring is not enabled.</span></span><br /><br /> <span data-ttu-id="085ca-119">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="085ca-119">-or-</span></span><br /><br /> <span data-ttu-id="085ca-120">所有其他失败。</span><span class="sxs-lookup"><span data-stu-id="085ca-120">All other failures.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="085ca-121">备注</span><span class="sxs-lookup"><span data-stu-id="085ca-121">Remarks</span></span>  

 <span data-ttu-id="085ca-122">此方法是托管属性的非托管等效项 <xref:System.AppDomain.MonitoringTotalProcessorTime%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="085ca-122">This method is the unmanaged equivalent of the managed <xref:System.AppDomain.MonitoringTotalProcessorTime%2A?displayProperty=nameWithType> property.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="085ca-123">要求</span><span class="sxs-lookup"><span data-stu-id="085ca-123">Requirements</span></span>  

 <span data-ttu-id="085ca-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="085ca-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="085ca-125">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="085ca-125">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="085ca-126">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="085ca-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="085ca-127">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="085ca-127">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="085ca-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="085ca-128">See also</span></span>

- [<span data-ttu-id="085ca-129">ICLRAppDomainResourceMonitor 接口</span><span class="sxs-lookup"><span data-stu-id="085ca-129">ICLRAppDomainResourceMonitor Interface</span></span>](iclrappdomainresourcemonitor-interface.md)
- [<span data-ttu-id="085ca-130">承载接口</span><span class="sxs-lookup"><span data-stu-id="085ca-130">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="085ca-131">应用程序域资源监视</span><span class="sxs-lookup"><span data-stu-id="085ca-131">Application Domain Resource Monitoring</span></span>](../../../standard/garbage-collection/app-domain-resource-monitoring.md)
- [<span data-ttu-id="085ca-132">承载</span><span class="sxs-lookup"><span data-stu-id="085ca-132">Hosting</span></span>](index.md)
