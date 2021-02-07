---
description: 了解详细信息： IHostMemoryManager：： CreateMAlloc 方法
title: IHostMemoryManager::CreateMAlloc 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.CreateMAlloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::CreateMAlloc
helpviewer_keywords:
- CreateAlloc method [.NET Framework hosting]
- IHostMemoryManager::CreateMAlloc method [.NET Framework hosting]
ms.assetid: 9ee6e052-bef7-4350-9e4f-edfffd99ad6f
topic_type:
- apiref
ms.openlocfilehash: de73490a5c8b4e1672beb4750bcc617c2371f07b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707879"
---
# <a name="ihostmemorymanagercreatemalloc-method"></a><span data-ttu-id="1fe4b-103">IHostMemoryManager::CreateMAlloc 方法</span><span class="sxs-lookup"><span data-stu-id="1fe4b-103">IHostMemoryManager::CreateMAlloc Method</span></span>

<span data-ttu-id="1fe4b-104">获取一个接口指针，该指针指向用于从主机创建的堆发出分配请求的 [IHostMAlloc](ihostmalloc-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-104">Gets an interface pointer to an [IHostMAlloc](ihostmalloc-interface.md) instance that is used to make allocation requests from a heap created by the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1fe4b-105">语法</span><span class="sxs-lookup"><span data-stu-id="1fe4b-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateMalloc (  
    [in]  DWORD         dwMallocType,  
    [out] IHostMalloc **ppMalloc  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1fe4b-106">参数</span><span class="sxs-lookup"><span data-stu-id="1fe4b-106">Parameters</span></span>  

 `dwMallocType`  
 <span data-ttu-id="1fe4b-107">中 [MALLOC_TYPE](malloc-type-enumeration.md) 标志的组合，这些标志指定正在分配的内存的特征。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-107">[in] A combination of [MALLOC_TYPE](malloc-type-enumeration.md) flags that specifies the characteristics of the memory that is being allocated.</span></span>  
  
 `ppMAlloc`  
 <span data-ttu-id="1fe4b-108">弄指向主机提供的实例的地址的指针 `IHostMAlloc` 。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-108">[out] A pointer to the address of an `IHostMAlloc` instance provided by the host.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1fe4b-109">返回值</span><span class="sxs-lookup"><span data-stu-id="1fe4b-109">Return Value</span></span>  
  
|<span data-ttu-id="1fe4b-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1fe4b-110">HRESULT</span></span>|<span data-ttu-id="1fe4b-111">说明</span><span class="sxs-lookup"><span data-stu-id="1fe4b-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1fe4b-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="1fe4b-112">S_OK</span></span>|<span data-ttu-id="1fe4b-113">`CreateMAlloc` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-113">`CreateMAlloc` returned successfully.</span></span>|  
|<span data-ttu-id="1fe4b-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="1fe4b-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="1fe4b-115"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="1fe4b-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1fe4b-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="1fe4b-117">调用超时。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-117">The call timed out.</span></span>|  
|<span data-ttu-id="1fe4b-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="1fe4b-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="1fe4b-119">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="1fe4b-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="1fe4b-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="1fe4b-121">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="1fe4b-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="1fe4b-122">E_FAIL</span></span>|<span data-ttu-id="1fe4b-123">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="1fe4b-124">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="1fe4b-125">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="1fe4b-126">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="1fe4b-126">E_OUTOFMEMORY</span></span>|<span data-ttu-id="1fe4b-127">没有足够的物理内存可用于完成分配请求。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-127">Not enough physical memory was available to complete the allocation request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1fe4b-128">备注</span><span class="sxs-lookup"><span data-stu-id="1fe4b-128">Remarks</span></span>  

 <span data-ttu-id="1fe4b-129">`CreateMAlloc` 返回一个对象，该对象允许 CLR 通过主机发出分配请求，而不是使用标准的 Win32 函数。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-129">`CreateMAlloc` returns an object that allows the CLR to make allocation requests through the host instead of using the standard Win32 functions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1fe4b-130">要求</span><span class="sxs-lookup"><span data-stu-id="1fe4b-130">Requirements</span></span>  

 <span data-ttu-id="1fe4b-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1fe4b-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1fe4b-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="1fe4b-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1fe4b-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1fe4b-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1fe4b-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1fe4b-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fe4b-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="1fe4b-135">See also</span></span>

- [<span data-ttu-id="1fe4b-136">IHostMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="1fe4b-136">IHostMalloc Interface</span></span>](ihostmalloc-interface.md)
- [<span data-ttu-id="1fe4b-137">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="1fe4b-137">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
