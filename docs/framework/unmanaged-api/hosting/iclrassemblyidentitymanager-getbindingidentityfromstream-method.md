---
description: 了解详细信息： ICLRAssemblyIdentityManager：： GetBindingIdentityFromStream 方法
title: ICLRAssemblyIdentityManager::GetBindingIdentityFromStream 方法
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.GetBindingIdentityFromStream
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::GetBindingIdentityFromStream
helpviewer_keywords:
- GetBindingIdentityFromStream method [.NET Framework hosting]
- ICLRAssemblyIdentityManager::GetBindingIdentityFromStream method [.NET Framework hosting]
ms.assetid: 40123b30-a589-46b3-95d3-af7b2b0baa05
topic_type:
- apiref
ms.openlocfilehash: aed5968a5f5c22a2f5cbea66a350dbe452368325
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716882"
---
# <a name="iclrassemblyidentitymanagergetbindingidentityfromstream-method"></a><span data-ttu-id="0e9bd-103">ICLRAssemblyIdentityManager::GetBindingIdentityFromStream 方法</span><span class="sxs-lookup"><span data-stu-id="0e9bd-103">ICLRAssemblyIdentityManager::GetBindingIdentityFromStream Method</span></span>

<span data-ttu-id="0e9bd-104">获取指定流中的程序集的规范程序集标识数据。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-104">Gets the canonical assembly identity data for the assembly in the specified stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e9bd-105">语法</span><span class="sxs-lookup"><span data-stu-id="0e9bd-105">Syntax</span></span>  
  
```cpp  
HRESULT GetBindingIdentityFromStream (  
    [in] IStream    *pStream,  
    [in] DWORD       dwFlags,  
    [out, size_is(*pcchBufferSize)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0e9bd-106">参数</span><span class="sxs-lookup"><span data-stu-id="0e9bd-106">Parameters</span></span>  

 `pStream`  
 <span data-ttu-id="0e9bd-107">中要计算的程序集流。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-107">[in] The assembly stream to be evaluated.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="0e9bd-108">中提供用于将来的扩展性。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-108">[in] Provided for future extensibility.</span></span> <span data-ttu-id="0e9bd-109">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT 是公共语言运行时的当前版本 (CLR) 支持的唯一值。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-109">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT is the only value that the current version of the common language runtime (CLR) supports.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="0e9bd-110">弄包含不透明程序集标识数据的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-110">[out] A buffer containing the opaque assembly identity data.</span></span>  
  
 `pcchBufferSize`  
 <span data-ttu-id="0e9bd-111">[in，out]的大小 `pwzBuffer` 。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-111">[in, out] The size of `pwzBuffer`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0e9bd-112">返回值</span><span class="sxs-lookup"><span data-stu-id="0e9bd-112">Return Value</span></span>  
  
|<span data-ttu-id="0e9bd-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0e9bd-113">HRESULT</span></span>|<span data-ttu-id="0e9bd-114">说明</span><span class="sxs-lookup"><span data-stu-id="0e9bd-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0e9bd-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e9bd-115">S_OK</span></span>|<span data-ttu-id="0e9bd-116">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-116">The method returned successfully.</span></span>|  
|<span data-ttu-id="0e9bd-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0e9bd-117">E_INVALIDARG</span></span>|<span data-ttu-id="0e9bd-118">提供的 `pStream` 为 null。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-118">The supplied `pStream` is null.</span></span>|  
|<span data-ttu-id="0e9bd-119">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="0e9bd-119">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="0e9bd-120">的大小 `pwzBuffer` 太小。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-120">The size of `pwzBuffer` is too small.</span></span>|  
|<span data-ttu-id="0e9bd-121">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0e9bd-121">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="0e9bd-122">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-122">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="0e9bd-123">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0e9bd-123">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="0e9bd-124">调用超时。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-124">The call timed out.</span></span>|  
|<span data-ttu-id="0e9bd-125">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="0e9bd-125">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="0e9bd-126">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-126">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="0e9bd-127">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="0e9bd-127">HOST_E_ABANDONED</span></span>|<span data-ttu-id="0e9bd-128">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-128">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="0e9bd-129">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0e9bd-129">E_FAIL</span></span>|<span data-ttu-id="0e9bd-130">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-130">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="0e9bd-131">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-131">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="0e9bd-132">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-132">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0e9bd-133">要求</span><span class="sxs-lookup"><span data-stu-id="0e9bd-133">Requirements</span></span>  

 <span data-ttu-id="0e9bd-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0e9bd-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0e9bd-135">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="0e9bd-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0e9bd-136">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0e9bd-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0e9bd-137">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0e9bd-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e9bd-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="0e9bd-138">See also</span></span>

- [<span data-ttu-id="0e9bd-139">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="0e9bd-139">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="0e9bd-140">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="0e9bd-140">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
