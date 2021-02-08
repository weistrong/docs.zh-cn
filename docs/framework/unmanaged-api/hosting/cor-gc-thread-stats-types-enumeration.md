---
description: 了解详细信息： COR_GC_THREAD_STATS_TYPES 枚举
title: COR_GC_THREAD_STATS_TYPES 枚举
ms.date: 03/30/2017
api_name:
- COR_GC_THREAD_STATS_TYPES
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_GC_THREAD_STATS_TYPES
helpviewer_keywords:
- COR_GC_THREAD_STATS_TYPES enumeration [.NET Framework hosting]
ms.assetid: aa227704-0ab1-4b08-aee2-1f439762162e
topic_type:
- apiref
ms.openlocfilehash: 04bc4e11c527b83cf5f1384b1092cc0d084008a3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799767"
---
# <a name="cor_gc_thread_stats_types-enumeration"></a><span data-ttu-id="e241e-103">COR_GC_THREAD_STATS_TYPES 枚举</span><span class="sxs-lookup"><span data-stu-id="e241e-103">COR_GC_THREAD_STATS_TYPES Enumeration</span></span>

<span data-ttu-id="e241e-104">指示线程的垃圾回收统计信息。</span><span class="sxs-lookup"><span data-stu-id="e241e-104">Indicates the garbage collection statistics for a thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e241e-105">语法</span><span class="sxs-lookup"><span data-stu-id="e241e-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_GC_THREAD_HAS_PROMOTED_BYTES  = 0x00000001  
} COR_GC_THREAD_STATS_TYPES;  
```  
  
## <a name="members"></a><span data-ttu-id="e241e-106">成员</span><span class="sxs-lookup"><span data-stu-id="e241e-106">Members</span></span>  
  
|<span data-ttu-id="e241e-107">成员</span><span class="sxs-lookup"><span data-stu-id="e241e-107">Member</span></span>|<span data-ttu-id="e241e-108">说明</span><span class="sxs-lookup"><span data-stu-id="e241e-108">Description</span></span>|  
|------------|-----------------|  
|`COR_GC_THREAD_HAS_PROMOTED_BYTES`|<span data-ttu-id="e241e-109">线程具有在最近的垃圾回收中升级的字节数。</span><span class="sxs-lookup"><span data-stu-id="e241e-109">The thread has bytes that were promoted in the most recent garbage collection.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e241e-110">要求</span><span class="sxs-lookup"><span data-stu-id="e241e-110">Requirements</span></span>  

 <span data-ttu-id="e241e-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e241e-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e241e-112">**标头：** GCHost，GCHost</span><span class="sxs-lookup"><span data-stu-id="e241e-112">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="e241e-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e241e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e241e-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="e241e-114">See also</span></span>

- [<span data-ttu-id="e241e-115">承载枚举</span><span class="sxs-lookup"><span data-stu-id="e241e-115">Hosting Enumerations</span></span>](hosting-enumerations.md)
