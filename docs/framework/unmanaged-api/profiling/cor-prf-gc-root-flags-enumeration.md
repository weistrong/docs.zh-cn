---
description: 了解详细信息： COR_PRF_GC_ROOT_FLAGS 枚举
title: COR_PRF_GC_ROOT_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_GC_ROOT_FLAGS
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_GC_ROOT_FLAGS
helpviewer_keywords:
- COR_PRF_GC_ROOT_FLAGS enumeration [.NET Framework profiling]
ms.assetid: 4611ee6f-0f05-4d84-91e1-e83d5e7dd7e4
topic_type:
- apiref
ms.openlocfilehash: 6d566ed5ac1d0b4e15a855fbbb8a0fca3a5a429e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648794"
---
# <a name="cor_prf_gc_root_flags-enumeration"></a><span data-ttu-id="3310b-103">COR_PRF_GC_ROOT_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="3310b-103">COR_PRF_GC_ROOT_FLAGS Enumeration</span></span>

<span data-ttu-id="3310b-104">指示垃圾回收根的属性。</span><span class="sxs-lookup"><span data-stu-id="3310b-104">Indicates a property of a garbage collection root.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3310b-105">语法</span><span class="sxs-lookup"><span data-stu-id="3310b-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_GC_ROOT_PINNING = 0x1,  
    COR_PRF_GC_ROOT_WEAKREF = 0x2,  
    COR_PRF_GC_ROOT_INTERIOR = 0x4,  
    COR_PRF_GC_ROOT_REFCOUNTED = 0x8,  
} COR_PRF_GC_ROOT_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="3310b-106">成员</span><span class="sxs-lookup"><span data-stu-id="3310b-106">Members</span></span>  
  
|<span data-ttu-id="3310b-107">成员</span><span class="sxs-lookup"><span data-stu-id="3310b-107">Member</span></span>|<span data-ttu-id="3310b-108">说明</span><span class="sxs-lookup"><span data-stu-id="3310b-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_GC_ROOT_PINNING`|<span data-ttu-id="3310b-109">根禁止垃圾回收移动对象。</span><span class="sxs-lookup"><span data-stu-id="3310b-109">The root prevents a garbage collection from moving the object.</span></span>|  
|`COR_PRF_GC_ROOT_WEAKREF`|<span data-ttu-id="3310b-110">根不会阻止垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="3310b-110">The root does not prevent garbage collection.</span></span>|  
|`COR_PRF_GC_ROOT_INTERIOR`|<span data-ttu-id="3310b-111">根引用的是对象的字段，而不是对象本身。</span><span class="sxs-lookup"><span data-stu-id="3310b-111">The root refers to a field of the object rather than the object itself.</span></span>|  
|`COR_PRF_GC_ROOT_REFCOUNTED`|<span data-ttu-id="3310b-112">如果对象的引用计数为特定值，则根禁止垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="3310b-112">The root prevents garbage collection if the reference count of the object is a certain value.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3310b-113">备注</span><span class="sxs-lookup"><span data-stu-id="3310b-113">Remarks</span></span>  

 <span data-ttu-id="3310b-114">`COR_PRF_GC_ROOT_FLAGS` 是一个位掩码，提供有关特殊根的附加信息。</span><span class="sxs-lookup"><span data-stu-id="3310b-114">`COR_PRF_GC_ROOT_FLAGS` is a bitmask that provides additional information about special roots.</span></span> <span data-ttu-id="3310b-115">但是，并非所有的根都是特殊的。</span><span class="sxs-lookup"><span data-stu-id="3310b-115">However, not all roots are special.</span></span> <span data-ttu-id="3310b-116">例如，某些根不是弱引用、内部指针、固定或引用计数的。</span><span class="sxs-lookup"><span data-stu-id="3310b-116">For example, some roots are not weak references, interior pointers, pinned, or reference-counted.</span></span> <span data-ttu-id="3310b-117">对于这类根，没有要传达的标志。</span><span class="sxs-lookup"><span data-stu-id="3310b-117">For such roots, there are no flags to convey.</span></span> <span data-ttu-id="3310b-118">因此，使用此枚举的方法（如 [ICorProfilerCallback2：： RootReferences2](icorprofilercallback2-rootreferences2-method.md) 方法）为标志位掩码发送0，指示所有标志都处于关闭状态。</span><span class="sxs-lookup"><span data-stu-id="3310b-118">Therefore, methods that use this enumeration, such as the [ICorProfilerCallback2::RootReferences2](icorprofilercallback2-rootreferences2-method.md) method, send 0 for the flags bitmask, indicating that all flags are turned off.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3310b-119">要求</span><span class="sxs-lookup"><span data-stu-id="3310b-119">Requirements</span></span>  

 <span data-ttu-id="3310b-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3310b-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3310b-121">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3310b-121">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3310b-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3310b-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3310b-123">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3310b-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3310b-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="3310b-124">See also</span></span>

- [<span data-ttu-id="3310b-125">分析枚举</span><span class="sxs-lookup"><span data-stu-id="3310b-125">Profiling Enumerations</span></span>](profiling-enumerations.md)
