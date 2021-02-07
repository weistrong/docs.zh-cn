---
description: 了解详细信息： ICLRAssemblyIdentityManager：： GetBindingIdentityFromFile 方法
title: ICLRAssemblyIdentityManager::GetBindingIdentityFromFile 方法
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.GetBindingIdentityFromFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::GetBindingIdentityFromFile
helpviewer_keywords:
- GetBindingIdentityFromFile method [.NET Framework hosting]
- ICLRAssemblyIdentityManager::GetBindingIdentifyFromFile method [.NET Framework hosting]
ms.assetid: 7797562d-7b4c-4bd9-8b93-f35e0e2869e4
topic_type:
- apiref
ms.openlocfilehash: 82e72155b38f71fe2c024994f07178638095be9a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689542"
---
# <a name="iclrassemblyidentitymanagergetbindingidentityfromfile-method"></a><span data-ttu-id="b2a0c-103">ICLRAssemblyIdentityManager::GetBindingIdentityFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="b2a0c-103">ICLRAssemblyIdentityManager::GetBindingIdentityFromFile Method</span></span>

<span data-ttu-id="b2a0c-104">获取指定文件路径处的程序集的程序集标识绑定数据。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-104">Gets the assembly identity binding data for the assembly at the specified file path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b2a0c-105">语法</span><span class="sxs-lookup"><span data-stu-id="b2a0c-105">Syntax</span></span>  
  
```cpp  
HRESULT GetBindingIdentityFromFile(  
    [in] LPCWSTR     pwzFilePath,  
    [in] DWORD       dwFlags,  
    [out, size_is(*pcchBufferSize)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b2a0c-106">参数</span><span class="sxs-lookup"><span data-stu-id="b2a0c-106">Parameters</span></span>  

 `pwzFilePath`  
 <span data-ttu-id="b2a0c-107">中要计算的文件的路径。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-107">[in] The path to the file to be evaluated.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="b2a0c-108">中指示程序集的标识类型的 [ECLRAssemblyIdentityFlags](eclrassemblyidentityflags-enumeration.md) 枚举的值。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-108">[in] A value of the [ECLRAssemblyIdentityFlags](eclrassemblyidentityflags-enumeration.md) enumeration that indicates an assembly's identity type.</span></span> <span data-ttu-id="b2a0c-109">提供用于将来的扩展性。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-109">Provided for future extensibility.</span></span> <span data-ttu-id="b2a0c-110">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT 是公共语言运行时 (CLR) 版本2.0 支持的唯一值。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-110">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT is the only value that the common language runtime (CLR) version 2.0 supports.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="b2a0c-111">弄包含不透明程序集标识数据的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-111">[out] A buffer containing the opaque assembly identity data.</span></span>  
  
 `pcchBufferSize`  
 <span data-ttu-id="b2a0c-112">[in，out]指向的大小的指针 `pwzBuffer` 。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-112">[in, out] A pointer to the size of `pwzBuffer`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b2a0c-113">返回值</span><span class="sxs-lookup"><span data-stu-id="b2a0c-113">Return Value</span></span>  
  
|<span data-ttu-id="b2a0c-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b2a0c-114">HRESULT</span></span>|<span data-ttu-id="b2a0c-115">说明</span><span class="sxs-lookup"><span data-stu-id="b2a0c-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b2a0c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2a0c-116">S_OK</span></span>|<span data-ttu-id="b2a0c-117">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-117">The method returned successfully.</span></span>|  
|<span data-ttu-id="b2a0c-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b2a0c-118">E_INVALIDARG</span></span>|<span data-ttu-id="b2a0c-119">提供的 `pwzFilePath` 为 null。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-119">The supplied `pwzFilePath` is null.</span></span>|  
|<span data-ttu-id="b2a0c-120">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="b2a0c-120">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="b2a0c-121">的大小 `pwzBuffer` 太小。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-121">The size of `pwzBuffer` is too small.</span></span>|  
|<span data-ttu-id="b2a0c-122">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b2a0c-122">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b2a0c-123">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-123">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b2a0c-124">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b2a0c-124">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b2a0c-125">调用超时。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-125">The call timed out.</span></span>|  
|<span data-ttu-id="b2a0c-126">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b2a0c-126">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b2a0c-127">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-127">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b2a0c-128">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b2a0c-128">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b2a0c-129">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-129">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b2a0c-130">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b2a0c-130">E_FAIL</span></span>|<span data-ttu-id="b2a0c-131">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-131">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b2a0c-132">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-132">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b2a0c-133">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-133">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b2a0c-134">备注</span><span class="sxs-lookup"><span data-stu-id="b2a0c-134">Remarks</span></span>  

 <span data-ttu-id="b2a0c-135">`GetBindingIdentityFromFile` 通常称为两次。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-135">`GetBindingIdentityFromFile` is typically called twice.</span></span> <span data-ttu-id="b2a0c-136">第一次调用为提供一个 null 值 `pwzBuffer` ，并且该方法将在中返回适当大小 `pcchBufferSize` 。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-136">The first call supplies a null value for `pwzBuffer`, and the method returns the appropriate size in `pcchBufferSize`.</span></span> <span data-ttu-id="b2a0c-137">第二个调用提供适当分配的缓冲区，方法在完成时返回实际的缓冲区数据。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-137">The second call supplies an appropriately allocated buffer, and the method returns with the actual buffer data upon completion.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b2a0c-138">要求</span><span class="sxs-lookup"><span data-stu-id="b2a0c-138">Requirements</span></span>  

 <span data-ttu-id="b2a0c-139">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b2a0c-139">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b2a0c-140">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b2a0c-140">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b2a0c-141">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b2a0c-141">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b2a0c-142">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b2a0c-142">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2a0c-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="b2a0c-143">See also</span></span>

- [<span data-ttu-id="b2a0c-144">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="b2a0c-144">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="b2a0c-145">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="b2a0c-145">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="b2a0c-146">ICLRHostBindingPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="b2a0c-146">ICLRHostBindingPolicyManager Interface</span></span>](iclrhostbindingpolicymanager-interface.md)
