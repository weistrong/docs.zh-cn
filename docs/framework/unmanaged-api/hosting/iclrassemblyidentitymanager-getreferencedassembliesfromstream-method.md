---
description: 了解详细信息： ICLRAssemblyIdentityManager：： GetReferencedAssembliesFromStream 方法
title: ICLRAssemblyIdentityManager::GetReferencedAssembliesFromStream 方法
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.GetReferencedAssembliesFromStream
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::GetReferencedAssembliesFromStream
helpviewer_keywords:
- ICLRAssemblyIdentityManager::GetReferencedAssembliesFromStream method [.NET Framework hosting]
- GetReferencedAssembliesFromStream method [.NET Framework hosting]
ms.assetid: fe9849c1-c3fc-477b-a31f-e8619f5516f5
topic_type:
- apiref
ms.openlocfilehash: 9173587125e7b528e203dcb7e6a19d3e3f2fb990
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746082"
---
# <a name="iclrassemblyidentitymanagergetreferencedassembliesfromstream-method"></a><span data-ttu-id="1cdec-103">ICLRAssemblyIdentityManager::GetReferencedAssembliesFromStream 方法</span><span class="sxs-lookup"><span data-stu-id="1cdec-103">ICLRAssemblyIdentityManager::GetReferencedAssembliesFromStream Method</span></span>

<span data-ttu-id="1cdec-104">获取一个指向 [ICLRReferenceAssemblyEnum](iclrreferenceassemblyenum-interface.md) 对象的指针，该对象包含指定流中的程序集所引用的程序集的程序集标识数据。</span><span class="sxs-lookup"><span data-stu-id="1cdec-104">Gets a pointer to an [ICLRReferenceAssemblyEnum](iclrreferenceassemblyenum-interface.md) object that contains assembly identity data for the assemblies referenced by the assembly in the specified stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1cdec-105">语法</span><span class="sxs-lookup"><span data-stu-id="1cdec-105">Syntax</span></span>  
  
```cpp  
HRESULT GetReferencedAssembliesFromStream (  
    [in]  IStream *pStream,  
    [in]  DWORD    dwFlags,  
    [in]  ICLRAssemblyReferenceList  *pExcludeAssembliesList,  
    [out] ICLRReferenceAssemblyEnum **ppReferenceEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1cdec-106">参数</span><span class="sxs-lookup"><span data-stu-id="1cdec-106">Parameters</span></span>  

 `pStream`  
 <span data-ttu-id="1cdec-107">中一个接口指针，指向 `IStream` 包含要计算的程序集的。</span><span class="sxs-lookup"><span data-stu-id="1cdec-107">[in] An interface pointer to an `IStream` containing the assembly to be evaluated.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="1cdec-108">中提供用于将来的扩展性。</span><span class="sxs-lookup"><span data-stu-id="1cdec-108">[in] Provided for future extensibility.</span></span> <span data-ttu-id="1cdec-109">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT 是公共语言运行时的当前版本 (CLR) 支持的唯一值。</span><span class="sxs-lookup"><span data-stu-id="1cdec-109">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT is the only value that the current version of the common language runtime (CLR) supports.</span></span>  
  
 `pExcludeAssembliesList`  
 <span data-ttu-id="1cdec-110">中指向 [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) 对象的指针，该对象包含要从中排除的程序集的程序集标识数据 `ppReferenceEnum` 。</span><span class="sxs-lookup"><span data-stu-id="1cdec-110">[in] A pointer to an [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) object that contains assembly identity data for the assemblies to be excluded from `ppReferenceEnum`.</span></span>  
  
 `ppReferenceEnum`  
 <span data-ttu-id="1cdec-111">弄指向对象地址的指针 `ICLRReferenceAssemblyEnum` ，该对象包含中程序集引用的程序集的程序集标识数据 `pStream` ，不包括中的程序集 `pExcludeAssembliesList` 。</span><span class="sxs-lookup"><span data-stu-id="1cdec-111">[out] A pointer to the address of an `ICLRReferenceAssemblyEnum` object that contains assembly identity data for the assemblies referenced by the assembly in `pStream`, excluding the assemblies in `pExcludeAssembliesList`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1cdec-112">返回值</span><span class="sxs-lookup"><span data-stu-id="1cdec-112">Return Value</span></span>  
  
|<span data-ttu-id="1cdec-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1cdec-113">HRESULT</span></span>|<span data-ttu-id="1cdec-114">说明</span><span class="sxs-lookup"><span data-stu-id="1cdec-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1cdec-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cdec-115">S_OK</span></span>|<span data-ttu-id="1cdec-116">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="1cdec-116">The method returned successfully.</span></span>|  
|<span data-ttu-id="1cdec-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="1cdec-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="1cdec-118">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="1cdec-118">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="1cdec-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1cdec-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="1cdec-120">调用超时。</span><span class="sxs-lookup"><span data-stu-id="1cdec-120">The call timed out.</span></span>|  
|<span data-ttu-id="1cdec-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="1cdec-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="1cdec-122">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="1cdec-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="1cdec-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="1cdec-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="1cdec-124">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="1cdec-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="1cdec-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="1cdec-125">E_FAIL</span></span>|<span data-ttu-id="1cdec-126">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="1cdec-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="1cdec-127">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="1cdec-127">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="1cdec-128">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="1cdec-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1cdec-129">备注</span><span class="sxs-lookup"><span data-stu-id="1cdec-129">Remarks</span></span>  

 <span data-ttu-id="1cdec-130">调用方可以选择从返回的列表中排除一组已知的程序集引用。</span><span class="sxs-lookup"><span data-stu-id="1cdec-130">The caller can choose to exclude a set of known assembly references from the returned list.</span></span> <span data-ttu-id="1cdec-131">此集由定义 `pExcludeAssembliesList` 。</span><span class="sxs-lookup"><span data-stu-id="1cdec-131">This set is defined by `pExcludeAssembliesList`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1cdec-132">要求</span><span class="sxs-lookup"><span data-stu-id="1cdec-132">Requirements</span></span>  

 <span data-ttu-id="1cdec-133">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1cdec-133">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1cdec-134">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="1cdec-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1cdec-135">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1cdec-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1cdec-136">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1cdec-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1cdec-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="1cdec-137">See also</span></span>

- [<span data-ttu-id="1cdec-138">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="1cdec-138">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="1cdec-139">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="1cdec-139">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="1cdec-140">ICLRReferenceAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="1cdec-140">ICLRReferenceAssemblyEnum Interface</span></span>](iclrreferenceassemblyenum-interface.md)
