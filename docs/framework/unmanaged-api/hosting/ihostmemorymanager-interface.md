---
description: 了解详细信息： IHostMemoryManager 接口
title: IHostMemoryManager 接口
ms.date: 03/30/2017
api_name:
- IHostMemoryManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager
helpviewer_keywords:
- IHostMemoryManager interface [.NET Framework hosting]
ms.assetid: a945d439-3b34-4aa4-b575-8413dd7806ce
topic_type:
- apiref
ms.openlocfilehash: c9b6f83b5c70a53388e886e1047798f660b826e0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707863"
---
# <a name="ihostmemorymanager-interface"></a><span data-ttu-id="dcbd5-103">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="dcbd5-103">IHostMemoryManager Interface</span></span>

<span data-ttu-id="dcbd5-104">提供一些方法，通过这些方法，公共语言运行时 (CLR) 通过主机进行虚拟内存请求，而不是使用标准 Win32 虚拟内存函数。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-104">Provides methods that allow the common language runtime (CLR) to make virtual memory requests through the host, instead of using the standard Win32 virtual memory functions.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="dcbd5-105">方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-105">Methods</span></span>  
  
|<span data-ttu-id="dcbd5-106">方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-106">Method</span></span>|<span data-ttu-id="dcbd5-107">说明</span><span class="sxs-lookup"><span data-stu-id="dcbd5-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="dcbd5-108">AcquiredVirtualAddressSpace 方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-108">AcquiredVirtualAddressSpace Method</span></span>](ihostmemorymanager-acquiredvirtualaddressspace-method.md)|<span data-ttu-id="dcbd5-109">向宿主通知公共语言运行时 (CLR) 已从操作系统中获取指定内存。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-109">Notifies the host that the common language runtime (CLR) has acquired the specified memory from the operating system.</span></span>|  
|[<span data-ttu-id="dcbd5-110">CreateMAlloc 方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-110">CreateMAlloc Method</span></span>](ihostmemorymanager-createmalloc-method.md)|<span data-ttu-id="dcbd5-111">获取一个接口指针，该指针指向用于从主机创建的堆请求内存分配的 [IHostMAlloc](ihostmalloc-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-111">Gets an interface pointer to an [IHostMAlloc](ihostmalloc-interface.md) instance that is used to request memory allocations from a heap created by the host.</span></span>|  
|[<span data-ttu-id="dcbd5-112">GetMemoryLoad 方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-112">GetMemoryLoad Method</span></span>](ihostmemorymanager-getmemoryload-method.md)|<span data-ttu-id="dcbd5-113">获取主机报告的当前正使用的物理内存量。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-113">Gets the amount of physical memory that is currently being used, as reported by the host.</span></span>|  
|[<span data-ttu-id="dcbd5-114">NeedsVirtualAddressSpace 方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-114">NeedsVirtualAddressSpace Method</span></span>](ihostmemorymanager-needsvirtualaddressspace-method.md)|<span data-ttu-id="dcbd5-115">向宿主通知 CLR 将尝试使用指定的内存。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-115">Notifies the host that the CLR is going to attempt to use the specified memory.</span></span>|  
|[<span data-ttu-id="dcbd5-116">RegisterMemoryNotificationCallback 方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-116">RegisterMemoryNotificationCallback Method</span></span>](ihostmemorymanager-registermemorynotificationcallback-method.md)|<span data-ttu-id="dcbd5-117">注册一个指针，该指针指向主机调用以通知 CLR 当前计算机上的当前内存负载的回调函数。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-117">Registers a pointer to a callback function that the host invokes to notify the CLR of the current memory load on the computer.</span></span>|  
|[<span data-ttu-id="dcbd5-118">ReleasedVirtualAddressSpace 方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-118">ReleasedVirtualAddressSpace Method</span></span>](ihostmemorymanager-releasedvirtualaddressspace-method.md)|<span data-ttu-id="dcbd5-119">向宿主通知 CLR 已使用指定的内存完成。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-119">Notifies the host that the CLR has finished using the specified memory.</span></span>|  
|[<span data-ttu-id="dcbd5-120">VirtualAlloc 方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-120">VirtualAlloc Method</span></span>](ihostmemorymanager-virtualalloc-method.md)|<span data-ttu-id="dcbd5-121">用作相应 Win32 函数的逻辑包装，该函数可在调用进程的虚拟地址空间中保留或提交页区域。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-121">Serves as a logical wrapper for the corresponding Win32 function, which reserves or commits a region of pages in the virtual address space of the calling process.</span></span>|  
|[<span data-ttu-id="dcbd5-122">VirtualFree 方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-122">VirtualFree Method</span></span>](ihostmemorymanager-virtualfree-method.md)|<span data-ttu-id="dcbd5-123">用作相应 Win32 函数的逻辑包装，该函数释放、解除或释放和解除调用进程的虚拟地址空间中的页面区域。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-123">Serves as a logical wrapper for the corresponding Win32 function, which releases, decommits, or releases and decommits a region of pages within the virtual address space of the calling process.</span></span>|  
|[<span data-ttu-id="dcbd5-124">VirtualProtect 方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-124">VirtualProtect Method</span></span>](ihostmemorymanager-virtualprotect-method.md)|<span data-ttu-id="dcbd5-125">用作相应 Win32 函数的逻辑包装，该函数更改调用进程的虚拟地址空间中已提交页面区域的保护。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-125">Serves as a logical wrapper for the corresponding Win32 function, which changes the protection on a region of committed pages in the virtual address space of the calling process.</span></span>|  
|[<span data-ttu-id="dcbd5-126">VirtualQuery 方法</span><span class="sxs-lookup"><span data-stu-id="dcbd5-126">VirtualQuery Method</span></span>](ihostmemorymanager-virtualquery-method.md)|<span data-ttu-id="dcbd5-127">用作相应 Win32 函数的逻辑包装，它检索有关调用进程的虚拟地址空间中的一系列页面的信息。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-127">Serves as a logical wrapper for the corresponding Win32 function, which retrieves information about a range of pages in the virtual address space of the calling process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dcbd5-128">备注</span><span class="sxs-lookup"><span data-stu-id="dcbd5-128">Remarks</span></span>  

 <span data-ttu-id="dcbd5-129">`IHostMemoryManager` 还为 CLR 提供一些方法，用于获取一个指针，通过该指针可以在堆上发出内存请求并在进程中获取由主机报告的内存压力级别。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-129">`IHostMemoryManager` also provides methods for the CLR to obtain a pointer through which to make memory requests on the heap and to get the level of memory pressure in the process, as reported by the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dcbd5-130">要求</span><span class="sxs-lookup"><span data-stu-id="dcbd5-130">Requirements</span></span>  

 <span data-ttu-id="dcbd5-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dcbd5-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dcbd5-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="dcbd5-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="dcbd5-133">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="dcbd5-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dcbd5-134">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dcbd5-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dcbd5-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="dcbd5-135">See also</span></span>

- [<span data-ttu-id="dcbd5-136">IHostMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="dcbd5-136">IHostMalloc Interface</span></span>](ihostmalloc-interface.md)
- [<span data-ttu-id="dcbd5-137">承载接口</span><span class="sxs-lookup"><span data-stu-id="dcbd5-137">Hosting Interfaces</span></span>](hosting-interfaces.md)
