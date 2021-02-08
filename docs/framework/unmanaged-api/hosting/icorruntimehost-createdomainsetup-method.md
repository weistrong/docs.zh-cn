---
description: 了解详细信息： ICorRuntimeHost：： CreateDomainSetup 方法
title: ICorRuntimeHost::CreateDomainSetup 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.CreateDomainSetup
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::CreateDomainSetup
helpviewer_keywords:
- CreateDomainSetup method [.NET Framework hosting]
- ICorRuntimeHost::CreateDomainSetup method [.NET Framework hosting]
ms.assetid: c21dab60-fb65-47d9-8a94-7fd47ca53b48
topic_type:
- apiref
ms.openlocfilehash: b7c2dc55fa9f0d3d5a5c18e38c2c825048ae5f53
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789679"
---
# <a name="icorruntimehostcreatedomainsetup-method"></a><span data-ttu-id="39f91-103">ICorRuntimeHost::CreateDomainSetup 方法</span><span class="sxs-lookup"><span data-stu-id="39f91-103">ICorRuntimeHost::CreateDomainSetup Method</span></span>

<span data-ttu-id="39f91-104">获取实例的 IAppDomainSetup 类型的接口指针 <xref:System.AppDomainSetup?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="39f91-104">Gets an interface pointer of type IAppDomainSetup to an <xref:System.AppDomainSetup?displayProperty=nameWithType> instance.</span></span> <span data-ttu-id="39f91-105">`IAppDomainSetup` 提供用于配置应用程序域在创建之前的各个方面的方法。</span><span class="sxs-lookup"><span data-stu-id="39f91-105">`IAppDomainSetup` provides methods to configure aspects of an application domain before it is created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39f91-106">语法</span><span class="sxs-lookup"><span data-stu-id="39f91-106">Syntax</span></span>  
  
```cpp  
HRESULT CreateDomainSetup (  
    [out] IUnknown** pAppDomainSetup  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="39f91-107">参数</span><span class="sxs-lookup"><span data-stu-id="39f91-107">Parameters</span></span>  

 `pAppDomainSetup`  
 <span data-ttu-id="39f91-108">弄指向实例的接口指针 <xref:System.AppDomainSetup?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="39f91-108">[out] An interface pointer to an <xref:System.AppDomainSetup?displayProperty=nameWithType> instance.</span></span> <span data-ttu-id="39f91-109">此参数的类型为 `IUnknown` ，因此调用方通常应 `QueryInterface` 在此指针上调用，以获取类型的接口指针 `IAppDomainSetup` 。</span><span class="sxs-lookup"><span data-stu-id="39f91-109">This parameter is typed as `IUnknown`, so callers should generally call `QueryInterface` on this pointer to obtain an interface pointer of type `IAppDomainSetup`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="39f91-110">返回值</span><span class="sxs-lookup"><span data-stu-id="39f91-110">Return Value</span></span>  
  
|<span data-ttu-id="39f91-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="39f91-111">HRESULT</span></span>|<span data-ttu-id="39f91-112">说明</span><span class="sxs-lookup"><span data-stu-id="39f91-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="39f91-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="39f91-113">S_OK</span></span>|<span data-ttu-id="39f91-114">操作成功。</span><span class="sxs-lookup"><span data-stu-id="39f91-114">The operation was successful.</span></span>|  
|<span data-ttu-id="39f91-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="39f91-115">S_FALSE</span></span>|<span data-ttu-id="39f91-116">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="39f91-116">The operation failed to complete.</span></span>|  
|<span data-ttu-id="39f91-117">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="39f91-117">E_FAIL</span></span>|<span data-ttu-id="39f91-118">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="39f91-118">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="39f91-119">如果某个方法返回 E_FAIL，则公共语言运行时 (CLR) 在该进程中不再可用。</span><span class="sxs-lookup"><span data-stu-id="39f91-119">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="39f91-120">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="39f91-120">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="39f91-121">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="39f91-121">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="39f91-122">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="39f91-122">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="39f91-123">备注</span><span class="sxs-lookup"><span data-stu-id="39f91-123">Remarks</span></span>  

 <span data-ttu-id="39f91-124">从此方法返回的指针通常作为参数传递给 [CreateDomainEx](icorruntimehost-createdomainex-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="39f91-124">The pointer returned from this method is typically passed as a parameter to the [CreateDomainEx](icorruntimehost-createdomainex-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="39f91-125">要求</span><span class="sxs-lookup"><span data-stu-id="39f91-125">Requirements</span></span>  

 <span data-ttu-id="39f91-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="39f91-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="39f91-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="39f91-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="39f91-128">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="39f91-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="39f91-129">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="39f91-129">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39f91-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="39f91-130">See also</span></span>

- <xref:System._AppDomain>
- <xref:System.AppDomain>
- <xref:System.AppDomainSetup>
- <xref:System.IAppDomainSetup?displayProperty=nameWithType>
- [<span data-ttu-id="39f91-131">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="39f91-131">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
