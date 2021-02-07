---
description: 了解详细信息： IHostSecurityManager：： GetSecurityContext 方法
title: IHostSecurityManager::GetSecurityContext 方法
ms.date: 03/30/2017
api_name:
- IHostSecurityManager.GetSecurityContext
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager::GetSecurityContext
helpviewer_keywords:
- GetSecurityContext method [.NET Framework hosting]
- IHostSecurityManager::GetSecurityContext method [.NET Framework hosting]
ms.assetid: 958970d6-f6a2-4b84-b32a-f555cbaf8f61
topic_type:
- apiref
ms.openlocfilehash: 0dc9e0380d2fb218b68f6beb85fa1ccba8826d85
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671555"
---
# <a name="ihostsecuritymanagergetsecuritycontext-method"></a><span data-ttu-id="745a0-103">IHostSecurityManager::GetSecurityContext 方法</span><span class="sxs-lookup"><span data-stu-id="745a0-103">IHostSecurityManager::GetSecurityContext Method</span></span>

<span data-ttu-id="745a0-104">从主机获取请求的 [IHostSecurityContext](ihostsecuritycontext-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="745a0-104">Gets the requested [IHostSecurityContext](ihostsecuritycontext-interface.md) from the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="745a0-105">语法</span><span class="sxs-lookup"><span data-stu-id="745a0-105">Syntax</span></span>  
  
```cpp
HRESULT GetSecurityContext (  
    [in]  EContextType eContextType,
    [out] IHostSecurityContext** ppSecurityContext  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="745a0-106">参数</span><span class="sxs-lookup"><span data-stu-id="745a0-106">Parameters</span></span>  

 `eContextType`  
 <span data-ttu-id="745a0-107">中 [EContextType](econtexttype-enumeration.md) 值之一，指示要返回的安全上下文的类型。</span><span class="sxs-lookup"><span data-stu-id="745a0-107">[in] One of the [EContextType](econtexttype-enumeration.md) values, indicating what type of security context to return.</span></span>  
  
 `ppSecurityContext`  
 <span data-ttu-id="745a0-108">弄的接口指针的地址 `IHostSecurityContext` `eContextType` 。</span><span class="sxs-lookup"><span data-stu-id="745a0-108">[out] The address of an interface pointer to the `IHostSecurityContext` of `eContextType`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="745a0-109">返回值</span><span class="sxs-lookup"><span data-stu-id="745a0-109">Return Value</span></span>  
  
|<span data-ttu-id="745a0-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="745a0-110">HRESULT</span></span>|<span data-ttu-id="745a0-111">说明</span><span class="sxs-lookup"><span data-stu-id="745a0-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="745a0-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="745a0-112">S_OK</span></span>|<span data-ttu-id="745a0-113">`GetSecurityContext` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="745a0-113">`GetSecurityContext` returned successfully.</span></span>|  
|<span data-ttu-id="745a0-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="745a0-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="745a0-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="745a0-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="745a0-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="745a0-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="745a0-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="745a0-117">The call timed out.</span></span>|  
|<span data-ttu-id="745a0-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="745a0-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="745a0-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="745a0-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="745a0-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="745a0-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="745a0-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="745a0-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="745a0-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="745a0-122">E_FAIL</span></span>|<span data-ttu-id="745a0-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="745a0-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="745a0-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="745a0-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="745a0-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="745a0-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="745a0-126">备注</span><span class="sxs-lookup"><span data-stu-id="745a0-126">Remarks</span></span>  

 <span data-ttu-id="745a0-127">宿主可以通过 CLR 和用户代码控制对线程标记的所有代码访问。</span><span class="sxs-lookup"><span data-stu-id="745a0-127">A host can control all code access to thread tokens by both the CLR and user code.</span></span> <span data-ttu-id="745a0-128">它还可以确保在异步操作或代码点之间跨受限制的代码访问传递完整的安全上下文信息。</span><span class="sxs-lookup"><span data-stu-id="745a0-128">It can also ensure that complete security context information is passed across asynchronous operations or code points with restricted code access.</span></span> <span data-ttu-id="745a0-129">`IHostSecurityContext` 封装此安全上下文信息，这对于 CLR 是不透明的。</span><span class="sxs-lookup"><span data-stu-id="745a0-129">`IHostSecurityContext` encapsulates this security context information, which is opaque to the CLR.</span></span> <span data-ttu-id="745a0-130">CLR 捕获此信息，并在线程池辅助角色项调度、终结器执行以及模块和类构造之间移动。</span><span class="sxs-lookup"><span data-stu-id="745a0-130">The CLR captures this information and moves it across thread pool worker item dispatch, finalizer execution, and module and class construction.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="745a0-131">要求</span><span class="sxs-lookup"><span data-stu-id="745a0-131">Requirements</span></span>  

 <span data-ttu-id="745a0-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="745a0-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="745a0-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="745a0-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="745a0-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="745a0-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="745a0-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="745a0-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="745a0-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="745a0-136">See also</span></span>

- [<span data-ttu-id="745a0-137">EContextType 枚举</span><span class="sxs-lookup"><span data-stu-id="745a0-137">EContextType Enumeration</span></span>](econtexttype-enumeration.md)
- [<span data-ttu-id="745a0-138">IHostSecurityContext 接口</span><span class="sxs-lookup"><span data-stu-id="745a0-138">IHostSecurityContext Interface</span></span>](ihostsecuritycontext-interface.md)
- [<span data-ttu-id="745a0-139">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="745a0-139">IHostSecurityManager Interface</span></span>](ihostsecuritymanager-interface.md)
