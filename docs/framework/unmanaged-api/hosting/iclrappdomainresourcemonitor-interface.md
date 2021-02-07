---
description: 了解详细信息： ICLRAppDomainResourceMonitor 接口
title: ICLRAppDomainResourceMonitor 接口
ms.date: 03/30/2017
api_name:
- ICLRAppDomainResourceMonitor
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAppDomainResourceMonitor
helpviewer_keywords:
- ICLRAppDomainResourceMonitor interface [.NET Framework hosting]
ms.assetid: 72fa83a1-8997-41d7-b355-ab177a24a303
topic_type:
- apiref
ms.openlocfilehash: 85321eabedb6912efabe57553732f8c6a4063155
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753895"
---
# <a name="iclrappdomainresourcemonitor-interface"></a><span data-ttu-id="8f8cc-103">ICLRAppDomainResourceMonitor 接口</span><span class="sxs-lookup"><span data-stu-id="8f8cc-103">ICLRAppDomainResourceMonitor Interface</span></span>

<span data-ttu-id="8f8cc-104">提供检查应用程序域的内存和 CPU 使用情况的方法。</span><span class="sxs-lookup"><span data-stu-id="8f8cc-104">Provides methods that inspect an application domain's memory and CPU usage.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8f8cc-105">方法</span><span class="sxs-lookup"><span data-stu-id="8f8cc-105">Methods</span></span>  
  
|<span data-ttu-id="8f8cc-106">方法</span><span class="sxs-lookup"><span data-stu-id="8f8cc-106">Method</span></span>|<span data-ttu-id="8f8cc-107">说明</span><span class="sxs-lookup"><span data-stu-id="8f8cc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8f8cc-108">GetCurrentAllocated 方法</span><span class="sxs-lookup"><span data-stu-id="8f8cc-108">GetCurrentAllocated Method</span></span>](iclrappdomainresourcemonitor-getcurrentallocated-method.md)|<span data-ttu-id="8f8cc-109">获取应用程序域创建后所做的所有内存分配的总大小（以字节为单位），而不会减去已进行垃圾回收的内存。</span><span class="sxs-lookup"><span data-stu-id="8f8cc-109">Gets the total size, in bytes, of all memory allocations that have been made by the application domain since it was created, without subtracting memory that has been garbage-collected.</span></span>|  
|[<span data-ttu-id="8f8cc-110">GetCurrentSurvived 方法</span><span class="sxs-lookup"><span data-stu-id="8f8cc-110">GetCurrentSurvived Method</span></span>](iclrappdomainresourcemonitor-getcurrentsurvived-method.md)|<span data-ttu-id="8f8cc-111">获取当前应用程序域引用的最后一个完整的、阻止的垃圾回收和所引用的字节数。</span><span class="sxs-lookup"><span data-stu-id="8f8cc-111">Gets the number of bytes that survived the last full, blocking garbage collection and that are referenced by the current application domain.</span></span>|  
|[<span data-ttu-id="8f8cc-112">GetCurrentCpuTime 方法</span><span class="sxs-lookup"><span data-stu-id="8f8cc-112">GetCurrentCpuTime Method</span></span>](iclrappdomainresourcemonitor-getcurrentcputime-method.md)|<span data-ttu-id="8f8cc-113">获取自应用程序域创建以来在当前应用程序域中执行时所有线程已使用的总处理器时间。</span><span class="sxs-lookup"><span data-stu-id="8f8cc-113">Gets the total processor time that has been used by all threads while executing in the current application domain, since the application domain was created.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8f8cc-114">备注</span><span class="sxs-lookup"><span data-stu-id="8f8cc-114">Remarks</span></span>  

 <span data-ttu-id="8f8cc-115">`ICLRAppDomainResourceMonitor`接口提供类似于以下托管属性的功能：</span><span class="sxs-lookup"><span data-stu-id="8f8cc-115">The `ICLRAppDomainResourceMonitor` interface provides functionality that is similar to the following managed properties:</span></span>  
  
- <xref:System.AppDomain.MonitoringIsEnabled%2A?displayProperty=nameWithType>  
  
- <xref:System.AppDomain.MonitoringTotalProcessorTime%2A?displayProperty=nameWithType>  
  
- <xref:System.AppDomain.MonitoringTotalAllocatedMemorySize%2A?displayProperty=nameWithType>  
  
- <xref:System.AppDomain.MonitoringSurvivedProcessMemorySize%2A?displayProperty=nameWithType>  
  
- <xref:System.AppDomain.MonitoringSurvivedMemorySize%2A?displayProperty=nameWithType>  
  
## <a name="requirements"></a><span data-ttu-id="8f8cc-116">要求</span><span class="sxs-lookup"><span data-stu-id="8f8cc-116">Requirements</span></span>  

 <span data-ttu-id="8f8cc-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8f8cc-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8f8cc-118">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="8f8cc-118">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="8f8cc-119">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8f8cc-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8f8cc-120">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8f8cc-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f8cc-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="8f8cc-121">See also</span></span>

- [<span data-ttu-id="8f8cc-122">\<appDomainResourceMonitoring> 元素</span><span class="sxs-lookup"><span data-stu-id="8f8cc-122">\<appDomainResourceMonitoring> Element</span></span>](../../configure-apps/file-schema/runtime/appdomainresourcemonitoring-element.md)
- [<span data-ttu-id="8f8cc-123">应用程序域资源监视</span><span class="sxs-lookup"><span data-stu-id="8f8cc-123">Application Domain Resource Monitoring</span></span>](../../../standard/garbage-collection/app-domain-resource-monitoring.md)
- [<span data-ttu-id="8f8cc-124">承载接口</span><span class="sxs-lookup"><span data-stu-id="8f8cc-124">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="8f8cc-125">承载</span><span class="sxs-lookup"><span data-stu-id="8f8cc-125">Hosting</span></span>](index.md)
