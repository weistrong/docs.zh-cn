---
description: 了解详细信息： COR_GC_STATS 结构
title: COR_GC_STATS 结构
ms.date: 03/30/2017
api_name:
- COR_GC_STATS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_GC_STATS
helpviewer_keywords:
- COR_GC_STATS structure [.NET Framework hosting]
ms.assetid: 8d4ff73e-739b-40f6-9349-359fbc99c2f9
topic_type:
- apiref
ms.openlocfilehash: 9b1002f462fb9b447e521cd1b3e5c78297eefc04
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799794"
---
# <a name="cor_gc_stats-structure"></a><span data-ttu-id="94ae5-103">COR_GC_STATS 结构</span><span class="sxs-lookup"><span data-stu-id="94ae5-103">COR_GC_STATS Structure</span></span>

<span data-ttu-id="94ae5-104">提供有关公共语言运行时 (CLR) 的垃圾回收机制的统计信息。</span><span class="sxs-lookup"><span data-stu-id="94ae5-104">Provides statistics about the garbage collection mechanism of the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94ae5-105">语法</span><span class="sxs-lookup"><span data-stu-id="94ae5-105">Syntax</span></span>  
  
```cpp  
typedef struct _COR_GC_STATS {  
    ULONG   Flags;
    SIZE_T  ExplicitGCCount;  
    SIZE_T  GenCollectionsTaken[3];  
    SIZE_T  CommittedKBytes;
    SIZE_T  ReservedKBytes;  
    SIZE_T  Gen0HeapSizeKBytes;  
    SIZE_T  Gen1HeapSizeKBytes;  
    SIZE_T  Gen2HeapSizeKBytes;  
    SIZE_T  LargeObjectHeapSizeKBytes;  
    SIZE_T  KBytesPromotedFromGen0;  
    SIZE_T  KBytesPromotedFromGen1;  
} COR_GC_STATS;  
```  
  
## <a name="members"></a><span data-ttu-id="94ae5-106">成员</span><span class="sxs-lookup"><span data-stu-id="94ae5-106">Members</span></span>  
  
|<span data-ttu-id="94ae5-107">成员</span><span class="sxs-lookup"><span data-stu-id="94ae5-107">Member</span></span>|<span data-ttu-id="94ae5-108">说明</span><span class="sxs-lookup"><span data-stu-id="94ae5-108">Description</span></span>|  
|------------|-----------------|  
|`Flags`|<span data-ttu-id="94ae5-109">指示应计算并返回的字段值。</span><span class="sxs-lookup"><span data-stu-id="94ae5-109">Indicates which field values should be calculated and returned.</span></span>|  
|`ExplicitGCCount`|<span data-ttu-id="94ae5-110">指示外部请求强制执行的垃圾回收数。</span><span class="sxs-lookup"><span data-stu-id="94ae5-110">Indicates the number of garbage collections that were forced by external request.</span></span>|  
|`GenCollectionsTaken`|<span data-ttu-id="94ae5-111">指示为每个代执行的垃圾回收数。</span><span class="sxs-lookup"><span data-stu-id="94ae5-111">Indicates the number of garbage collections performed for each generation.</span></span>|  
|`CommittedKBytes`|<span data-ttu-id="94ae5-112">所有堆中提交的总千字节数。</span><span class="sxs-lookup"><span data-stu-id="94ae5-112">The total number of kilobytes committed in all heaps.</span></span>|  
|`ReservedKBytes`|<span data-ttu-id="94ae5-113">所有堆中保留的总千字节数。</span><span class="sxs-lookup"><span data-stu-id="94ae5-113">The total number of kilobytes reserved in all heaps.</span></span>|  
|`Gen0HeapSizeKBytes`|<span data-ttu-id="94ae5-114">代零堆的大小（以 kb 为单位）。</span><span class="sxs-lookup"><span data-stu-id="94ae5-114">The size, in kilobytes, of the generation-zero heap.</span></span>|  
|`Gen1HeapSizeKBytes`|<span data-ttu-id="94ae5-115">第一代堆的大小（以 kb 为单位）。</span><span class="sxs-lookup"><span data-stu-id="94ae5-115">The size, in kilobytes, of the generation-one heap.</span></span>|  
|`Gen2HeapSizeKBytes`|<span data-ttu-id="94ae5-116">第二代堆的大小（以 kb 为单位）。</span><span class="sxs-lookup"><span data-stu-id="94ae5-116">The size, in kilobytes, of the generation-two heap.</span></span>|  
|`LargeObjectHeapSizeKBytes`|<span data-ttu-id="94ae5-117">大型对象堆的大小（以 kb 为单位）。</span><span class="sxs-lookup"><span data-stu-id="94ae5-117">The size, in kilobytes, of the large object heap.</span></span>|  
|`KBytesPromotedFromGen0`|<span data-ttu-id="94ae5-118">从零代升级到第1代的对象的大小（以 kb 为单位）。</span><span class="sxs-lookup"><span data-stu-id="94ae5-118">The size, in kilobytes, of the objects promoted from generation zero to generation one.</span></span>|  
|`KBytesPromotedFromGen1`|<span data-ttu-id="94ae5-119">从第一代升级到第二代的对象的大小（以 kb 为单位）。</span><span class="sxs-lookup"><span data-stu-id="94ae5-119">The size, in kilobytes, of the objects promoted from generation one to generation two.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="94ae5-120">备注</span><span class="sxs-lookup"><span data-stu-id="94ae5-120">Remarks</span></span>  

 <span data-ttu-id="94ae5-121">[ICLRGCManager：： GetStats](iclrgcmanager-getstats-method.md)方法要求将 `Flags` 结构的字段 `COR_GC_STATS` 设置为一个或多个[COR_GC_STAT_TYPES](cor-gc-stat-types-enumeration.md)枚举的值，以指定要设置的统计信息。</span><span class="sxs-lookup"><span data-stu-id="94ae5-121">The [ICLRGCManager::GetStats](iclrgcmanager-getstats-method.md) method requires the `Flags` field of the `COR_GC_STATS` structure to be set to one or more values of the [COR_GC_STAT_TYPES](cor-gc-stat-types-enumeration.md) enumeration to specify which statistics are to be set.</span></span>  
  
 <span data-ttu-id="94ae5-122">下表将此结构提供的统计信息映射到两个 [COR_GC_STAT_TYPES](cor-gc-stat-types-enumeration.md) 枚举值 `COR_GC_COUNTS` 和 `COR_GC_MEMORYUSAGE` 。</span><span class="sxs-lookup"><span data-stu-id="94ae5-122">The following table maps the statistics provided by this structure to the two [COR_GC_STAT_TYPES](cor-gc-stat-types-enumeration.md) enumeration values, `COR_GC_COUNTS` and `COR_GC_MEMORYUSAGE`.</span></span>  
  
|<span data-ttu-id="94ae5-123">指定者 COR_GC_COUNTS</span><span class="sxs-lookup"><span data-stu-id="94ae5-123">Specified by COR_GC_COUNTS</span></span>|<span data-ttu-id="94ae5-124">指定者 COR_GC_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="94ae5-124">Specified by COR_GC_MEMORYUSAGE</span></span>|  
|----------------------------------|---------------------------------------|  
|`ExplicitGCCount`<br /><br /> `GenCollectionsTaken`|`CommittedKBytes`<br /><br /> `ReservedKBytes`<br /><br /> `Gen0HeapSizeKBytes`<br /><br /> `Gen1HeapSizeKBytes`<br /><br /> `Gen2HeapSizeKBytes`<br /><br /> `LargeObjectHeapSizeKBytes`<br /><br /> `KBytesPromotedFromGen0`<br /><br /> `KBytesPromotedFromGen1`|  
  
 <span data-ttu-id="94ae5-125">用法的示例如下所示：</span><span class="sxs-lookup"><span data-stu-id="94ae5-125">An example of the usage is as follows:</span></span>  
  
```cpp  
COR_GC_STATS GCStats;  
GCStats.Flags = COR_GC_COUNTS | COR_GC_MEMORYUSAGE;  
pCLRGCManager->GetStats(&GCStats);  
```  
  
## <a name="requirements"></a><span data-ttu-id="94ae5-126">要求</span><span class="sxs-lookup"><span data-stu-id="94ae5-126">Requirements</span></span>  

 <span data-ttu-id="94ae5-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="94ae5-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="94ae5-128">**标头：** GCHost .idl</span><span class="sxs-lookup"><span data-stu-id="94ae5-128">**Header:** GCHost.idl</span></span>  
  
 <span data-ttu-id="94ae5-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="94ae5-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="94ae5-130">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="94ae5-130">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94ae5-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="94ae5-131">See also</span></span>

- [<span data-ttu-id="94ae5-132">承载结构</span><span class="sxs-lookup"><span data-stu-id="94ae5-132">Hosting Structures</span></span>](hosting-structures.md)
- [<span data-ttu-id="94ae5-133">自动内存管理</span><span class="sxs-lookup"><span data-stu-id="94ae5-133">Automatic Memory Management</span></span>](../../../standard/automatic-memory-management.md)
- [<span data-ttu-id="94ae5-134">垃圾回收</span><span class="sxs-lookup"><span data-stu-id="94ae5-134">Garbage Collection</span></span>](../../../standard/garbage-collection/index.md)
