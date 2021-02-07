---
description: 了解详细信息： ICLRAssemblyIdentityManager：： IsStronglyNamed 方法
title: ICLRAssemblyIdentityManager::IsStronglyNamed 方法
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.IsStronglyNamed
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::IsStronglyNamed
helpviewer_keywords:
- IsStronglyNamed method [.NET Framework hosting]
- ICLRAssemblyIdentityManager::IsStronglyNamed method [.NET Framework hosting]
ms.assetid: 954bd386-2076-4d00-9d46-38c728aa9cab
topic_type:
- apiref
ms.openlocfilehash: f6f1715513fba56e10b10c14c298d3c553fd4652
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716828"
---
# <a name="iclrassemblyidentitymanagerisstronglynamed-method"></a><span data-ttu-id="ef31e-103">ICLRAssemblyIdentityManager::IsStronglyNamed 方法</span><span class="sxs-lookup"><span data-stu-id="ef31e-103">ICLRAssemblyIdentityManager::IsStronglyNamed Method</span></span>

<span data-ttu-id="ef31e-104">获取一个值，该值指示指定的程序集是否具有强名称。</span><span class="sxs-lookup"><span data-stu-id="ef31e-104">Gets a value that indicates whether the specified assembly is strongly named.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ef31e-105">语法</span><span class="sxs-lookup"><span data-stu-id="ef31e-105">Syntax</span></span>  
  
```cpp  
RESULT IsStronglyNamed (  
    [in]  LPCWSTR  pwzAssemblyIdentity,  
    [out] BOOL    *pbIsStronglyNamed  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ef31e-106">参数</span><span class="sxs-lookup"><span data-stu-id="ef31e-106">Parameters</span></span>  

 `pwzAssemblyIdentity`  
 <span data-ttu-id="ef31e-107">中要计算的程序集的不透明规范程序集标识数据。</span><span class="sxs-lookup"><span data-stu-id="ef31e-107">[in] The opaque canonical assembly identity data of the assembly to be evaluated.</span></span>  
  
 `pbIsStronglyNamed`  
 <span data-ttu-id="ef31e-108">[out] `true` 如果参数引用的程序集 `pwzAssemblyIdentity` 具有强名称，则为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="ef31e-108">[out] `true`, if the assembly referenced by the `pwzAssemblyIdentity` parameter is strongly named; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ef31e-109">返回值</span><span class="sxs-lookup"><span data-stu-id="ef31e-109">Return Value</span></span>  
  
|<span data-ttu-id="ef31e-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ef31e-110">HRESULT</span></span>|<span data-ttu-id="ef31e-111">说明</span><span class="sxs-lookup"><span data-stu-id="ef31e-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ef31e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef31e-112">S_OK</span></span>|<span data-ttu-id="ef31e-113">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ef31e-113">The method returned successfully.</span></span>|  
|<span data-ttu-id="ef31e-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ef31e-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ef31e-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ef31e-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ef31e-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ef31e-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ef31e-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ef31e-117">The call timed out.</span></span>|  
|<span data-ttu-id="ef31e-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ef31e-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ef31e-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ef31e-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ef31e-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ef31e-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ef31e-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ef31e-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ef31e-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ef31e-122">E_FAIL</span></span>|<span data-ttu-id="ef31e-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ef31e-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ef31e-124">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ef31e-124">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ef31e-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ef31e-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ef31e-126">要求</span><span class="sxs-lookup"><span data-stu-id="ef31e-126">Requirements</span></span>  

 <span data-ttu-id="ef31e-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ef31e-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ef31e-128">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ef31e-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ef31e-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ef31e-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ef31e-130">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ef31e-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef31e-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="ef31e-131">See also</span></span>

- [<span data-ttu-id="ef31e-132">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="ef31e-132">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
