---
description: 了解详细信息： ICLRAssemblyIdentityManager：： GetReferencedAssembliesFromFile 方法
title: ICLRAssemblyIdentityManager::GetReferencedAssembliesFromFile 方法
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.GetReferencedAssembliesFromFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::GetReferencedAssembliesFromFile
helpviewer_keywords:
- ICLRAssemblyIdentityManager::GetReferenceAssembliesFromFile method [.NET Framework hosting]
- GetReferenceAssembliesFromFile method [.NET Framework hosting]
ms.assetid: eed63d31-d977-4c7d-9443-f9d37a2a7d81
topic_type:
- apiref
ms.openlocfilehash: 46b2f392746c6e23e2a8a11aded5eacd8f5a597b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790045"
---
# <a name="iclrassemblyidentitymanagergetreferencedassembliesfromfile-method"></a><span data-ttu-id="6a5d0-103">ICLRAssemblyIdentityManager::GetReferencedAssembliesFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="6a5d0-103">ICLRAssemblyIdentityManager::GetReferencedAssembliesFromFile Method</span></span>

<span data-ttu-id="6a5d0-104">获取一个 [ICLRReferenceAssemblyEnum](iclrreferenceassemblyenum-interface.md) 实例，该实例包含程序集在指定文件路径处引用的程序集的列表。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-104">Gets an [ICLRReferenceAssemblyEnum](iclrreferenceassemblyenum-interface.md) instance that contains a list of assemblies referenced by the assembly at the specified file path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a5d0-105">语法</span><span class="sxs-lookup"><span data-stu-id="6a5d0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetReferencedAssembliesFromFile (  
    [in]  LPCWSTR pwzFilePath,  
    [in]  DWORD   dwFlags,  
    [in]  ICLRAssemblyReferenceList   *pExcludeAssembliesList,  
    [out] ICLRReferenceAssemblyEnum  **ppReferenceEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6a5d0-106">参数</span><span class="sxs-lookup"><span data-stu-id="6a5d0-106">Parameters</span></span>  

 `pwzFilePath`  
 <span data-ttu-id="6a5d0-107">中要计算的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-107">[in] The path to the assembly to be evaluated.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="6a5d0-108">中提供用于将来的扩展性。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-108">[in] Provided for future extensibility.</span></span> <span data-ttu-id="6a5d0-109">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT 是公共语言运行时的当前版本 (CLR) 支持的唯一值。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-109">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT is the only value that the current version of the common language runtime (CLR) supports.</span></span>  
  
 `pExcludeAssembliesList`  
 <span data-ttu-id="6a5d0-110">中指向 [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) 对象的指针，该对象表示应从中排除的程序集 `ppReferenceEnum` 。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-110">[in] A pointer to an [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) object that represents assemblies that should be excluded from `ppReferenceEnum`.</span></span>  
  
 `ppReferenceEnum`  
 <span data-ttu-id="6a5d0-111">弄指向对象地址的指针 `ICLRReferenceAssemblyEnum` ，该对象包含程序集引用的程序集的程序集标识数据，不包括由表示的程序集 `pwzFilePath` `pExcludeAssembliesList` 。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-111">[out] A pointer to the address of an `ICLRReferenceAssemblyEnum` object that contains assembly identity data for the assemblies referenced by the assembly at `pwzFilePath`, excluding the assemblies represented by `pExcludeAssembliesList`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6a5d0-112">返回值</span><span class="sxs-lookup"><span data-stu-id="6a5d0-112">Return Value</span></span>  
  
|<span data-ttu-id="6a5d0-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6a5d0-113">HRESULT</span></span>|<span data-ttu-id="6a5d0-114">说明</span><span class="sxs-lookup"><span data-stu-id="6a5d0-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6a5d0-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a5d0-115">S_OK</span></span>|<span data-ttu-id="6a5d0-116">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-116">The method returned successfully.</span></span>|  
|<span data-ttu-id="6a5d0-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="6a5d0-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="6a5d0-118">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-118">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="6a5d0-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6a5d0-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="6a5d0-120">调用超时。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-120">The call timed out.</span></span>|  
|<span data-ttu-id="6a5d0-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="6a5d0-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="6a5d0-122">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="6a5d0-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="6a5d0-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="6a5d0-124">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="6a5d0-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="6a5d0-125">E_FAIL</span></span>|<span data-ttu-id="6a5d0-126">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="6a5d0-127">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-127">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="6a5d0-128">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6a5d0-129">备注</span><span class="sxs-lookup"><span data-stu-id="6a5d0-129">Remarks</span></span>  

 <span data-ttu-id="6a5d0-130">调用方可以选择从返回的列表中排除一组已知的程序集引用。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-130">The caller can choose to exclude a set of known assembly references from the returned list.</span></span> <span data-ttu-id="6a5d0-131">此集由 `pExcludeAssembliesList` 参数定义。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-131">This set is defined by the `pExcludeAssembliesList` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6a5d0-132">要求</span><span class="sxs-lookup"><span data-stu-id="6a5d0-132">Requirements</span></span>  

 <span data-ttu-id="6a5d0-133">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6a5d0-133">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6a5d0-134">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="6a5d0-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6a5d0-135">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6a5d0-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6a5d0-136">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6a5d0-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a5d0-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="6a5d0-137">See also</span></span>

- [<span data-ttu-id="6a5d0-138">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="6a5d0-138">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="6a5d0-139">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="6a5d0-139">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="6a5d0-140">ICLRReferenceAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="6a5d0-140">ICLRReferenceAssemblyEnum Interface</span></span>](iclrreferenceassemblyenum-interface.md)
