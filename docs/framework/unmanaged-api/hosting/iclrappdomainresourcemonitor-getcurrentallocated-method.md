---
description: 了解详细信息： ICLRAppDomainResourceMonitor：： GetCurrentAllocated 方法
title: ICLRAppDomainResourceMonitor::GetCurrentAllocated 方法
ms.date: 03/30/2017
api_name:
- ICLRAppDomainResourceMonitor.GetCurrentAllocated
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAppDomainResourceMonitor::GetCurrentAllocated
helpviewer_keywords:
- GetCurrentAllocated method [.NET Framework hosting]
- ICLRAppDomainResourceMonitor::GetCurrentAllocated method [.NET Framework hosting]
ms.assetid: 7bab209c-efd4-44c2-af30-61abab0ae2fc
topic_type:
- apiref
ms.openlocfilehash: d7aaf31f775a9d6e2af95cf1a832c78587a85fe1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753947"
---
# <a name="iclrappdomainresourcemonitorgetcurrentallocated-method"></a><span data-ttu-id="57086-103">ICLRAppDomainResourceMonitor::GetCurrentAllocated 方法</span><span class="sxs-lookup"><span data-stu-id="57086-103">ICLRAppDomainResourceMonitor::GetCurrentAllocated Method</span></span>

<span data-ttu-id="57086-104">获取应用程序域创建后所做的所有内存分配的总大小（以字节为单位），而不会减去已进行垃圾回收的内存。</span><span class="sxs-lookup"><span data-stu-id="57086-104">Gets the total size, in bytes, of all memory allocations that have been made by the application domain since it was created, without subtracting memory that has been garbage-collected.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57086-105">语法</span><span class="sxs-lookup"><span data-stu-id="57086-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentAllocated([in]  DWORD dwAppDomainId,  
                            [out] ULONGLONG* pBytesAllocated);  
```  
  
## <a name="parameters"></a><span data-ttu-id="57086-106">参数</span><span class="sxs-lookup"><span data-stu-id="57086-106">Parameters</span></span>  

 `dwAppDomainId`  
 <span data-ttu-id="57086-107">中请求的应用程序域的 ID。</span><span class="sxs-lookup"><span data-stu-id="57086-107">[in] The ID of the requested application domain.</span></span>  
  
 `pBytesAllocated`  
 <span data-ttu-id="57086-108">弄一个指针，指向所有内存分配的总大小。</span><span class="sxs-lookup"><span data-stu-id="57086-108">[out] A pointer to the total size of all memory allocations.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="57086-109">返回值</span><span class="sxs-lookup"><span data-stu-id="57086-109">Return Value</span></span>  

 <span data-ttu-id="57086-110">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="57086-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="57086-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="57086-111">HRESULT</span></span>|<span data-ttu-id="57086-112">说明</span><span class="sxs-lookup"><span data-stu-id="57086-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="57086-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="57086-113">S_OK</span></span>|<span data-ttu-id="57086-114">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="57086-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="57086-115">COR_E_APPDOMAINUNLOADED</span><span class="sxs-lookup"><span data-stu-id="57086-115">COR_E_APPDOMAINUNLOADED</span></span>|<span data-ttu-id="57086-116">应用程序域已卸载或不存在。</span><span class="sxs-lookup"><span data-stu-id="57086-116">The application domain has been unloaded or does not exist.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="57086-117">备注</span><span class="sxs-lookup"><span data-stu-id="57086-117">Remarks</span></span>  

 <span data-ttu-id="57086-118">此方法是托管属性的非托管等效项 <xref:System.AppDomain.MonitoringTotalAllocatedMemorySize%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="57086-118">This method is the unmanaged equivalent of the managed <xref:System.AppDomain.MonitoringTotalAllocatedMemorySize%2A?displayProperty=nameWithType> property.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57086-119">要求</span><span class="sxs-lookup"><span data-stu-id="57086-119">Requirements</span></span>  

 <span data-ttu-id="57086-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="57086-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="57086-121">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="57086-121">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="57086-122">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="57086-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="57086-123">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="57086-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57086-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="57086-124">See also</span></span>

- [<span data-ttu-id="57086-125">ICLRAppDomainResourceMonitor 接口</span><span class="sxs-lookup"><span data-stu-id="57086-125">ICLRAppDomainResourceMonitor Interface</span></span>](iclrappdomainresourcemonitor-interface.md)
- [<span data-ttu-id="57086-126">应用程序域资源监视</span><span class="sxs-lookup"><span data-stu-id="57086-126">Application Domain Resource Monitoring</span></span>](../../../standard/garbage-collection/app-domain-resource-monitoring.md)
- [<span data-ttu-id="57086-127">承载接口</span><span class="sxs-lookup"><span data-stu-id="57086-127">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="57086-128">承载</span><span class="sxs-lookup"><span data-stu-id="57086-128">Hosting</span></span>](index.md)
