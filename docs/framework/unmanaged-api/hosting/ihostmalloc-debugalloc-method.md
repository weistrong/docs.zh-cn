---
description: 了解详细信息： IHostMAlloc：:D ebugAlloc 方法
title: IHostMAlloc::DebugAlloc 方法
ms.date: 03/30/2017
api_name:
- IHostMAlloc.DebugAlloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMAlloc::DebugAlloc
helpviewer_keywords:
- DebugAlloc method [.NET Framework hosting]
- IHostMAlloc::DebugAlloc method [.NET Framework hosting]
ms.assetid: 0bfbc527-bea2-43ce-b041-69186f4440dd
topic_type:
- apiref
ms.openlocfilehash: f94ff0d6cc1e25daee12c67c38167f7f14829510
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708211"
---
# <a name="ihostmallocdebugalloc-method"></a><span data-ttu-id="77178-103">IHostMAlloc::DebugAlloc 方法</span><span class="sxs-lookup"><span data-stu-id="77178-103">IHostMAlloc::DebugAlloc Method</span></span>

<span data-ttu-id="77178-104">请求宿主从堆分配指定内存量，并另外跟踪内存的分配位置。</span><span class="sxs-lookup"><span data-stu-id="77178-104">Requests that the host allocate the specified amount of memory from the heap, and additionally track where the memory was allocated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77178-105">语法</span><span class="sxs-lookup"><span data-stu-id="77178-105">Syntax</span></span>  
  
```cpp  
HRESULT DebugAlloc (  
    [in]  SIZE_T  cbSize,
    [in]  EMemoryCriticalLevel dwCriticalLevel,
    [in]  char*   pszFileName,
    [in]  int     iLineNo,
    [out] void**  ppMem  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="77178-106">参数</span><span class="sxs-lookup"><span data-stu-id="77178-106">Parameters</span></span>  

 `cbSize`  
 <span data-ttu-id="77178-107">中当前内存分配请求的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="77178-107">[in] The size, in bytes, of the current memory allocation request.</span></span>  
  
 `dwCriticalLevel`  
 <span data-ttu-id="77178-108">中 [EMemoryCriticalLevel](ememorycriticallevel-enumeration.md) 值之一，指示分配失败的影响。</span><span class="sxs-lookup"><span data-stu-id="77178-108">[in] One of the [EMemoryCriticalLevel](ememorycriticallevel-enumeration.md) values, indicating the impact of an allocation failure.</span></span>  
  
 `pszFileName`  
 <span data-ttu-id="77178-109">中正在调试的可执行文件的代码文件。</span><span class="sxs-lookup"><span data-stu-id="77178-109">[in] The code file of the executable being debugged.</span></span>  
  
 `iLineNo`  
 <span data-ttu-id="77178-110">中 `pszFileName` 请求分配的行号。</span><span class="sxs-lookup"><span data-stu-id="77178-110">[in] The line number in `pszFileName` where the allocation was requested.</span></span>  
  
 `ppMem`  
 <span data-ttu-id="77178-111">弄指向分配的内存的指针; 如果请求无法完成，则为 null。</span><span class="sxs-lookup"><span data-stu-id="77178-111">[out] A pointer to the allocated memory, or null if the request could not be completed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="77178-112">返回值</span><span class="sxs-lookup"><span data-stu-id="77178-112">Return Value</span></span>  
  
|<span data-ttu-id="77178-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="77178-113">HRESULT</span></span>|<span data-ttu-id="77178-114">说明</span><span class="sxs-lookup"><span data-stu-id="77178-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="77178-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="77178-115">S_OK</span></span>|<span data-ttu-id="77178-116">`DebugAlloc` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="77178-116">`DebugAlloc` returned successfully.</span></span>|  
|<span data-ttu-id="77178-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="77178-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="77178-118">CLR 未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="77178-118">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="77178-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="77178-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="77178-120">调用超时。</span><span class="sxs-lookup"><span data-stu-id="77178-120">The call timed out.</span></span>|  
|<span data-ttu-id="77178-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="77178-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="77178-122">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="77178-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="77178-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="77178-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="77178-124">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="77178-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="77178-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="77178-125">E_FAIL</span></span>|<span data-ttu-id="77178-126">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="77178-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="77178-127">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="77178-127">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="77178-128">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="77178-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="77178-129">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="77178-129">E_OUTOFMEMORY</span></span>|<span data-ttu-id="77178-130">没有足够的内存可用来完成分配请求。</span><span class="sxs-lookup"><span data-stu-id="77178-130">Not enough memory was available to complete the allocation request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="77178-131">备注</span><span class="sxs-lookup"><span data-stu-id="77178-131">Remarks</span></span>  

 <span data-ttu-id="77178-132">CLR 通过调用[IHostMemoryManager：： CreateMalloc](ihostmemorymanager-createmalloc-method.md)方法获取指向[IHostMalloc](ihostmalloc-interface.md)实例的接口指针。</span><span class="sxs-lookup"><span data-stu-id="77178-132">The CLR gets an interface pointer to an [IHostMalloc](ihostmalloc-interface.md) instance by calling the [IHostMemoryManager::CreateMalloc](ihostmemorymanager-createmalloc-method.md) method.</span></span> <span data-ttu-id="77178-133">`DebugAlloc` 允许运行时获取代码文件信息，以便在调试期间使用。</span><span class="sxs-lookup"><span data-stu-id="77178-133">`DebugAlloc` allows the runtime to get code file information for use during debugging.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77178-134">要求</span><span class="sxs-lookup"><span data-stu-id="77178-134">Requirements</span></span>  

 <span data-ttu-id="77178-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="77178-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77178-136">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="77178-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="77178-137">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="77178-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="77178-138">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="77178-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77178-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="77178-139">See also</span></span>

- [<span data-ttu-id="77178-140">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="77178-140">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
- [<span data-ttu-id="77178-141">IHostMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="77178-141">IHostMalloc Interface</span></span>](ihostmalloc-interface.md)
