---
description: 了解详细信息： ICorRuntimeHost：： CreateDomain 方法
title: ICorRuntimeHost::CreateDomain 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.CreateDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::CreateDomain
helpviewer_keywords:
- CreateDomain method [.NET Framework hosting]
- ICorRuntimeHost::CreateDomain method [.NET Framework hosting]
ms.assetid: b96c5ef3-a9df-4c7c-9952-432d3272cb5c
topic_type:
- apiref
ms.openlocfilehash: 6173d74d97ddb9dec619db8583036ec763a9e293
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789705"
---
# <a name="icorruntimehostcreatedomain-method"></a><span data-ttu-id="c073d-103">ICorRuntimeHost::CreateDomain 方法</span><span class="sxs-lookup"><span data-stu-id="c073d-103">ICorRuntimeHost::CreateDomain Method</span></span>

<span data-ttu-id="c073d-104">创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="c073d-104">Creates an application domain.</span></span> <span data-ttu-id="c073d-105">调用方接收类型为的实例的接口指针 <xref:System._AppDomain> <xref:System.AppDomain?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="c073d-105">The caller receives an interface pointer of type <xref:System._AppDomain> to an instance of type <xref:System.AppDomain?displayProperty=nameWithType>.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c073d-106">语法</span><span class="sxs-lookup"><span data-stu-id="c073d-106">Syntax</span></span>  
  
```cpp  
HRESULT CreateDomain (  
    [in] LPWSTR    pwzFriendlyName,  
    [in] IUnknown* pIdentityArray,  
    [out] void   **pAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c073d-107">参数</span><span class="sxs-lookup"><span data-stu-id="c073d-107">Parameters</span></span>  

 `pwzFriendlyName`  
 <span data-ttu-id="c073d-108">中用于给域指定友好名称的可选参数。</span><span class="sxs-lookup"><span data-stu-id="c073d-108">[in] An optional parameter used to give a friendly name to the domain.</span></span> <span data-ttu-id="c073d-109">此友好名称可在用户界面（例如调试器）中显示，以标识域。</span><span class="sxs-lookup"><span data-stu-id="c073d-109">This friendly name can be displayed in user interfaces such as debuggers to identify the domain.</span></span>  
  
 `pIdentityArray`  
 <span data-ttu-id="c073d-110">中指向实例的可选指针数组， `IIdentity` 这些实例表示通过安全策略映射以建立权限集的证据。</span><span class="sxs-lookup"><span data-stu-id="c073d-110">[in] An optional array of pointers to `IIdentity` instances that represent evidence mapped through security policy to establish a  permission set.</span></span> <span data-ttu-id="c073d-111">`IIdentity`可以通过调用[CreateEvidence](icorruntimehost-createevidence-method.md)方法来获取对象。</span><span class="sxs-lookup"><span data-stu-id="c073d-111">An `IIdentity` object can be obtained by calling the [CreateEvidence](icorruntimehost-createevidence-method.md) method.</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="c073d-112">弄类型为的接口指针 <xref:System._AppDomain> <xref:System.AppDomain?displayProperty=nameWithType> ，可用于进一步控制域。</span><span class="sxs-lookup"><span data-stu-id="c073d-112">[out] An interface pointer of type <xref:System._AppDomain> to an instance of <xref:System.AppDomain?displayProperty=nameWithType> that can be used to further control the domain.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c073d-113">返回值</span><span class="sxs-lookup"><span data-stu-id="c073d-113">Return Value</span></span>  
  
|<span data-ttu-id="c073d-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c073d-114">HRESULT</span></span>|<span data-ttu-id="c073d-115">说明</span><span class="sxs-lookup"><span data-stu-id="c073d-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c073d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c073d-116">S_OK</span></span>|<span data-ttu-id="c073d-117">操作成功。</span><span class="sxs-lookup"><span data-stu-id="c073d-117">The operation was successful.</span></span>|  
|<span data-ttu-id="c073d-118">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="c073d-118">S_FALSE</span></span>|<span data-ttu-id="c073d-119">操作未能完成。</span><span class="sxs-lookup"><span data-stu-id="c073d-119">The operation failed to complete.</span></span>|  
|<span data-ttu-id="c073d-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c073d-120">E_FAIL</span></span>|<span data-ttu-id="c073d-121">发生了未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="c073d-121">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="c073d-122">如果某个方法返回 E_FAIL，则公共语言运行时 (CLR) 在该进程中不再可用。</span><span class="sxs-lookup"><span data-stu-id="c073d-122">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="c073d-123">对任何宿主 Api 的后续调用都会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="c073d-123">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="c073d-124">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c073d-124">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c073d-125">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="c073d-125">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c073d-126">要求</span><span class="sxs-lookup"><span data-stu-id="c073d-126">Requirements</span></span>  

 <span data-ttu-id="c073d-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c073d-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c073d-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c073d-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c073d-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c073d-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c073d-130">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="c073d-130">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c073d-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="c073d-131">See also</span></span>

- <xref:System._AppDomain>
- <xref:System.AppDomain>
- [<span data-ttu-id="c073d-132">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="c073d-132">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
