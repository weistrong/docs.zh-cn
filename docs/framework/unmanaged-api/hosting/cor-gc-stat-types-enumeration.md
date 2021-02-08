---
description: 了解详细信息： COR_GC_STAT_TYPES 枚举
title: COR_GC_STAT_TYPES 枚举
ms.date: 03/30/2017
api_name:
- COR_GC_STAT_TYPES
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_GC_STAT_TYPES
helpviewer_keywords:
- COR_GC_STAT_TYPES enumeration [.NET Framework hosting]
ms.assetid: fc51d6db-f7f8-408b-b93d-c166fc712c99
topic_type:
- apiref
ms.openlocfilehash: c4ea3175c777d49a5d6cffdf506f42e479784971
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799795"
---
# <a name="cor_gc_stat_types-enumeration"></a><span data-ttu-id="592ab-103">COR_GC_STAT_TYPES 枚举</span><span class="sxs-lookup"><span data-stu-id="592ab-103">COR_GC_STAT_TYPES Enumeration</span></span>

<span data-ttu-id="592ab-104">指定要为垃圾回收记录的统计信息。</span><span class="sxs-lookup"><span data-stu-id="592ab-104">Specifies the statistics to be recorded for a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="592ab-105">语法</span><span class="sxs-lookup"><span data-stu-id="592ab-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_GC_COUNTS                 = 0x00000001  
    COR_GC_MEMORYUSAGE            = 0x00000002  
} COR_GC_STAT_TYPES;  
```  
  
## <a name="remarks"></a><span data-ttu-id="592ab-106">备注</span><span class="sxs-lookup"><span data-stu-id="592ab-106">Remarks</span></span>  

 <span data-ttu-id="592ab-107">此枚举指定 [COR_GC_STATS](cor-gc-stats-structure.md) 结构中的哪些统计信息由 [ICLRGCManager：： GetStats](iclrgcmanager-getstats-method.md) 方法设置。</span><span class="sxs-lookup"><span data-stu-id="592ab-107">This enumeration specifies which statistics in the [COR_GC_STATS](cor-gc-stats-structure.md) structure are to be set by [ICLRGCManager::GetStats](iclrgcmanager-getstats-method.md) method.</span></span>  
  
## <a name="members"></a><span data-ttu-id="592ab-108">成员</span><span class="sxs-lookup"><span data-stu-id="592ab-108">Members</span></span>  
  
|<span data-ttu-id="592ab-109">成员</span><span class="sxs-lookup"><span data-stu-id="592ab-109">Member</span></span>|<span data-ttu-id="592ab-110">说明</span><span class="sxs-lookup"><span data-stu-id="592ab-110">Description</span></span>|  
|------------|-----------------|  
|`COR_GC_COUNTS`|<span data-ttu-id="592ab-111">记录为每个代执行的垃圾回收数。</span><span class="sxs-lookup"><span data-stu-id="592ab-111">Records the number of garbage collections performed for each generation.</span></span>|  
|`COR_GC_MEMORYUSAGE`|<span data-ttu-id="592ab-112">记录内存使用情况和垃圾回收大小统计信息。</span><span class="sxs-lookup"><span data-stu-id="592ab-112">Records memory usage and garbage collection size statistics.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="592ab-113">要求</span><span class="sxs-lookup"><span data-stu-id="592ab-113">Requirements</span></span>  

 <span data-ttu-id="592ab-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="592ab-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="592ab-115">**标头：** GCHost，GCHost</span><span class="sxs-lookup"><span data-stu-id="592ab-115">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="592ab-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="592ab-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="592ab-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="592ab-117">See also</span></span>

- [<span data-ttu-id="592ab-118">COR_GC_STATS 结构</span><span class="sxs-lookup"><span data-stu-id="592ab-118">COR_GC_STATS Structure</span></span>](cor-gc-stats-structure.md)
- [<span data-ttu-id="592ab-119">承载枚举</span><span class="sxs-lookup"><span data-stu-id="592ab-119">Hosting Enumerations</span></span>](hosting-enumerations.md)
