---
description: 了解详细信息： ICLRDebugManager：： IsDebuggerAttached 方法
title: ICLRDebugManager::IsDebuggerAttached 方法
ms.date: 03/30/2017
api_name:
- ICLRDebugManager.IsDebuggerAttached
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDebugManager::IsDebuggerAttached
helpviewer_keywords:
- IsDebuggerAttached method, ICLRDebugManager interface [.NET Framework hosting]
- ICLRDebugManager::IsDebuggerAttached method [.NET Framework hosting]
ms.assetid: 2f105fe0-f52d-49c5-bda5-583fb27e3aa6
topic_type:
- apiref
ms.openlocfilehash: 74305989797bcb553feb727a133e24bd308ac715
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772128"
---
# <a name="iclrdebugmanagerisdebuggerattached-method"></a><span data-ttu-id="c2285-103">ICLRDebugManager::IsDebuggerAttached 方法</span><span class="sxs-lookup"><span data-stu-id="c2285-103">ICLRDebugManager::IsDebuggerAttached Method</span></span>

<span data-ttu-id="c2285-104">获取一个值，它指示调试器是否已附加到进程。</span><span class="sxs-lookup"><span data-stu-id="c2285-104">Gets a value that indicates whether a debugger is attached to the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2285-105">语法</span><span class="sxs-lookup"><span data-stu-id="c2285-105">Syntax</span></span>  
  
```cpp  
HRESULT IsDebuggerAttached (  
    [out] BOOL *pbAttached  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c2285-106">参数</span><span class="sxs-lookup"><span data-stu-id="c2285-106">Parameters</span></span>  

 `pbAttached`  
 <span data-ttu-id="c2285-107">[out] `true` 如果调试器附加到进程，则为; 否则为。否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="c2285-107">[out] `true` if a debugger is attached to the process; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c2285-108">返回值</span><span class="sxs-lookup"><span data-stu-id="c2285-108">Return Value</span></span>  
  
|<span data-ttu-id="c2285-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c2285-109">HRESULT</span></span>|<span data-ttu-id="c2285-110">说明</span><span class="sxs-lookup"><span data-stu-id="c2285-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c2285-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2285-111">S_OK</span></span>|<span data-ttu-id="c2285-112">`IsDebuggerAttached` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="c2285-112">`IsDebuggerAttached` returned successfully.</span></span>|  
|<span data-ttu-id="c2285-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c2285-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c2285-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="c2285-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="c2285-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c2285-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="c2285-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="c2285-116">The call timed out.</span></span>|  
|<span data-ttu-id="c2285-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="c2285-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="c2285-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="c2285-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="c2285-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="c2285-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="c2285-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="c2285-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="c2285-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c2285-121">E_FAIL</span></span>|<span data-ttu-id="c2285-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="c2285-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="c2285-123">方法返回 E_FAIL 后，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="c2285-123">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="c2285-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="c2285-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c2285-125">备注</span><span class="sxs-lookup"><span data-stu-id="c2285-125">Remarks</span></span>  

 <span data-ttu-id="c2285-126">`IsDebuggerAttached` 允许宿主查询 CLR 以确定调试器是否已附加到进程。</span><span class="sxs-lookup"><span data-stu-id="c2285-126">`IsDebuggerAttached` allows the host to query the CLR to determine whether a debugger is attached to the process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c2285-127">要求</span><span class="sxs-lookup"><span data-stu-id="c2285-127">Requirements</span></span>  

 <span data-ttu-id="c2285-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c2285-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c2285-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c2285-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c2285-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c2285-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c2285-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c2285-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2285-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="c2285-132">See also</span></span>

- [<span data-ttu-id="c2285-133">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="c2285-133">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="c2285-134">ICLRDebugManager 接口</span><span class="sxs-lookup"><span data-stu-id="c2285-134">ICLRDebugManager Interface</span></span>](iclrdebugmanager-interface.md)
- [<span data-ttu-id="c2285-135">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="c2285-135">IHostControl Interface</span></span>](ihostcontrol-interface.md)
