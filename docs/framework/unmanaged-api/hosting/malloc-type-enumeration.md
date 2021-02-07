---
description: 了解详细信息： MALLOC_TYPE 枚举
title: MALLOC_TYPE 枚举
ms.date: 03/30/2017
api_name:
- MALLOC_TYPE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- MALLOC_TYPE
helpviewer_keywords:
- MALLOC_TYPE Enumeration
ms.assetid: c02476f9-23a2-4af7-9282-aa9c42c7429b
topic_type:
- apiref
ms.openlocfilehash: 47eb58107d79309c34af5f0acdf614804d1f208f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679792"
---
# <a name="malloc_type-enumeration"></a><span data-ttu-id="4764f-103">MALLOC_TYPE 枚举</span><span class="sxs-lookup"><span data-stu-id="4764f-103">MALLOC_TYPE Enumeration</span></span>

<span data-ttu-id="4764f-104">包含指定正在分配的内存特性的值。</span><span class="sxs-lookup"><span data-stu-id="4764f-104">Contains values that specify the characteristics of the memory that is being allocated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4764f-105">语法</span><span class="sxs-lookup"><span data-stu-id="4764f-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    MALLOC_THREADSAFE = 0x1,  
    MALLOC_EXECUTABLE = 0x2,  
} MALLOC_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="4764f-106">成员</span><span class="sxs-lookup"><span data-stu-id="4764f-106">Members</span></span>  
  
|<span data-ttu-id="4764f-107">成员</span><span class="sxs-lookup"><span data-stu-id="4764f-107">Member</span></span>|<span data-ttu-id="4764f-108">说明</span><span class="sxs-lookup"><span data-stu-id="4764f-108">Description</span></span>|  
|------------|-----------------|  
|`MALLOC_EXECUTABLE`|<span data-ttu-id="4764f-109">分配的内存可以包含可执行文件。</span><span class="sxs-lookup"><span data-stu-id="4764f-109">The allocated memory can contain an executable file.</span></span>|  
|`MALLOC_THREADSAFE`|<span data-ttu-id="4764f-110">分配的内存是线程安全的。</span><span class="sxs-lookup"><span data-stu-id="4764f-110">The allocated memory is thread-safe.</span></span> <span data-ttu-id="4764f-111">也就是说，无需任何同步即可通过多个线程访问内存。</span><span class="sxs-lookup"><span data-stu-id="4764f-111">That is, the memory can be accessed by multiple threads without any synchronization.</span></span><br /><br /> <span data-ttu-id="4764f-112">如果未设置此标志，则必须序列化对该对象的调用。</span><span class="sxs-lookup"><span data-stu-id="4764f-112">If this flag is not set, calls on the object must be serialized.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4764f-113">要求</span><span class="sxs-lookup"><span data-stu-id="4764f-113">Requirements</span></span>  

 <span data-ttu-id="4764f-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4764f-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4764f-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="4764f-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4764f-116">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4764f-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4764f-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4764f-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4764f-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="4764f-118">See also</span></span>

- [<span data-ttu-id="4764f-119">承载枚举</span><span class="sxs-lookup"><span data-stu-id="4764f-119">Hosting Enumerations</span></span>](hosting-enumerations.md)
