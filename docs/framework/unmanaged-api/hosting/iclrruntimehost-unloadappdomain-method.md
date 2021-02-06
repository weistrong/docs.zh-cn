---
description: 了解详细信息： ICLRRuntimeHost：： UnloadAppDomain 方法
title: ICLRRuntimeHost::UnloadAppDomain 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.UnloadAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::UnloadAppDomain
helpviewer_keywords:
- ICLRRuntimeHost::UnloadAppDomain method [.NET Framework hosting]
- UnloadAppDomain method [.NET Framework hosting]
ms.assetid: 571912bc-3429-4ff8-8eb2-ea993ffbd901
topic_type:
- apiref
ms.openlocfilehash: 2a47c6250434c3ee4122f8eeae75f25ee4c08a34
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637282"
---
# <a name="iclrruntimehostunloadappdomain-method"></a><span data-ttu-id="b88fa-103">ICLRRuntimeHost::UnloadAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="b88fa-103">ICLRRuntimeHost::UnloadAppDomain Method</span></span>

<span data-ttu-id="b88fa-104">卸载 <xref:System.AppDomain> 与指定数值标识符对应的托管。</span><span class="sxs-lookup"><span data-stu-id="b88fa-104">Unloads the managed <xref:System.AppDomain> that corresponds to the specified numeric identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b88fa-105">语法</span><span class="sxs-lookup"><span data-stu-id="b88fa-105">Syntax</span></span>  
  
```cpp  
HRESULT UnloadAppDomain(  
    [in] DWORD dwAppDomainId  
    [in] BOOL  fWaitUntilDone  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b88fa-106">参数</span><span class="sxs-lookup"><span data-stu-id="b88fa-106">Parameters</span></span>  

 `dwAppDomainId`  
 <span data-ttu-id="b88fa-107">中要卸载的应用程序域的数值标识符。</span><span class="sxs-lookup"><span data-stu-id="b88fa-107">[in] The numeric identifier of the application domain to unload.</span></span>  
  
 `fWaitUntilDone`  
 <span data-ttu-id="b88fa-108">[in] `true` 若要指示公共语言运行时 ( CLR) 必须等到它完成执行应用程序的当前线程，然后再尝试卸载应用程序域。</span><span class="sxs-lookup"><span data-stu-id="b88fa-108">[in] `true` to indicate that the common language runtime( CLR) must wait until it has finished executing the application's current thread before attempting to unload the application domain.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b88fa-109">返回值</span><span class="sxs-lookup"><span data-stu-id="b88fa-109">Return Value</span></span>  
  
|<span data-ttu-id="b88fa-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b88fa-110">HRESULT</span></span>|<span data-ttu-id="b88fa-111">说明</span><span class="sxs-lookup"><span data-stu-id="b88fa-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b88fa-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b88fa-112">S_OK</span></span>|<span data-ttu-id="b88fa-113">`UnloadAppDomain` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="b88fa-113">`UnloadAppDomain` returned successfully.</span></span>|  
|<span data-ttu-id="b88fa-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b88fa-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b88fa-115">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="b88fa-115">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b88fa-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b88fa-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b88fa-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="b88fa-117">The call timed out.</span></span>|  
|<span data-ttu-id="b88fa-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b88fa-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b88fa-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="b88fa-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b88fa-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b88fa-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b88fa-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="b88fa-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b88fa-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b88fa-122">E_FAIL</span></span>|<span data-ttu-id="b88fa-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="b88fa-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b88fa-124">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="b88fa-124">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b88fa-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="b88fa-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b88fa-126">备注</span><span class="sxs-lookup"><span data-stu-id="b88fa-126">Remarks</span></span>  

 <span data-ttu-id="b88fa-127">可以通过调用 [GetCurrentAppDomainId](iclrruntimehost-getcurrentappdomainid-method.md)获取当前线程正在其中执行的应用程序域的数值标识符。</span><span class="sxs-lookup"><span data-stu-id="b88fa-127">You can get the numeric identifier of the application domain in which the current thread is executing by calling [GetCurrentAppDomainId](iclrruntimehost-getcurrentappdomainid-method.md).</span></span> <span data-ttu-id="b88fa-128">此标识符与 <xref:System.AppDomain.Id%2A> 托管类型的属性相对应 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="b88fa-128">This identifier corresponds to the <xref:System.AppDomain.Id%2A> property of the managed <xref:System.AppDomain> type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b88fa-129">要求</span><span class="sxs-lookup"><span data-stu-id="b88fa-129">Requirements</span></span>  

 <span data-ttu-id="b88fa-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b88fa-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b88fa-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b88fa-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b88fa-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b88fa-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b88fa-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b88fa-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b88fa-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="b88fa-134">See also</span></span>

- [<span data-ttu-id="b88fa-135">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="b88fa-135">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)
