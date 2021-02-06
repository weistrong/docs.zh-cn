---
description: 了解详细信息： ICLRHostProtectionManager：： SetProtectedCategories 方法
title: ICLRHostProtectionManager::SetProtectedCategories 方法
ms.date: 03/30/2017
api_name:
- ICLRHostProtectionManager.SetProtectedCategories
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostProtectionManager::SetProtectedCategories
helpviewer_keywords:
- SetProtectedCategories method [.NET Framework hosting]
- ICLRHostProtectionManager::SetProtectedCategories method [.NET Framework hosting]
ms.assetid: fa21dc7b-5da7-440b-b59e-9180e5181f9d
topic_type:
- apiref
ms.openlocfilehash: 9138c31ea1a2d9b7ebeaeac8ef5ef9305eabef8d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637529"
---
# <a name="iclrhostprotectionmanagersetprotectedcategories-method"></a><span data-ttu-id="bce80-103">ICLRHostProtectionManager::SetProtectedCategories 方法</span><span class="sxs-lookup"><span data-stu-id="bce80-103">ICLRHostProtectionManager::SetProtectedCategories Method</span></span>

<span data-ttu-id="bce80-104">指定应阻止在部分受信任代码中运行的托管类型和成员的类别。</span><span class="sxs-lookup"><span data-stu-id="bce80-104">Specifies which categories of managed types and members should be blocked from running in partially trusted code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bce80-105">语法</span><span class="sxs-lookup"><span data-stu-id="bce80-105">Syntax</span></span>  
  
```cpp  
HRESULT SetProtectedCategories (  
    [in] EApiCategories  categories  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bce80-106">参数</span><span class="sxs-lookup"><span data-stu-id="bce80-106">Parameters</span></span>  

 `categories`  
 <span data-ttu-id="bce80-107">中 [EApiCategories](eapicategories-enumeration.md) 值的组合，指示应阻止托管类型和成员的哪些类别在部分受信任的代码中运行。</span><span class="sxs-lookup"><span data-stu-id="bce80-107">[in] A combination of [EApiCategories](eapicategories-enumeration.md) values, indicating which categories of managed types and members should be blocked from running in partially trusted code.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bce80-108">返回值</span><span class="sxs-lookup"><span data-stu-id="bce80-108">Return Value</span></span>  
  
|<span data-ttu-id="bce80-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bce80-109">HRESULT</span></span>|<span data-ttu-id="bce80-110">说明</span><span class="sxs-lookup"><span data-stu-id="bce80-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bce80-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="bce80-111">S_OK</span></span>|<span data-ttu-id="bce80-112">`SetProtectedCategories` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="bce80-112">`SetProtectedCategories` returned successfully.</span></span>|  
|<span data-ttu-id="bce80-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bce80-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bce80-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="bce80-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bce80-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bce80-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bce80-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="bce80-116">The call timed out.</span></span>|  
|<span data-ttu-id="bce80-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bce80-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bce80-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="bce80-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bce80-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bce80-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bce80-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="bce80-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="bce80-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bce80-121">E_FAIL</span></span>|<span data-ttu-id="bce80-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="bce80-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bce80-123">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="bce80-123">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bce80-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="bce80-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bce80-125">备注</span><span class="sxs-lookup"><span data-stu-id="bce80-125">Remarks</span></span>  

 <span data-ttu-id="bce80-126">每个 `EApiCategories` 值都是指托管类型和成员的列表。</span><span class="sxs-lookup"><span data-stu-id="bce80-126">Each `EApiCategories` value refers to a list of managed types and members.</span></span> <span data-ttu-id="bce80-127">`EApiCategories`枚举和方法与 `SetProtectedCategories` 托管类直接相关 <xref:System.Security.Permissions.HostProtectionAttribute> ，后者用于标记公开与所述的类别对应的功能的托管类型和成员 `EApiCategories` 。</span><span class="sxs-lookup"><span data-stu-id="bce80-127">The `EApiCategories` enumeration and the `SetProtectedCategories` method are directly related to the managed <xref:System.Security.Permissions.HostProtectionAttribute> class, which is used to mark managed types and members that expose capabilities corresponding to the categories described by `EApiCategories`.</span></span> <span data-ttu-id="bce80-128">有关详细信息，请参阅 <xref:System.Security.Permissions.HostProtectionAttribute> 和 <xref:System.Security.Permissions.HostProtectionResource> 枚举，后者直接对应于 `EApiCategories` 。</span><span class="sxs-lookup"><span data-stu-id="bce80-128">For more information, see <xref:System.Security.Permissions.HostProtectionAttribute> and the <xref:System.Security.Permissions.HostProtectionResource> enumeration, which directly corresponds to `EApiCategories`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bce80-129">要求</span><span class="sxs-lookup"><span data-stu-id="bce80-129">Requirements</span></span>  

 <span data-ttu-id="bce80-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bce80-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bce80-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="bce80-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bce80-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bce80-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bce80-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bce80-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bce80-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="bce80-134">See also</span></span>

- <xref:System.Security.Permissions.HostProtectionAttribute>
- <xref:System.Security.Permissions.HostProtectionResource>
- [<span data-ttu-id="bce80-135">EApiCategories 枚举</span><span class="sxs-lookup"><span data-stu-id="bce80-135">EApiCategories Enumeration</span></span>](eapicategories-enumeration.md)
- [<span data-ttu-id="bce80-136">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="bce80-136">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="bce80-137">ICLRHostProtectionManager 接口</span><span class="sxs-lookup"><span data-stu-id="bce80-137">ICLRHostProtectionManager Interface</span></span>](iclrhostprotectionmanager-interface.md)
