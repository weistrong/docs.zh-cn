---
description: 了解详细信息： ICLRRuntimeHost：： ExecuteInDefaultAppDomain 方法
title: ICLRRuntimeHost::ExecuteInDefaultAppDomain 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.ExecuteInDefaultAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::ExecuteInDefaultAppDomain
helpviewer_keywords:
- ICLRRuntimeHost::ExecuteInDefaultAppDomain method [.NET Framework hosting]
- ExecuteInDefaultAppDomain method [.NET Framework hosting]
ms.assetid: 30b5cf9a-a762-4bd4-be12-d6c1442b78b1
topic_type:
- apiref
ms.openlocfilehash: 0fae9be69cf67da252dcdb423432ec922c0b00ac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785103"
---
# <a name="iclrruntimehostexecuteindefaultappdomain-method"></a><span data-ttu-id="761a9-103">ICLRRuntimeHost::ExecuteInDefaultAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="761a9-103">ICLRRuntimeHost::ExecuteInDefaultAppDomain Method</span></span>

<span data-ttu-id="761a9-104">在指定的托管程序集中调用指定类型的指定方法。</span><span class="sxs-lookup"><span data-stu-id="761a9-104">Calls the specified method of the specified type in the specified managed assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="761a9-105">语法</span><span class="sxs-lookup"><span data-stu-id="761a9-105">Syntax</span></span>  
  
```cpp  
HRESULT ExecuteInDefaultAppDomain (  
    [in] LPCWSTR pwzAssemblyPath,  
    [in] LPCWSTR pwzTypeName,
    [in] LPCWSTR pwzMethodName,  
    [in] LPCWSTR pwzArgument,  
    [out] DWORD *pReturnValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="761a9-106">参数</span><span class="sxs-lookup"><span data-stu-id="761a9-106">Parameters</span></span>  

 `pwzAssemblyPath`  
 <span data-ttu-id="761a9-107">中的路径，该路径 <xref:System.Reflection.Assembly> 定义 <xref:System.Type> 要调用其方法的。</span><span class="sxs-lookup"><span data-stu-id="761a9-107">[in] The path to the <xref:System.Reflection.Assembly> that defines the <xref:System.Type> whose method is to be invoked.</span></span>  
  
 `pwzTypeName`  
 <span data-ttu-id="761a9-108">中 <xref:System.Type> 定义要调用的方法的的名称。</span><span class="sxs-lookup"><span data-stu-id="761a9-108">[in] The name of the <xref:System.Type> that defines the method to invoke.</span></span>  
  
 `pwzMethodName`  
 <span data-ttu-id="761a9-109">中要调用的方法的名称。</span><span class="sxs-lookup"><span data-stu-id="761a9-109">[in] The name of the method to invoke.</span></span>  
  
 `pwzArgument`  
 <span data-ttu-id="761a9-110">中要传递给方法的字符串参数。</span><span class="sxs-lookup"><span data-stu-id="761a9-110">[in] The string parameter to pass to the method.</span></span>  
  
 `pReturnValue`  
 <span data-ttu-id="761a9-111">弄被调用方法返回的整数值。</span><span class="sxs-lookup"><span data-stu-id="761a9-111">[out] The integer value returned by the invoked method.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="761a9-112">返回值</span><span class="sxs-lookup"><span data-stu-id="761a9-112">Return Value</span></span>  
  
|<span data-ttu-id="761a9-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="761a9-113">HRESULT</span></span>|<span data-ttu-id="761a9-114">说明</span><span class="sxs-lookup"><span data-stu-id="761a9-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="761a9-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="761a9-115">S_OK</span></span>|<span data-ttu-id="761a9-116">`ExecuteInDefaultAppDomain` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="761a9-116">`ExecuteInDefaultAppDomain` returned successfully.</span></span>|  
|<span data-ttu-id="761a9-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="761a9-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="761a9-118"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="761a9-118">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="761a9-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="761a9-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="761a9-120">调用超时。</span><span class="sxs-lookup"><span data-stu-id="761a9-120">The call timed out.</span></span>|  
|<span data-ttu-id="761a9-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="761a9-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="761a9-122">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="761a9-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="761a9-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="761a9-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="761a9-124">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="761a9-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="761a9-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="761a9-125">E_FAIL</span></span>|<span data-ttu-id="761a9-126">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="761a9-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="761a9-127">如果某个方法返回 E_FAIL，则该 CRL 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="761a9-127">If a method returns E_FAIL, the CRL is no longer usable within the process.</span></span> <span data-ttu-id="761a9-128">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="761a9-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="761a9-129">备注</span><span class="sxs-lookup"><span data-stu-id="761a9-129">Remarks</span></span>  

 <span data-ttu-id="761a9-130">调用的方法必须具有以下签名：</span><span class="sxs-lookup"><span data-stu-id="761a9-130">The invoked method must have the following signature:</span></span>  
  
```cpp  
static int pwzMethodName (String pwzArgument)  
```  
  
 <span data-ttu-id="761a9-131">其中 `pwzMethodName` ，表示被调用方法的名称， `pwzArgument` 表示作为参数传递给该方法的字符串值。</span><span class="sxs-lookup"><span data-stu-id="761a9-131">where `pwzMethodName` represents the name of the invoked method, and `pwzArgument` represents the string value passed as a parameter to that method.</span></span> <span data-ttu-id="761a9-132">如果 HRESULT 值设置为 S_OK，则将 `pReturnValue` 设置为被调用方法返回的整数值。</span><span class="sxs-lookup"><span data-stu-id="761a9-132">If the HRESULT value is set to S_OK, `pReturnValue` is set to the integer value returned by the invoked method.</span></span> <span data-ttu-id="761a9-133">否则， `pReturnValue` 则不设置。</span><span class="sxs-lookup"><span data-stu-id="761a9-133">Otherwise, `pReturnValue` is not set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="761a9-134">要求</span><span class="sxs-lookup"><span data-stu-id="761a9-134">Requirements</span></span>  

 <span data-ttu-id="761a9-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="761a9-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="761a9-136">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="761a9-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="761a9-137">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="761a9-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="761a9-138">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="761a9-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="761a9-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="761a9-139">See also</span></span>

- [<span data-ttu-id="761a9-140">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="761a9-140">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)
