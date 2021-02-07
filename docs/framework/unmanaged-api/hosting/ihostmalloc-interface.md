---
description: 了解详细信息： IHostMalloc 接口
title: IHostMalloc 接口
ms.date: 03/30/2017
api_name:
- IHostMAlloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMAlloc
helpviewer_keywords:
- IHostMAlloc interface [.NET Framework hosting]
ms.assetid: e3c6643b-6fc7-4a99-959d-4b7b4e63fdee
topic_type:
- apiref
ms.openlocfilehash: cd04a0f71fd429ea10b9edcce02806f4afa57148
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708172"
---
# <a name="ihostmalloc-interface"></a><span data-ttu-id="c0776-103">IHostMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="c0776-103">IHostMalloc Interface</span></span>

<span data-ttu-id="c0776-104">提供一些方法，这些方法允许公共语言运行时 (CLR) 通过宿主请求从堆进行细化分配。</span><span class="sxs-lookup"><span data-stu-id="c0776-104">Provides methods that allow the common language runtime (CLR) to request fine-grained allocations from the heap through the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c0776-105">方法</span><span class="sxs-lookup"><span data-stu-id="c0776-105">Methods</span></span>  
  
|<span data-ttu-id="c0776-106">方法</span><span class="sxs-lookup"><span data-stu-id="c0776-106">Method</span></span>|<span data-ttu-id="c0776-107">说明</span><span class="sxs-lookup"><span data-stu-id="c0776-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c0776-108">Alloc 方法</span><span class="sxs-lookup"><span data-stu-id="c0776-108">Alloc Method</span></span>](ihostmalloc-alloc-method.md)|<span data-ttu-id="c0776-109">请求宿主从堆分配请求的内存量。</span><span class="sxs-lookup"><span data-stu-id="c0776-109">Requests that the host allocate the requested amount of memory from the heap.</span></span>|  
|[<span data-ttu-id="c0776-110">DebugAlloc 方法</span><span class="sxs-lookup"><span data-stu-id="c0776-110">DebugAlloc Method</span></span>](ihostmalloc-debugalloc-method.md)|<span data-ttu-id="c0776-111">请求宿主从堆分配请求的内存量，并另外跟踪内存的分配位置。</span><span class="sxs-lookup"><span data-stu-id="c0776-111">Requests that the host allocate the requested amount of memory from the heap, and additionally track where the memory was allocated.</span></span>|  
|[<span data-ttu-id="c0776-112">Free 方法</span><span class="sxs-lookup"><span data-stu-id="c0776-112">Free Method</span></span>](ihostmalloc-free-method.md)|<span data-ttu-id="c0776-113">释放通过使用方法分配的内存 `Alloc` 。</span><span class="sxs-lookup"><span data-stu-id="c0776-113">Frees memory that was allocated by using the `Alloc` method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c0776-114">备注</span><span class="sxs-lookup"><span data-stu-id="c0776-114">Remarks</span></span>  

 <span data-ttu-id="c0776-115">CLR `IHostMalloc` 通过调用 [IHostMemoryManager：： CreateMalloc](ihostmemorymanager-createmalloc-method.md) 方法获取指向实例的接口指针。</span><span class="sxs-lookup"><span data-stu-id="c0776-115">The CLR gets an interface pointer to an `IHostMalloc` instance by calling the [IHostMemoryManager::CreateMalloc](ihostmemorymanager-createmalloc-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0776-116">要求</span><span class="sxs-lookup"><span data-stu-id="c0776-116">Requirements</span></span>  

 <span data-ttu-id="c0776-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c0776-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0776-118">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="c0776-118">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c0776-119">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c0776-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c0776-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0776-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0776-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="c0776-121">See also</span></span>

- [<span data-ttu-id="c0776-122">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="c0776-122">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
- [<span data-ttu-id="c0776-123">承载接口</span><span class="sxs-lookup"><span data-stu-id="c0776-123">Hosting Interfaces</span></span>](hosting-interfaces.md)
