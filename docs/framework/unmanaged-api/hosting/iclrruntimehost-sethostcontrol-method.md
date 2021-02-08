---
description: 了解详细信息： ICLRRuntimeHost：： SetHostControl 方法
title: ICLRRuntimeHost::SetHostControl 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.SetHostControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::SetHostControl
helpviewer_keywords:
- SetHostControl method [.NET Framework hosting]
- ICLRRuntimeHost::SetHostControl method [.NET Framework hosting]
ms.assetid: 6136be87-e631-4756-81ed-74b66581bad4
topic_type:
- apiref
ms.openlocfilehash: e51c61666716badc7214f9a74ad11aa646f2316c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785089"
---
# <a name="iclrruntimehostsethostcontrol-method"></a><span data-ttu-id="94680-103">ICLRRuntimeHost::SetHostControl 方法</span><span class="sxs-lookup"><span data-stu-id="94680-103">ICLRRuntimeHost::SetHostControl Method</span></span>

<span data-ttu-id="94680-104">设置公共语言运行时 (CLR) 可用于获取宿主的 [IHostControl 接口](ihostcontrol-interface.md)实现的接口指针。</span><span class="sxs-lookup"><span data-stu-id="94680-104">Sets the interface pointer that the common language runtime (CLR) can use to get the host's implementation of [IHostControl Interface](ihostcontrol-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94680-105">语法</span><span class="sxs-lookup"><span data-stu-id="94680-105">Syntax</span></span>  
  
```cpp  
HRESULT SetHostControl(  
    [in] IHostControl* pHostControl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="94680-106">参数</span><span class="sxs-lookup"><span data-stu-id="94680-106">Parameters</span></span>  

 `pHostControl`  
 <span data-ttu-id="94680-107">中指向主机的 [IHostControl 接口](ihostcontrol-interface.md)实现的接口指针。</span><span class="sxs-lookup"><span data-stu-id="94680-107">[in] An interface pointer to the host's implementation of [IHostControl Interface](ihostcontrol-interface.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="94680-108">返回值</span><span class="sxs-lookup"><span data-stu-id="94680-108">Return Value</span></span>  
  
|<span data-ttu-id="94680-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="94680-109">HRESULT</span></span>|<span data-ttu-id="94680-110">说明</span><span class="sxs-lookup"><span data-stu-id="94680-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="94680-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="94680-111">S_OK</span></span>|<span data-ttu-id="94680-112">`SetHostControl` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="94680-112">`SetHostControl` returned successfully.</span></span>|  
|<span data-ttu-id="94680-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="94680-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="94680-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="94680-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="94680-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="94680-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="94680-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="94680-116">The call timed out.</span></span>|  
|<span data-ttu-id="94680-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="94680-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="94680-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="94680-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="94680-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="94680-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="94680-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="94680-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="94680-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="94680-121">E_FAIL</span></span>|<span data-ttu-id="94680-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="94680-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="94680-123">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="94680-123">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="94680-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="94680-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="94680-125">E_CLR_ALREADY_STARTED</span><span class="sxs-lookup"><span data-stu-id="94680-125">E_CLR_ALREADY_STARTED</span></span>|<span data-ttu-id="94680-126">CLR 已初始化。</span><span class="sxs-lookup"><span data-stu-id="94680-126">The CLR has already been initialized.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="94680-127">备注</span><span class="sxs-lookup"><span data-stu-id="94680-127">Remarks</span></span>  

 <span data-ttu-id="94680-128">必须在 `SetHostControl` 初始化 CLR 之前调用，也就是说，在调用 [Start 方法](iclrruntimehost-start-method.md) 或使用任何 [元数据接口](../metadata/metadata-interfaces.md)之前。</span><span class="sxs-lookup"><span data-stu-id="94680-128">You must call `SetHostControl` before the CLR is initialized, that is, before you call [Start Method](iclrruntimehost-start-method.md) or use any of the [Metadata Interfaces](../metadata/metadata-interfaces.md).</span></span> <span data-ttu-id="94680-129">建议在 `SetHostControl` 调用 [CorBindToCurrentRuntime 函数](corbindtocurrentruntime-function.md) 或 [CorBindToRuntimeEx 函数](corbindtoruntimeex-function.md)之后立即调用。</span><span class="sxs-lookup"><span data-stu-id="94680-129">It is recommended that you call `SetHostControl` immediately after calling [CorBindToCurrentRuntime Function](corbindtocurrentruntime-function.md) or [CorBindToRuntimeEx Function](corbindtoruntimeex-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="94680-130">要求</span><span class="sxs-lookup"><span data-stu-id="94680-130">Requirements</span></span>  

 <span data-ttu-id="94680-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="94680-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="94680-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="94680-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="94680-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="94680-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="94680-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="94680-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94680-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="94680-135">See also</span></span>

- [<span data-ttu-id="94680-136">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="94680-136">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)
- [<span data-ttu-id="94680-137">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="94680-137">IHostControl Interface</span></span>](ihostcontrol-interface.md)
