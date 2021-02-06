---
description: 了解详细信息： ICLRAssemblyIdentityManager：： GetCLRAssemblyReferenceList 方法
title: ICLRAssemblyIdentityManager::GetCLRAssemblyReferenceList 方法
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.GetCLRAssemblyReferenceList
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::GetCLRAssemblyReferenceList
helpviewer_keywords:
- GetClrAssemblyReferenceList method [.NET Framework hosting]
- ICLRAssemblyIdentityManager::GetCLRAssemblyReferenceList method [.NET Framework hosting]
ms.assetid: cb5ffae5-287b-4a87-9ca8-7ce3ae0601b7
topic_type:
- apiref
ms.openlocfilehash: 91f7b9eaacee559c5e404b5dda0f8b4201f91a66
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649554"
---
# <a name="iclrassemblyidentitymanagergetclrassemblyreferencelist-method"></a><span data-ttu-id="a78e3-103">ICLRAssemblyIdentityManager::GetCLRAssemblyReferenceList 方法</span><span class="sxs-lookup"><span data-stu-id="a78e3-103">ICLRAssemblyIdentityManager::GetCLRAssemblyReferenceList Method</span></span>

<span data-ttu-id="a78e3-104">从提供的部分程序集标识列表中获取指向 [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) 实例的接口指针。</span><span class="sxs-lookup"><span data-stu-id="a78e3-104">Gets an interface pointer to an [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) instance from the supplied list of partial assembly identities.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a78e3-105">语法</span><span class="sxs-lookup"><span data-stu-id="a78e3-105">Syntax</span></span>  
  
```cpp  
HRESULT  GetCLRAssemblyReferenceList (  
    [in] LPCWSTR *ppwzAssemblyReferences,  
    [in] DWORD    dwNumOfReferences,  
    [out] ICLRAssemblyReferenceList **ppReferenceList  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a78e3-106">参数</span><span class="sxs-lookup"><span data-stu-id="a78e3-106">Parameters</span></span>  

 `ppwzAssemblyReferences`  
 <span data-ttu-id="a78e3-107">中以 null 结尾的字符串数组，格式为 "name，property = value ..."，它指定部分程序集标识的列表。</span><span class="sxs-lookup"><span data-stu-id="a78e3-107">[in] An array of null-terminated strings in the form "name, property=value..." that specify a list of partial assembly identities.</span></span>  
  
 `dwNumOfReferences`  
 <span data-ttu-id="a78e3-108">中中的项数 `ppwzAssemblyReferences` 。</span><span class="sxs-lookup"><span data-stu-id="a78e3-108">[in] The number of items in `ppwzAssemblyReferences`.</span></span>  
  
 `ppReferenceList`  
 <span data-ttu-id="a78e3-109">弄一个指向对象的接口指针， `ICLRAssemblyReferenceList` 该对象包含在中指定的程序集列表的程序集标识数据 `ppwzAssemblyReferences` 。</span><span class="sxs-lookup"><span data-stu-id="a78e3-109">[out] An interface pointer to an `ICLRAssemblyReferenceList` object that contains the assembly identity data for the list of assemblies specified in `ppwzAssemblyReferences`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a78e3-110">返回值</span><span class="sxs-lookup"><span data-stu-id="a78e3-110">Return Value</span></span>  
  
|<span data-ttu-id="a78e3-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a78e3-111">HRESULT</span></span>|<span data-ttu-id="a78e3-112">说明</span><span class="sxs-lookup"><span data-stu-id="a78e3-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a78e3-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a78e3-113">S_OK</span></span>|<span data-ttu-id="a78e3-114">该方法已成功返回。</span><span class="sxs-lookup"><span data-stu-id="a78e3-114">The method returned successfully.</span></span>|  
|<span data-ttu-id="a78e3-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a78e3-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a78e3-116"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="a78e3-116">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a78e3-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a78e3-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a78e3-118">调用超时。</span><span class="sxs-lookup"><span data-stu-id="a78e3-118">The call timed out.</span></span>|  
|<span data-ttu-id="a78e3-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a78e3-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a78e3-120">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="a78e3-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a78e3-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a78e3-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a78e3-122">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="a78e3-122">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a78e3-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a78e3-123">E_FAIL</span></span>|<span data-ttu-id="a78e3-124">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="a78e3-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a78e3-125">如果方法返回 E_FAIL，则 CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="a78e3-125">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a78e3-126">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="a78e3-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a78e3-127">要求</span><span class="sxs-lookup"><span data-stu-id="a78e3-127">Requirements</span></span>  

 <span data-ttu-id="a78e3-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a78e3-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a78e3-129">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a78e3-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a78e3-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a78e3-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a78e3-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a78e3-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a78e3-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="a78e3-132">See also</span></span>

- [<span data-ttu-id="a78e3-133">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="a78e3-133">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="a78e3-134">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="a78e3-134">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
