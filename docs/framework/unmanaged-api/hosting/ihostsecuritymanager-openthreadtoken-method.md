---
description: 了解详细信息： IHostSecurityManager：： OpenThreadToken 方法
title: IHostSecurityManager::OpenThreadToken 方法
ms.date: 03/30/2017
api_name:
- IHostSecurityManager.OpenThreadToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager::OpenThreadToken
helpviewer_keywords:
- IHostSecurityManager::OpenThreadToken method [.NET Framework hosting]
- OpenThreadToken method [.NET Framework hosting]
ms.assetid: d5999052-8bf0-4a9e-8621-da6284406b18
topic_type:
- apiref
ms.openlocfilehash: 9e0273f379f4adcf71396630b367a94c623ae15f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671550"
---
# <a name="ihostsecuritymanageropenthreadtoken-method"></a><span data-ttu-id="ce00c-103">IHostSecurityManager::OpenThreadToken 方法</span><span class="sxs-lookup"><span data-stu-id="ce00c-103">IHostSecurityManager::OpenThreadToken Method</span></span>

<span data-ttu-id="ce00c-104">打开与当前正在执行的线程关联的自由访问令牌。</span><span class="sxs-lookup"><span data-stu-id="ce00c-104">Opens the discretionary access token associated with the currently executing thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce00c-105">语法</span><span class="sxs-lookup"><span data-stu-id="ce00c-105">Syntax</span></span>  
  
```cpp  
HRESULT OpenThreadToken (  
    [in]  DWORD    dwDesiredAccess,
    [in]  BOOL     bOpenAsSelf,
    [out] HANDLE   *phThreadToken  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ce00c-106">参数</span><span class="sxs-lookup"><span data-stu-id="ce00c-106">Parameters</span></span>  

 `dwDesiredAccess`  
 <span data-ttu-id="ce00c-107">中访问值的掩码，指定请求的线程标记访问类型。</span><span class="sxs-lookup"><span data-stu-id="ce00c-107">[in] A mask of access values that specify the requested types of access to the thread token.</span></span> <span data-ttu-id="ce00c-108">这些值是在 Win32 函数中定义的 `OpenThreadToken` 。</span><span class="sxs-lookup"><span data-stu-id="ce00c-108">These values are defined in the Win32 `OpenThreadToken` function.</span></span> <span data-ttu-id="ce00c-109">请求的访问类型将与令牌的自由访问控制列表 (DACL) ，以确定要授予或拒绝的访问权限的类型。</span><span class="sxs-lookup"><span data-stu-id="ce00c-109">The requested access types are reconciled against the token's discretionary access control list (DACL) to determine which types of access to grant or deny.</span></span>  
  
 `bOpenAsSelf`  
 <span data-ttu-id="ce00c-110">[in] `true` 指定应使用调用线程的进程的安全上下文进行访问检查; `false` 若为，则指定应使用调用线程本身的安全上下文来执行访问检查。</span><span class="sxs-lookup"><span data-stu-id="ce00c-110">[in] `true` to specify that the access check should be made using the security context of the process for the calling thread; `false` to specify that the access check should be performed using the security context for the calling thread itself.</span></span> <span data-ttu-id="ce00c-111">如果线程正在模拟客户端，安全上下文可以是客户端进程的安全上下文。</span><span class="sxs-lookup"><span data-stu-id="ce00c-111">If the thread is impersonating a client, the security context can be that of a client process.</span></span>  
  
 `phThreadToken`  
 <span data-ttu-id="ce00c-112">弄指向新打开的访问令牌的指针。</span><span class="sxs-lookup"><span data-stu-id="ce00c-112">[out] A pointer to the newly opened access token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ce00c-113">返回值</span><span class="sxs-lookup"><span data-stu-id="ce00c-113">Return Value</span></span>  
  
|<span data-ttu-id="ce00c-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ce00c-114">HRESULT</span></span>|<span data-ttu-id="ce00c-115">说明</span><span class="sxs-lookup"><span data-stu-id="ce00c-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ce00c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce00c-116">S_OK</span></span>|<span data-ttu-id="ce00c-117">`OpenThreadToken` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="ce00c-117">`OpenThreadToken` returned successfully.</span></span>|  
|<span data-ttu-id="ce00c-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ce00c-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ce00c-119"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="ce00c-119">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ce00c-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ce00c-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ce00c-121">调用超时。</span><span class="sxs-lookup"><span data-stu-id="ce00c-121">The call timed out.</span></span>|  
|<span data-ttu-id="ce00c-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ce00c-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ce00c-123">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="ce00c-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ce00c-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ce00c-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ce00c-125">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="ce00c-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ce00c-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ce00c-126">E_FAIL</span></span>|<span data-ttu-id="ce00c-127">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="ce00c-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ce00c-128">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="ce00c-128">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ce00c-129">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ce00c-129">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ce00c-130">备注</span><span class="sxs-lookup"><span data-stu-id="ce00c-130">Remarks</span></span>  

 <span data-ttu-id="ce00c-131">`IHostSecurityManager::OpenThreadToken` 的行为类似于具有相同名称的对应 Win32 函数，只不过 Win32 函数允许调用方将句柄传入任意线程，同时 `IHostSecurityManager::OpenThreadToken` 仅打开与调用线程关联的标记。</span><span class="sxs-lookup"><span data-stu-id="ce00c-131">`IHostSecurityManager::OpenThreadToken` behaves similarly to the corresponding Win32 function of the same name, except that the Win32 function allows the caller to pass in a handle to an arbitrary thread, while `IHostSecurityManager::OpenThreadToken` opens only the token associated with the calling thread.</span></span>  
  
 <span data-ttu-id="ce00c-132">`HANDLE`类型不符合 COM 要求，也就是说，其大小特定于操作系统，并需要自定义封送处理。</span><span class="sxs-lookup"><span data-stu-id="ce00c-132">The `HANDLE` type is not COM-compliant, that is, its size is specific to the operating system, and it requires custom marshaling.</span></span> <span data-ttu-id="ce00c-133">因此，此令牌仅在该进程内的 CLR 和主机之间使用。</span><span class="sxs-lookup"><span data-stu-id="ce00c-133">Thus, this token is for use only within the process, between the CLR and the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ce00c-134">要求</span><span class="sxs-lookup"><span data-stu-id="ce00c-134">Requirements</span></span>  

 <span data-ttu-id="ce00c-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ce00c-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ce00c-136">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ce00c-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ce00c-137">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ce00c-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ce00c-138">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ce00c-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce00c-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="ce00c-139">See also</span></span>

- [<span data-ttu-id="ce00c-140">IHostSecurityContext 接口</span><span class="sxs-lookup"><span data-stu-id="ce00c-140">IHostSecurityContext Interface</span></span>](ihostsecuritycontext-interface.md)
- [<span data-ttu-id="ce00c-141">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="ce00c-141">IHostSecurityManager Interface</span></span>](ihostsecuritymanager-interface.md)
