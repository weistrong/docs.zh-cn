---
description: 了解详细信息： IHostAssemblyManager：： GetNonHostStoreAssemblies 方法
title: IHostAssemblyManager::GetNonHostStoreAssemblies 方法
ms.date: 03/30/2017
api_name:
- IHostAssemblyManager.GetNonHostStoreAssemblies
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyManager::GetNonHostStoreAssemblies
helpviewer_keywords:
- IHostAssemblyManager::GetNonHostStoreAssemblies method [.NET Framework hosting]
- GetNonHostStoreAssemblies method [.NET Framework hosting]
ms.assetid: d2250b38-c76a-40ce-80c8-ba45149886e8
topic_type:
- apiref
ms.openlocfilehash: ef551db45428b2381dfeae8f722257241a4deaf0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709043"
---
# <a name="ihostassemblymanagergetnonhoststoreassemblies-method"></a><span data-ttu-id="e7b59-103">IHostAssemblyManager::GetNonHostStoreAssemblies 方法</span><span class="sxs-lookup"><span data-stu-id="e7b59-103">IHostAssemblyManager::GetNonHostStoreAssemblies Method</span></span>

<span data-ttu-id="e7b59-104">获取一个指向 [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) 的接口指针，该指针表示宿主需要公共语言运行时 (CLR) 加载的程序集的列表。</span><span class="sxs-lookup"><span data-stu-id="e7b59-104">Gets an interface pointer to an [ICLRAssemblyReferenceList](iclrassemblyreferencelist-interface.md) that represents the list of assemblies that the host expects the common language runtime (CLR) to load.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e7b59-105">语法</span><span class="sxs-lookup"><span data-stu-id="e7b59-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNonHostStoreAssemblies (  
    [out] ICLRAssemblyReferenceList **ppReferenceList  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e7b59-106">参数</span><span class="sxs-lookup"><span data-stu-id="e7b59-106">Parameters</span></span>  

 `ppReferenceList`  
 <span data-ttu-id="e7b59-107">弄指向的地址的指针 `ICLRAssemblyReferenceList` ，该地址包含对宿主预期 CLR 加载的程序集的引用的列表。</span><span class="sxs-lookup"><span data-stu-id="e7b59-107">[out] A pointer to the address of an `ICLRAssemblyReferenceList` that contains a list of references to assemblies that the host expects the CLR to load.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e7b59-108">返回值</span><span class="sxs-lookup"><span data-stu-id="e7b59-108">Return Value</span></span>  
  
|<span data-ttu-id="e7b59-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e7b59-109">HRESULT</span></span>|<span data-ttu-id="e7b59-110">说明</span><span class="sxs-lookup"><span data-stu-id="e7b59-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e7b59-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7b59-111">S_OK</span></span>|<span data-ttu-id="e7b59-112">`GetNonHostStoreAssemblies` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="e7b59-112">`GetNonHostStoreAssemblies` returned successfully.</span></span>|  
|<span data-ttu-id="e7b59-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e7b59-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e7b59-114">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="e7b59-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="e7b59-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e7b59-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="e7b59-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="e7b59-116">The call timed out.</span></span>|  
|<span data-ttu-id="e7b59-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="e7b59-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="e7b59-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="e7b59-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="e7b59-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="e7b59-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="e7b59-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="e7b59-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="e7b59-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e7b59-121">E_FAIL</span></span>|<span data-ttu-id="e7b59-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="e7b59-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="e7b59-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="e7b59-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="e7b59-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="e7b59-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="e7b59-125">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="e7b59-125">E_OUTOFMEMORY</span></span>|<span data-ttu-id="e7b59-126">没有足够的内存可用于创建请求的引用列表 `ICLRAssemblyReferenceList` 。</span><span class="sxs-lookup"><span data-stu-id="e7b59-126">Not enough memory was available to create the list of references for the requested `ICLRAssemblyReferenceList`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e7b59-127">备注</span><span class="sxs-lookup"><span data-stu-id="e7b59-127">Remarks</span></span>  

 <span data-ttu-id="e7b59-128">CLR 使用以下一组准则来解析引用：</span><span class="sxs-lookup"><span data-stu-id="e7b59-128">The CLR resolves references using the following set of guidelines:</span></span>  
  
- <span data-ttu-id="e7b59-129">首先，它会咨询返回的程序集引用的列表 `GetNonHostStoreAssemblies` 。</span><span class="sxs-lookup"><span data-stu-id="e7b59-129">First, it consults the list of assembly references returned by `GetNonHostStoreAssemblies`.</span></span>  
  
- <span data-ttu-id="e7b59-130">如果该程序集出现在列表中，则 CLR 正常绑定到该程序集。</span><span class="sxs-lookup"><span data-stu-id="e7b59-130">If the assembly appears in the list, the CLR binds to it normally.</span></span>  
  
- <span data-ttu-id="e7b59-131">如果程序集未出现在列表中，并且宿主已提供 [IHostAssemblyStore](ihostassemblystore-interface.md)的实现，则 CLR 将调用 [IHostAssemblyStore：:P rovideassembly](ihostassemblystore-provideassembly-method.md) ，以允许主机提供要绑定到的程序集。</span><span class="sxs-lookup"><span data-stu-id="e7b59-131">If the assembly does not appear in the list and the host has provided an implementation of [IHostAssemblyStore](ihostassemblystore-interface.md), the CLR calls [IHostAssemblyStore::ProvideAssembly](ihostassemblystore-provideassembly-method.md) to allow the host to supply the assembly to bind to.</span></span>  
  
- <span data-ttu-id="e7b59-132">否则，CLR 无法绑定到程序集。</span><span class="sxs-lookup"><span data-stu-id="e7b59-132">Otherwise, the CLR fails to bind to the assembly.</span></span>  
  
 <span data-ttu-id="e7b59-133">如果主机设置 `ppReferenceList` 为 null，则 CLR 首先探测全局程序集缓存，调用 `ProvideAssembly` ，然后探测应用程序基以解析程序集引用。</span><span class="sxs-lookup"><span data-stu-id="e7b59-133">If the host sets `ppReferenceList` to null, the CLR first probes the global assembly cache, calls `ProvideAssembly`, and then probes the application base to resolve an assembly reference.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e7b59-134">初始化后，CLR 只调用 `GetNonHostStoreAssemblies` 一次。</span><span class="sxs-lookup"><span data-stu-id="e7b59-134">Upon initialization, the CLR calls `GetNonHostStoreAssemblies` only once.</span></span> <span data-ttu-id="e7b59-135">不会再次调用方法。</span><span class="sxs-lookup"><span data-stu-id="e7b59-135">The method is not called again.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e7b59-136">要求</span><span class="sxs-lookup"><span data-stu-id="e7b59-136">Requirements</span></span>  

 <span data-ttu-id="e7b59-137">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e7b59-137">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7b59-138">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="e7b59-138">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e7b59-139">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e7b59-139">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e7b59-140">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7b59-140">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7b59-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="e7b59-141">See also</span></span>

- [<span data-ttu-id="e7b59-142">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="e7b59-142">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="e7b59-143">IHostAssemblyManager 接口</span><span class="sxs-lookup"><span data-stu-id="e7b59-143">IHostAssemblyManager Interface</span></span>](ihostassemblymanager-interface.md)
- [<span data-ttu-id="e7b59-144">IHostAssemblyStore 接口</span><span class="sxs-lookup"><span data-stu-id="e7b59-144">IHostAssemblyStore Interface</span></span>](ihostassemblystore-interface.md)
