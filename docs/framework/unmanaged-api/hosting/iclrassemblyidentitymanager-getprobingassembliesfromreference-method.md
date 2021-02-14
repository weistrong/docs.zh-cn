---
description: 了解详细信息： ICLRAssemblyIdentityManager：： GetProbingAssembliesFromReference 方法
title: ICLRAssemblyIdentityManager::GetProbingAssembliesFromReference 方法
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.GetProbingAssembliesFromReference
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::GetProbingAssembliesFromReference
helpviewer_keywords:
- ICLRAssemblyIdentityManager::GetProbingAssembliesFromReference method [.NET Framework hosting]
- GetProbingAssembliesFromReference method [.NET Framework hosting]
ms.assetid: aec05744-e8d4-44c6-b4a8-e583229ac34e
topic_type:
- apiref
ms.openlocfilehash: 38fcea460537ebed0e54103b460a48c2e58d8173
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100431420"
---
# <a name="iclrassemblyidentitymanagergetprobingassembliesfromreference-method"></a><span data-ttu-id="5d2c8-103">ICLRAssemblyIdentityManager::GetProbingAssembliesFromReference 方法</span><span class="sxs-lookup"><span data-stu-id="5d2c8-103">ICLRAssemblyIdentityManager::GetProbingAssembliesFromReference Method</span></span>

<span data-ttu-id="5d2c8-104">获取具有指定标识类型的程序集所引用的程序集标识的 [ICLRProbingAssemblyEnum](iclrprobingassemblyenum-interface.md) 枚举器。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-104">Gets an [ICLRProbingAssemblyEnum](iclrprobingassemblyenum-interface.md) enumerator for the assembly identities referenced by the assembly with the specified identity type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5d2c8-105">语法</span><span class="sxs-lookup"><span data-stu-id="5d2c8-105">Syntax</span></span>  
  
```cpp  
HRESULT GetProbingAssembliesFromReference (  
    [in] DWORD   dwMachineType,  
    [in] DWORD   dwFlags,  
    [in] LPCWSTR pwzReferenceIdentity,  
    [out] ICLRProbingAssemblyEnum **ppProbingAssemblyEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5d2c8-106">parameters</span><span class="sxs-lookup"><span data-stu-id="5d2c8-106">Parameters</span></span>  

 `dwMachineType`  
 <span data-ttu-id="5d2c8-107">中一个有效的值，该值指定处理器体系结构（如 WinNT 中所定义）。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-107">[in] A valid value that specifies the processor architecture, as defined in WinNT.h.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="5d2c8-108">中提供用于将来的扩展性。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-108">[in] Provided for future extensibility.</span></span> <span data-ttu-id="5d2c8-109">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT 是公共语言运行时的当前版本 (CLR) 支持的唯一值。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-109">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT is the only value that the current version of the common language runtime (CLR) supports.</span></span>  
  
 `pwzReferenceIdentity`  
 <span data-ttu-id="5d2c8-110">中不透明的程序集绑定标识，通常是从对 [ICLRAssemblyIdentityManager：： GetBindingIdentityFromFile](iclrassemblyidentitymanager-getbindingidentityfromfile-method.md) 或 [ICLRAssemblyIdentityManager：： GetBindingIdentityFromStream](iclrassemblyidentitymanager-getbindingidentityfromstream-method.md) 方法的调用返回的。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-110">[in] An opaque assembly binding identity, typically returned from a call to the [ICLRAssemblyIdentityManager::GetBindingIdentityFromFile](iclrassemblyidentitymanager-getbindingidentityfromfile-method.md) or [ICLRAssemblyIdentityManager::GetBindingIdentityFromStream](iclrassemblyidentitymanager-getbindingidentityfromstream-method.md) method.</span></span>  
  
 `ppProbingAssemblyEnum`  
 <span data-ttu-id="5d2c8-111">弄一个指向 `ICLRProbingAssemblyEnum` 枚举数的接口指针，该枚举数包含对由标识的程序集所引用的程序集的引用 `pwzReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-111">[out] An interface pointer to an `ICLRProbingAssemblyEnum` enumerator that contains references to the assemblies referenced by the assembly identified by `pwzReferenceIdentity`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5d2c8-112">返回值</span><span class="sxs-lookup"><span data-stu-id="5d2c8-112">Return Value</span></span>  
  
|<span data-ttu-id="5d2c8-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="5d2c8-113">HRESULT</span></span>|<span data-ttu-id="5d2c8-114">说明</span><span class="sxs-lookup"><span data-stu-id="5d2c8-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5d2c8-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="5d2c8-115">S_OK</span></span>|<span data-ttu-id="5d2c8-116">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-116">The method returned successfully.</span></span>|  
|<span data-ttu-id="5d2c8-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="5d2c8-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="5d2c8-118">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-118">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="5d2c8-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="5d2c8-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="5d2c8-120">调用超时。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-120">The call timed out.</span></span>|  
|<span data-ttu-id="5d2c8-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="5d2c8-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="5d2c8-122">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="5d2c8-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="5d2c8-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="5d2c8-124">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="5d2c8-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="5d2c8-125">E_FAIL</span></span>|<span data-ttu-id="5d2c8-126">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="5d2c8-127">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-127">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="5d2c8-128">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5d2c8-129">要求</span><span class="sxs-lookup"><span data-stu-id="5d2c8-129">Requirements</span></span>  

 <span data-ttu-id="5d2c8-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5d2c8-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5d2c8-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5d2c8-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5d2c8-132">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5d2c8-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5d2c8-133">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5d2c8-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d2c8-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="5d2c8-134">See also</span></span>

- [<span data-ttu-id="5d2c8-135">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="5d2c8-135">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="5d2c8-136">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="5d2c8-136">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="5d2c8-137">ICLRProbingAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="5d2c8-137">ICLRProbingAssemblyEnum Interface</span></span>](iclrprobingassemblyenum-interface.md)
