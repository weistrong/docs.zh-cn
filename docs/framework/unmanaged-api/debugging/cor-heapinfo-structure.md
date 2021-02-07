---
description: 了解详细信息： COR_HEAPINFO 结构
title: COR_HEAPINFO 结构
ms.date: 03/30/2017
api_name:
- COR_HEAPINFO
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_HEAPINFO
helpviewer_keywords:
- COR_HEAPINFO structure [.NET Framework debugging]
ms.assetid: bfb2cd39-3e0b-4d51-ba0c-f009755c1456
topic_type:
- apiref
ms.openlocfilehash: 0841739172b3eaf807813af28e0b20fbb54608b2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712307"
---
# <a name="cor_heapinfo-structure"></a><span data-ttu-id="b9ff4-103">COR_HEAPINFO 结构</span><span class="sxs-lookup"><span data-stu-id="b9ff4-103">COR_HEAPINFO Structure</span></span>

<span data-ttu-id="b9ff4-104">提供有关垃圾回收堆的常规信息，包括它是否是可枚举的。</span><span class="sxs-lookup"><span data-stu-id="b9ff4-104">Provides general information about the garbage collection heap, including whether it is enumerable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9ff4-105">语法</span><span class="sxs-lookup"><span data-stu-id="b9ff4-105">Syntax</span></span>  
  
```cpp  
typedef struct _COR_HEAPINFO {  
    BOOL areGCStructuresValid;
    DWORD pointerSize;
    DWORD numHeaps;  
    BOOL concurrent;
    CorDebugGCType gcType;
} COR_HEAPINFO;  
```  
  
## <a name="members"></a><span data-ttu-id="b9ff4-106">成员</span><span class="sxs-lookup"><span data-stu-id="b9ff4-106">Members</span></span>  
  
|<span data-ttu-id="b9ff4-107">成员</span><span class="sxs-lookup"><span data-stu-id="b9ff4-107">Member</span></span>|<span data-ttu-id="b9ff4-108">说明</span><span class="sxs-lookup"><span data-stu-id="b9ff4-108">Description</span></span>|  
|------------|-----------------|  
|`areGCStructuresValid`|<span data-ttu-id="b9ff4-109">`true` 如果垃圾回收结构有效并且可以枚举堆，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="b9ff4-109">`true` if garbage collection structures are valid and the heap can be enumerated; otherwise, `false`.</span></span>|  
|`pointerSize`|<span data-ttu-id="b9ff4-110">目标体系结构上指针的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="b9ff4-110">The size, in bytes, of pointers on the target architecture.</span></span>|  
|`numHeaps`|<span data-ttu-id="b9ff4-111">进程中逻辑垃圾回收堆的数目。</span><span class="sxs-lookup"><span data-stu-id="b9ff4-111">The number of logical garbage collection heaps in the process.</span></span>|  
|`concurrent`|<span data-ttu-id="b9ff4-112">`TRUE` 如果启用了并发 (后台) 垃圾回收，则为;否则为 `FALSE` 。</span><span class="sxs-lookup"><span data-stu-id="b9ff4-112">`TRUE` if concurrent (background) garbage collection is enabled; otherwise, `FALSE`.</span></span>|  
|`gcType`|<span data-ttu-id="b9ff4-113">[CorDebugGCType](cordebuggctype-enumeration.md)枚举的成员，它指示垃圾回收器是在工作站上运行还是在服务器上运行。</span><span class="sxs-lookup"><span data-stu-id="b9ff4-113">A member of the [CorDebugGCType](cordebuggctype-enumeration.md) enumeration that indicates whether the garbage collector is running on a workstation or a server.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b9ff4-114">备注</span><span class="sxs-lookup"><span data-stu-id="b9ff4-114">Remarks</span></span>  

 <span data-ttu-id="b9ff4-115">使用 `COR_HEAPINFO` [ICorDebugProcess5：： GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) 方法返回结构的实例。</span><span class="sxs-lookup"><span data-stu-id="b9ff4-115">An instance of the `COR_HEAPINFO` structure is returned by calling the [ICorDebugProcess5::GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) method.</span></span>  
  
 <span data-ttu-id="b9ff4-116">枚举垃圾回收堆上的对象之前，必须始终检查 `areGCStructuresValid` 字段以确保堆处于可枚举状态。</span><span class="sxs-lookup"><span data-stu-id="b9ff4-116">Before enumerating objects on the garbage collection heap, you must always check the `areGCStructuresValid` field to ensure that the heap is in an enumerable state.</span></span> <span data-ttu-id="b9ff4-117">有关详细信息，请参阅 [ICorDebugProcess5：： GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b9ff4-117">For more information, see the [ICorDebugProcess5::GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b9ff4-118">要求</span><span class="sxs-lookup"><span data-stu-id="b9ff4-118">Requirements</span></span>  

 <span data-ttu-id="b9ff4-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b9ff4-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9ff4-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b9ff4-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b9ff4-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b9ff4-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b9ff4-122">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b9ff4-122">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9ff4-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="b9ff4-123">See also</span></span>

- [<span data-ttu-id="b9ff4-124">调试结构</span><span class="sxs-lookup"><span data-stu-id="b9ff4-124">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="b9ff4-125">调试</span><span class="sxs-lookup"><span data-stu-id="b9ff4-125">Debugging</span></span>](index.md)
