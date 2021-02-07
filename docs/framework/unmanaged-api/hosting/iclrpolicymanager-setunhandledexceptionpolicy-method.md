---
description: 了解详细信息： ICLRPolicyManager：： SetUnhandledExceptionPolicy 方法
title: ICLRPolicyManager::SetUnhandledExceptionPolicy 方法
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager.SetUnhandledExceptionPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager::SetUnhandledExceptionPolicy
helpviewer_keywords:
- ICLRPolicyManager::SetUnhandledExceptionPolicy method [.NET Framework hosting]
- SetUnhandledExceptionPolicy method [.NET Framework hosting]
ms.assetid: 5268480e-280a-4931-b7a3-dc3ffdf7f78f
topic_type:
- apiref
ms.openlocfilehash: 489127bb00b2b65466460baa3cfd31439672cd1c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716531"
---
# <a name="iclrpolicymanagersetunhandledexceptionpolicy-method"></a><span data-ttu-id="8dbe0-103">ICLRPolicyManager::SetUnhandledExceptionPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="8dbe0-103">ICLRPolicyManager::SetUnhandledExceptionPolicy Method</span></span>

<span data-ttu-id="8dbe0-104">指定在发生未经处理的异常时公共语言运行时 (CLR) 的行为。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-104">Specifies the behavior of the common language runtime (CLR) when an unhandled exception occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8dbe0-105">语法</span><span class="sxs-lookup"><span data-stu-id="8dbe0-105">Syntax</span></span>  
  
```cpp  
HRESULT SetUnhandledExceptionPolicy (  
    [in] EClrUnhandledExceptionPolicy policy  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8dbe0-106">参数</span><span class="sxs-lookup"><span data-stu-id="8dbe0-106">Parameters</span></span>  

 `policy`  
 <span data-ttu-id="8dbe0-107">中 [EClrUnhandledException](eclrunhandledexception-enumeration.md) 值之一，指示行为是由 CLR 还是宿主设置。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-107">[in] One of the [EClrUnhandledException](eclrunhandledexception-enumeration.md) values, indicating whether the behavior is set by the CLR or the host.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8dbe0-108">返回值</span><span class="sxs-lookup"><span data-stu-id="8dbe0-108">Return Value</span></span>  
  
|<span data-ttu-id="8dbe0-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8dbe0-109">HRESULT</span></span>|<span data-ttu-id="8dbe0-110">说明</span><span class="sxs-lookup"><span data-stu-id="8dbe0-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8dbe0-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="8dbe0-111">S_OK</span></span>|<span data-ttu-id="8dbe0-112">`SetUnhandledExceptionPolicy` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-112">`SetUnhandledExceptionPolicy` returned successfully.</span></span>|  
|<span data-ttu-id="8dbe0-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="8dbe0-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="8dbe0-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="8dbe0-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="8dbe0-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="8dbe0-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-116">The call timed out.</span></span>|  
|<span data-ttu-id="8dbe0-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="8dbe0-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="8dbe0-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="8dbe0-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="8dbe0-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="8dbe0-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="8dbe0-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8dbe0-121">E_FAIL</span></span>|<span data-ttu-id="8dbe0-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="8dbe0-123">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-123">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="8dbe0-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8dbe0-125">备注</span><span class="sxs-lookup"><span data-stu-id="8dbe0-125">Remarks</span></span>  

 <span data-ttu-id="8dbe0-126">默认情况下，CLR 是所有未经处理的异常的最终处理程序，其默认行为是销毁进程。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-126">By default, the CLR is the final handler for all unhandled exceptions, and its default behavior is to tear down the process.</span></span> <span data-ttu-id="8dbe0-127">宿主可以通过将值设置为 eHostDeterminedPolicy 来更改此行为 `policy` 。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-127">The host can change this behavior by setting the `policy` value to eHostDeterminedPolicy.</span></span> <span data-ttu-id="8dbe0-128">与早期版本的 CLR 一样，此值允许主机实现其自己的默认行为。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-128">This value allows the host to implement its own default behavior, as with earlier versions of the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8dbe0-129">要求</span><span class="sxs-lookup"><span data-stu-id="8dbe0-129">Requirements</span></span>  

 <span data-ttu-id="8dbe0-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8dbe0-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8dbe0-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="8dbe0-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8dbe0-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8dbe0-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8dbe0-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8dbe0-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8dbe0-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="8dbe0-134">See also</span></span>

- [<span data-ttu-id="8dbe0-135">EClrUnhandledException 枚举</span><span class="sxs-lookup"><span data-stu-id="8dbe0-135">EClrUnhandledException Enumeration</span></span>](eclrunhandledexception-enumeration.md)
- [<span data-ttu-id="8dbe0-136">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="8dbe0-136">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="8dbe0-137">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="8dbe0-137">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
- [<span data-ttu-id="8dbe0-138">IHostPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="8dbe0-138">IHostPolicyManager Interface</span></span>](ihostpolicymanager-interface.md)
