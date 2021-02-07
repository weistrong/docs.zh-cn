---
description: 了解详细信息： IHostAssemblyManager：： GetAssemblyStore 方法
title: IHostAssemblyManager::GetAssemblyStore 方法
ms.date: 03/30/2017
api_name:
- IHostAssemblyManager.GetAssemblyStore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyManager::GetAssemblyStore
helpviewer_keywords:
- IHostAssemblyManager::GetAssemblyStore method [.NET Framework hosting]
- GetAssemblyStore method [.NET Framework hosting]
ms.assetid: d0f74593-9bb1-4a11-8096-e29734b20698
topic_type:
- apiref
ms.openlocfilehash: 5edfdc5481803ce0dd3a6f8f400b18e3f1600ea8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709108"
---
# <a name="ihostassemblymanagergetassemblystore-method"></a><span data-ttu-id="22e4d-103">IHostAssemblyManager::GetAssemblyStore 方法</span><span class="sxs-lookup"><span data-stu-id="22e4d-103">IHostAssemblyManager::GetAssemblyStore Method</span></span>

<span data-ttu-id="22e4d-104">获取一个接口指针，该指针指向表示宿主加载的程序集列表的 [IHostAssemblyStore](ihostassemblystore-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="22e4d-104">Gets an interface pointer to an [IHostAssemblyStore](ihostassemblystore-interface.md) that represents the list of assemblies loaded by the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22e4d-105">语法</span><span class="sxs-lookup"><span data-stu-id="22e4d-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAssemblyStore (  
    [out] IHostAssemblyStore **ppAssemblyStore  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="22e4d-106">参数</span><span class="sxs-lookup"><span data-stu-id="22e4d-106">Parameters</span></span>  

 `ppAssemblyStore`  
 <span data-ttu-id="22e4d-107">弄指向实例的函数指针 `IHostAssemblyStore` ，如果宿主未实现，则为 null `IHostAssemblyStore` 。</span><span class="sxs-lookup"><span data-stu-id="22e4d-107">[out] A function pointer to an `IHostAssemblyStore` instance, or null, if the host does not implement `IHostAssemblyStore`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="22e4d-108">返回值</span><span class="sxs-lookup"><span data-stu-id="22e4d-108">Return Value</span></span>  
  
|<span data-ttu-id="22e4d-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="22e4d-109">HRESULT</span></span>|<span data-ttu-id="22e4d-110">说明</span><span class="sxs-lookup"><span data-stu-id="22e4d-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="22e4d-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="22e4d-111">S_OK</span></span>|<span data-ttu-id="22e4d-112">`GetAssemblyStore` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="22e4d-112">`GetAssemblyStore` returned successfully.</span></span>|  
|<span data-ttu-id="22e4d-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="22e4d-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="22e4d-114"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="22e4d-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="22e4d-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="22e4d-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="22e4d-116">调用超时。</span><span class="sxs-lookup"><span data-stu-id="22e4d-116">The call timed out.</span></span>|  
|<span data-ttu-id="22e4d-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="22e4d-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="22e4d-118">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="22e4d-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="22e4d-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="22e4d-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="22e4d-120">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="22e4d-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="22e4d-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="22e4d-121">E_FAIL</span></span>|<span data-ttu-id="22e4d-122">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="22e4d-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="22e4d-123">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="22e4d-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="22e4d-124">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="22e4d-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="22e4d-125">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="22e4d-125">E_NOINTERFACE</span></span>|<span data-ttu-id="22e4d-126">宿主不提供的实现 `IHostAssemblyStore` 。</span><span class="sxs-lookup"><span data-stu-id="22e4d-126">The host does not provide an implementation of `IHostAssemblyStore`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="22e4d-127">备注</span><span class="sxs-lookup"><span data-stu-id="22e4d-127">Remarks</span></span>  

 <span data-ttu-id="22e4d-128">`IHostAssemblyStore` 提供允许主机独立于 CLR 绑定到程序集和模块的方法。</span><span class="sxs-lookup"><span data-stu-id="22e4d-128">`IHostAssemblyStore` provides methods that allow a host to bind to assemblies and modules independently of the CLR.</span></span> <span data-ttu-id="22e4d-129">主机通常提供程序集存储区，以允许从文件系统以外的其他格式加载程序集。</span><span class="sxs-lookup"><span data-stu-id="22e4d-129">Hosts typically provide assembly stores to allow assemblies to be loaded from formats other than the file system.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="22e4d-130">如果主机未实现，则 `IHostAssemblyStore` `GetAssemblyStore` 应将 HRESULT 值返回 E_NOINTERFACE，并将设置 `ppAssemblyStore` 为 null。</span><span class="sxs-lookup"><span data-stu-id="22e4d-130">If the host does not implement `IHostAssemblyStore`, `GetAssemblyStore` should return an HRESULT value of E_NOINTERFACE, and should set `ppAssemblyStore` to null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="22e4d-131">要求</span><span class="sxs-lookup"><span data-stu-id="22e4d-131">Requirements</span></span>  

 <span data-ttu-id="22e4d-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="22e4d-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22e4d-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="22e4d-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="22e4d-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="22e4d-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="22e4d-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22e4d-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22e4d-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="22e4d-136">See also</span></span>

- [<span data-ttu-id="22e4d-137">IHostAssemblyManager 接口</span><span class="sxs-lookup"><span data-stu-id="22e4d-137">IHostAssemblyManager Interface</span></span>](ihostassemblymanager-interface.md)
- [<span data-ttu-id="22e4d-138">IHostAssemblyStore 接口</span><span class="sxs-lookup"><span data-stu-id="22e4d-138">IHostAssemblyStore Interface</span></span>](ihostassemblystore-interface.md)
