---
description: 了解详细信息： IHostControl：： SetAppDomainManager 方法
title: IHostControl::SetAppDomainManager 方法
ms.date: 03/30/2017
api_name:
- IHostControl.SetAppDomainManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostControl::SetAppDomainManager
helpviewer_keywords:
- IHostControl::SetAppDomainManager method [.NET Framework hosting]
- SetAppDomainManager method [.NET Framework hosting]
ms.assetid: 6562bbe7-0d67-4c50-a958-3a18cf680375
topic_type:
- apiref
ms.openlocfilehash: 1fc5efc0afad73d1805338140f186a50913ca542
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708887"
---
# <a name="ihostcontrolsetappdomainmanager-method"></a><span data-ttu-id="cd071-103">IHostControl::SetAppDomainManager 方法</span><span class="sxs-lookup"><span data-stu-id="cd071-103">IHostControl::SetAppDomainManager Method</span></span>

<span data-ttu-id="cd071-104">通知宿主已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="cd071-104">Notifies the host that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd071-105">语法</span><span class="sxs-lookup"><span data-stu-id="cd071-105">Syntax</span></span>  
  
```cpp  
HRESULT SetAppDomainManager (  
    [in] DWORD     dwAppDomainID,  
    [in] IUnknown* pUnkAppDomainManager  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cd071-106">参数</span><span class="sxs-lookup"><span data-stu-id="cd071-106">Parameters</span></span>  

 `dwAppDomainID`  
 <span data-ttu-id="cd071-107">中选定的的数值标识符 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="cd071-107">[in] The numeric identifier of the selected <xref:System.AppDomain>.</span></span>  
  
 `pUnkAppDomainManager`  
 <span data-ttu-id="cd071-108">中指向 <xref:System.AppDomainManager> 宿主作为实现的对象的指针 `IUnknown` 。</span><span class="sxs-lookup"><span data-stu-id="cd071-108">[in] A pointer to the <xref:System.AppDomainManager> object that the host implements as `IUnknown`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cd071-109">返回值</span><span class="sxs-lookup"><span data-stu-id="cd071-109">Return Value</span></span>  
  
|<span data-ttu-id="cd071-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="cd071-110">HRESULT</span></span>|<span data-ttu-id="cd071-111">说明</span><span class="sxs-lookup"><span data-stu-id="cd071-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="cd071-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd071-112">S_OK</span></span>|<span data-ttu-id="cd071-113">`SetAppDomainManager` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="cd071-113">`SetAppDomainManager` returned successfully.</span></span>|  
|<span data-ttu-id="cd071-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="cd071-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="cd071-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="cd071-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="cd071-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="cd071-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="cd071-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="cd071-117">The call timed out.</span></span>|  
|<span data-ttu-id="cd071-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="cd071-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="cd071-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="cd071-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="cd071-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="cd071-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="cd071-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="cd071-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="cd071-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd071-122">E_FAIL</span></span>|<span data-ttu-id="cd071-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="cd071-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="cd071-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="cd071-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="cd071-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="cd071-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cd071-126">备注</span><span class="sxs-lookup"><span data-stu-id="cd071-126">Remarks</span></span>  

 <span data-ttu-id="cd071-127">向 <xref:System.AppDomainManager> 宿主提供一种机制，用于启动到托管代码并控制每个代码的创建和设置 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="cd071-127">The <xref:System.AppDomainManager> provides the host with a mechanism to bootstrap into managed code and to control the creation and settings of each <xref:System.AppDomain>.</span></span> <span data-ttu-id="cd071-128"><xref:System.AppDomainManager>创建时，将加载到每个中 <xref:System.AppDomain> <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="cd071-128">The <xref:System.AppDomainManager> is loaded into each <xref:System.AppDomain> when that <xref:System.AppDomain> is created.</span></span> <span data-ttu-id="cd071-129">如果选择此选项，CLR 将通过设置参数的值，通知宿主已创建应用程序域 `pUnkAppDomainManager` 。</span><span class="sxs-lookup"><span data-stu-id="cd071-129">If it chooses, the CLR notifies the host that the application domain has been created by setting the value of the `pUnkAppDomainManager` parameter.</span></span>  
  
 <span data-ttu-id="cd071-130">在其方法的实现中 `SetAppDomainManager` ，宿主可以设置应用程序域管理器的程序集名称和类型。</span><span class="sxs-lookup"><span data-stu-id="cd071-130">In its implementation of the `SetAppDomainManager` method, the host can set the assembly name and type for the application domain manager.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd071-131">要求</span><span class="sxs-lookup"><span data-stu-id="cd071-131">Requirements</span></span>  

 <span data-ttu-id="cd071-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cd071-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd071-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="cd071-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cd071-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cd071-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cd071-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cd071-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd071-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="cd071-136">See also</span></span>

- <xref:System.AppDomain>
- <xref:System.AppDomainManager>
- [<span data-ttu-id="cd071-137">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="cd071-137">IHostControl Interface</span></span>](ihostcontrol-interface.md)
