---
description: 了解详细信息： IHostMAlloc：：分配方法
title: IHostMAlloc::Alloc 方法
ms.date: 03/30/2017
api_name:
- IHostMAlloc.Alloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMAlloc::Alloc
helpviewer_keywords:
- Alloc method, IHostMAlloc interface [.NET Framework hosting]
- IHostMAlloc::Alloc method [.NET Framework hosting]
ms.assetid: a3007f5e-d75d-4b37-842b-704e9edced5e
topic_type:
- apiref
ms.openlocfilehash: e0349c273ef9e3194bb8bad167510dd8fefcab62
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708224"
---
# <a name="ihostmallocalloc-method"></a><span data-ttu-id="a23ea-103">IHostMAlloc::Alloc 方法</span><span class="sxs-lookup"><span data-stu-id="a23ea-103">IHostMAlloc::Alloc Method</span></span>

<span data-ttu-id="a23ea-104">请求宿主从堆分配指定内存量。</span><span class="sxs-lookup"><span data-stu-id="a23ea-104">Requests that the host allocate the specified amount of memory from the heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a23ea-105">语法</span><span class="sxs-lookup"><span data-stu-id="a23ea-105">Syntax</span></span>  
  
```cpp  
HRESULT Alloc (  
    [in] SIZE_T  cbSize,
    [in] EMemoryCriticalLevel dwCriticalLevel,
    [out] void** ppMem  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a23ea-106">参数</span><span class="sxs-lookup"><span data-stu-id="a23ea-106">Parameters</span></span>  

 `cbSize`  
 <span data-ttu-id="a23ea-107">中当前内存分配请求的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="a23ea-107">[in] The size, in bytes, of the current memory allocation request.</span></span>  
  
 `dwCriticalLevel`  
 <span data-ttu-id="a23ea-108">中 [EMemoryCriticalLevel](ememorycriticallevel-enumeration.md) 值之一，指示分配失败的影响。</span><span class="sxs-lookup"><span data-stu-id="a23ea-108">[in] One of the [EMemoryCriticalLevel](ememorycriticallevel-enumeration.md) values, indicating the impact of an allocation failure.</span></span>  
  
 `ppMem`  
 <span data-ttu-id="a23ea-109">弄指向分配的内存的指针; 如果请求无法完成，则为 null。</span><span class="sxs-lookup"><span data-stu-id="a23ea-109">[out] A pointer to the allocated memory, or null if the request could not be completed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a23ea-110">返回值</span><span class="sxs-lookup"><span data-stu-id="a23ea-110">Return Value</span></span>  
  
|<span data-ttu-id="a23ea-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a23ea-111">HRESULT</span></span>|<span data-ttu-id="a23ea-112">说明</span><span class="sxs-lookup"><span data-stu-id="a23ea-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a23ea-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a23ea-113">S_OK</span></span>|<span data-ttu-id="a23ea-114">`Alloc` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="a23ea-114">`Alloc` returned successfully.</span></span>|  
|<span data-ttu-id="a23ea-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a23ea-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a23ea-116"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="a23ea-116">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a23ea-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a23ea-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a23ea-118">调用超时。</span><span class="sxs-lookup"><span data-stu-id="a23ea-118">The call timed out.</span></span>|  
|<span data-ttu-id="a23ea-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a23ea-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a23ea-120">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="a23ea-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a23ea-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a23ea-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a23ea-122">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="a23ea-122">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a23ea-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a23ea-123">E_FAIL</span></span>|<span data-ttu-id="a23ea-124">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="a23ea-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a23ea-125">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="a23ea-125">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a23ea-126">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="a23ea-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="a23ea-127">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="a23ea-127">E_OUTOFMEMORY</span></span>|<span data-ttu-id="a23ea-128">没有足够的内存可用来完成分配请求。</span><span class="sxs-lookup"><span data-stu-id="a23ea-128">Not enough memory was available to complete the allocation request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a23ea-129">备注</span><span class="sxs-lookup"><span data-stu-id="a23ea-129">Remarks</span></span>  

 <span data-ttu-id="a23ea-130">CLR `IHostMalloc` 通过调用 [IHostMemoryManager：： CreateMalloc](ihostmemorymanager-createmalloc-method.md) 方法获取指向实例的接口指针。</span><span class="sxs-lookup"><span data-stu-id="a23ea-130">The CLR gets an interface pointer to an `IHostMalloc` instance by calling the [IHostMemoryManager::CreateMalloc](ihostmemorymanager-createmalloc-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a23ea-131">要求</span><span class="sxs-lookup"><span data-stu-id="a23ea-131">Requirements</span></span>  

 <span data-ttu-id="a23ea-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a23ea-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a23ea-133">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a23ea-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a23ea-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a23ea-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a23ea-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a23ea-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a23ea-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="a23ea-136">See also</span></span>

- [<span data-ttu-id="a23ea-137">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="a23ea-137">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
- [<span data-ttu-id="a23ea-138">IHostMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="a23ea-138">IHostMalloc Interface</span></span>](ihostmalloc-interface.md)
