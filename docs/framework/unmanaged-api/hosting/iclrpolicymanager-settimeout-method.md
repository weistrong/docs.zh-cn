---
description: 了解详细信息： ICLRPolicyManager：： SetTimeout 方法
title: ICLRPolicyManager::SetTimeout 方法
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager.SetTimeout
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager::SetTimeout
helpviewer_keywords:
- SetTimeout method [.NET Framework hosting]
- ICLRPolicyManager::SetTimeout method [.NET Framework hosting]
ms.assetid: 954404fd-d52d-4e68-b582-8692f3a5f608
topic_type:
- apiref
ms.openlocfilehash: 5fb65e93cc6eea7826498ff6b03147773f06e0b8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781891"
---
# <a name="iclrpolicymanagersettimeout-method"></a><span data-ttu-id="f6e04-103">ICLRPolicyManager::SetTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="f6e04-103">ICLRPolicyManager::SetTimeout Method</span></span>

<span data-ttu-id="f6e04-104">设置指定操作的超时值。</span><span class="sxs-lookup"><span data-stu-id="f6e04-104">Sets a timeout value for the specified operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6e04-105">语法</span><span class="sxs-lookup"><span data-stu-id="f6e04-105">Syntax</span></span>  
  
```cpp  
HRESULT SetTimeout (  
    [in] EClrOperation operation,  
    [in] DWORD dsMilliseconds  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f6e04-106">参数</span><span class="sxs-lookup"><span data-stu-id="f6e04-106">Parameters</span></span>  

 `operation`  
 <span data-ttu-id="f6e04-107">中 [EClrOperation](eclroperation-enumeration.md) 值之一，指示公共语言运行时 (CLR) 操作设置超时。</span><span class="sxs-lookup"><span data-stu-id="f6e04-107">[in] One of the [EClrOperation](eclroperation-enumeration.md) values, indicating the common language runtime (CLR) operation for which to set a timeout.</span></span> <span data-ttu-id="f6e04-108">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="f6e04-108">The following values are supported:</span></span>  
  
- <span data-ttu-id="f6e04-109">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="f6e04-109">OPR_AppDomainUnload</span></span>  
  
- <span data-ttu-id="f6e04-110">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="f6e04-110">OPR_ProcessExit</span></span>  
  
- <span data-ttu-id="f6e04-111">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="f6e04-111">OPR_ThreadRudeAbortInCriticalRegion</span></span>  
  
- <span data-ttu-id="f6e04-112">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="f6e04-112">OPR_ThreadRudeAbortInNonCriticalRegion</span></span>  
  
 `dwMilliseconds`  
 <span data-ttu-id="f6e04-113">中新的超时值（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="f6e04-113">[in] The new timeout value, in milliseconds.</span></span> <span data-ttu-id="f6e04-114">如果值为 "无限"，则操作永远不会超时。</span><span class="sxs-lookup"><span data-stu-id="f6e04-114">A value of INFINITE causes the operation never to time out.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f6e04-115">返回值</span><span class="sxs-lookup"><span data-stu-id="f6e04-115">Return Value</span></span>  
  
|<span data-ttu-id="f6e04-116">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f6e04-116">HRESULT</span></span>|<span data-ttu-id="f6e04-117">说明</span><span class="sxs-lookup"><span data-stu-id="f6e04-117">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f6e04-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6e04-118">S_OK</span></span>|<span data-ttu-id="f6e04-119">`SetTimeout` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="f6e04-119">`SetTimeout` returned successfully.</span></span>|  
|<span data-ttu-id="f6e04-120">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f6e04-120">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f6e04-121">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="f6e04-121">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f6e04-122">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f6e04-122">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f6e04-123">调用超时。</span><span class="sxs-lookup"><span data-stu-id="f6e04-123">The call timed out.</span></span>|  
|<span data-ttu-id="f6e04-124">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f6e04-124">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f6e04-125">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="f6e04-125">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f6e04-126">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f6e04-126">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f6e04-127">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="f6e04-127">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f6e04-128">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f6e04-128">E_FAIL</span></span>|<span data-ttu-id="f6e04-129">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="f6e04-129">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f6e04-130">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="f6e04-130">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f6e04-131">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="f6e04-131">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="f6e04-132">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f6e04-132">E_INVALIDARG</span></span>|<span data-ttu-id="f6e04-133">无法为指定的设置超时 `operation` ，或者为提供的值无效 `operation` 。</span><span class="sxs-lookup"><span data-stu-id="f6e04-133">A timeout cannot be set for the specified `operation`, or an invalid value was supplied for `operation`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f6e04-134">要求</span><span class="sxs-lookup"><span data-stu-id="f6e04-134">Requirements</span></span>  

 <span data-ttu-id="f6e04-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f6e04-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6e04-136">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f6e04-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f6e04-137">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f6e04-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f6e04-138">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6e04-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6e04-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="f6e04-139">See also</span></span>

- [<span data-ttu-id="f6e04-140">EClrOperation 枚举</span><span class="sxs-lookup"><span data-stu-id="f6e04-140">EClrOperation Enumeration</span></span>](eclroperation-enumeration.md)
- [<span data-ttu-id="f6e04-141">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="f6e04-141">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="f6e04-142">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="f6e04-142">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
