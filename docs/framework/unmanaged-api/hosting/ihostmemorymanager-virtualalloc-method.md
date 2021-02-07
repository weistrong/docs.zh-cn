---
description: 了解详细信息： IHostMemoryManager：： VirtualAlloc 方法
title: IHostMemoryManager::VirtualAlloc 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.VirtualAlloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::VirtualAlloc
helpviewer_keywords:
- VirtualAlloc method [.NET Framework hosting]
- IHostMemoryManager::VirtualAlloc method [.NET Framework hosting]
ms.assetid: 4dff3646-a050-4bd9-ac31-fe307e8637ec
topic_type:
- apiref
ms.openlocfilehash: 28682aea5e6e7951b3b8f0a9af946a3f3828601b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707834"
---
# <a name="ihostmemorymanagervirtualalloc-method"></a><span data-ttu-id="b1c88-103">IHostMemoryManager::VirtualAlloc 方法</span><span class="sxs-lookup"><span data-stu-id="b1c88-103">IHostMemoryManager::VirtualAlloc Method</span></span>

<span data-ttu-id="b1c88-104">用作相应 Win32 函数的逻辑包装。</span><span class="sxs-lookup"><span data-stu-id="b1c88-104">Serves as a logical wrapper for the corresponding Win32 function.</span></span> <span data-ttu-id="b1c88-105">的 Win32 实现 `VirtualAlloc` 保留或提交调用进程的虚拟地址空间中的页面区域。</span><span class="sxs-lookup"><span data-stu-id="b1c88-105">The Win32 implementation of `VirtualAlloc` reserves or commits a region of pages in the virtual address space of the calling process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1c88-106">语法</span><span class="sxs-lookup"><span data-stu-id="b1c88-106">Syntax</span></span>  
  
```cpp  
HRESULT VirtualAlloc (  
    [in]  void*   pAddress,  
    [in]  SIZE_T  dwSize,  
    [in]  DWORD   flAllocationType,  
    [in]  DWORD   flProtect,  
    [in]  EMemoryCriticalLevel dwCriticalLevel,  
    [out] void**  ppMem  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b1c88-107">参数</span><span class="sxs-lookup"><span data-stu-id="b1c88-107">Parameters</span></span>  

 `pAddress`  
 <span data-ttu-id="b1c88-108">中指向要分配的区域的起始地址的指针。</span><span class="sxs-lookup"><span data-stu-id="b1c88-108">[in] A pointer to the starting address of the region to allocate.</span></span>  
  
 `dwSize`  
 <span data-ttu-id="b1c88-109">中区域的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="b1c88-109">[in] The size, in bytes, of the region.</span></span>  
  
 `flAllocationType`  
 <span data-ttu-id="b1c88-110">中内存分配的类型。</span><span class="sxs-lookup"><span data-stu-id="b1c88-110">[in] The type of memory allocation.</span></span>  
  
 `flProtect`  
 <span data-ttu-id="b1c88-111">中要分配的页面区域的内存保护。</span><span class="sxs-lookup"><span data-stu-id="b1c88-111">[in] Memory protection for the region of pages to be allocated.</span></span>  
  
 `dwCriticalLevel`  
 <span data-ttu-id="b1c88-112">中指示分配失败的影响的 [EMemoryCriticalLevel](ememorycriticallevel-enumeration.md) 值。</span><span class="sxs-lookup"><span data-stu-id="b1c88-112">[in] An [EMemoryCriticalLevel](ememorycriticallevel-enumeration.md) value that indicates the impact of an allocation failure.</span></span>  
  
 `ppMem`  
 <span data-ttu-id="b1c88-113">弄指向分配的内存的起始地址的指针; 如果无法满足请求，则为 null。</span><span class="sxs-lookup"><span data-stu-id="b1c88-113">[out] Pointer to the starting address of the allocated memory, or null if the request could not be satisfied.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b1c88-114">返回值</span><span class="sxs-lookup"><span data-stu-id="b1c88-114">Return Value</span></span>  
  
|<span data-ttu-id="b1c88-115">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b1c88-115">HRESULT</span></span>|<span data-ttu-id="b1c88-116">说明</span><span class="sxs-lookup"><span data-stu-id="b1c88-116">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b1c88-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1c88-117">S_OK</span></span>|<span data-ttu-id="b1c88-118">`VirtualAlloc` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="b1c88-118">`VirtualAlloc` returned successfully.</span></span>|  
|<span data-ttu-id="b1c88-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b1c88-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b1c88-120"> (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="b1c88-120">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b1c88-121">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b1c88-121">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b1c88-122">调用超时。</span><span class="sxs-lookup"><span data-stu-id="b1c88-122">The call timed out.</span></span>|  
|<span data-ttu-id="b1c88-123">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b1c88-123">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b1c88-124">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="b1c88-124">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b1c88-125">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b1c88-125">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b1c88-126">已阻止的线程或纤程正在等待某个事件时，该事件被取消。</span><span class="sxs-lookup"><span data-stu-id="b1c88-126">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b1c88-127">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b1c88-127">E_FAIL</span></span>|<span data-ttu-id="b1c88-128">发生未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="b1c88-128">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b1c88-129">当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。</span><span class="sxs-lookup"><span data-stu-id="b1c88-129">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b1c88-130">对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="b1c88-130">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="b1c88-131">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="b1c88-131">E_OUTOFMEMORY</span></span>|<span data-ttu-id="b1c88-132">没有足够的可用内存来完成分配请求</span><span class="sxs-lookup"><span data-stu-id="b1c88-132">Not enough memory was available to complete the allocation request</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b1c88-133">备注</span><span class="sxs-lookup"><span data-stu-id="b1c88-133">Remarks</span></span>  

 <span data-ttu-id="b1c88-134">可以通过调用在进程的地址空间中保留区域 `VirtualAlloc` 。</span><span class="sxs-lookup"><span data-stu-id="b1c88-134">You reserve a region in the address space of your process by calling `VirtualAlloc`.</span></span> <span data-ttu-id="b1c88-135">`pAddress`参数包含所需内存块的起始地址。</span><span class="sxs-lookup"><span data-stu-id="b1c88-135">The `pAddress` parameter contains the beginning address of the memory block you want.</span></span> <span data-ttu-id="b1c88-136">此参数通常设置为 null。</span><span class="sxs-lookup"><span data-stu-id="b1c88-136">This parameter is typically set to null.</span></span> <span data-ttu-id="b1c88-137">操作系统会保留可用于进程的免费地址范围记录。</span><span class="sxs-lookup"><span data-stu-id="b1c88-137">The operating system keeps a record of free address ranges available to your process.</span></span> <span data-ttu-id="b1c88-138">如果 `pAddress` 值为 null，则指示系统在其认为合适的位置保留区域。</span><span class="sxs-lookup"><span data-stu-id="b1c88-138">A `pAddress` value of null instructs the system to reserve the region wherever it sees fit.</span></span> <span data-ttu-id="b1c88-139">或者，您可以为内存块提供特定的起始地址。</span><span class="sxs-lookup"><span data-stu-id="b1c88-139">Alternatively, you can provide a specific starting address for the memory block.</span></span> <span data-ttu-id="b1c88-140">在这两种情况下，output 参数 `ppMem` 将作为指向已分配内存的指针返回。</span><span class="sxs-lookup"><span data-stu-id="b1c88-140">In both cases, the output parameter `ppMem` is returned as a pointer to the allocated memory.</span></span> <span data-ttu-id="b1c88-141">函数本身返回 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="b1c88-141">The function itself returns an HRESULT value.</span></span>  
  
 <span data-ttu-id="b1c88-142">Win32 `VirtualAlloc` 函数没有 `ppMem` 参数，而是返回指向分配的内存的指针。</span><span class="sxs-lookup"><span data-stu-id="b1c88-142">The Win32 `VirtualAlloc` function does not have a `ppMem` parameter, and returns the pointer to the allocated memory instead.</span></span> <span data-ttu-id="b1c88-143">有关详细信息，请参阅 Windows 平台文档。</span><span class="sxs-lookup"><span data-stu-id="b1c88-143">For more information, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1c88-144">要求</span><span class="sxs-lookup"><span data-stu-id="b1c88-144">Requirements</span></span>  

 <span data-ttu-id="b1c88-145">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b1c88-145">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1c88-146">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b1c88-146">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b1c88-147">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b1c88-147">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b1c88-148">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b1c88-148">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1c88-149">请参阅</span><span class="sxs-lookup"><span data-stu-id="b1c88-149">See also</span></span>

- [<span data-ttu-id="b1c88-150">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="b1c88-150">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
