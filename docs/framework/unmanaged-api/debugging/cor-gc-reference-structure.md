---
description: 了解详细信息： COR_GC_REFERENCE 结构
title: COR_GC_REFERENCE 结构
ms.date: 03/30/2017
api_name:
- COR_GC_REFERENCE
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_GC_REFERENCE
helpviewer_keywords:
- COR_GC_REFERENCE structure [.NET Framework debugging]
ms.assetid: 162e8179-0cd4-4110-8f06-5f387698bd62
topic_type:
- apiref
ms.openlocfilehash: 38518bb1eb870081621bf32af9e63cdaa208dbd3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801808"
---
# <a name="cor_gc_reference-structure"></a><span data-ttu-id="6bfa8-103">COR_GC_REFERENCE 结构</span><span class="sxs-lookup"><span data-stu-id="6bfa8-103">COR_GC_REFERENCE Structure</span></span>

<span data-ttu-id="6bfa8-104">包含有关要进行垃圾回收的对象的信息。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-104">Contains information about an object that is to be garbage-collected.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6bfa8-105">语法</span><span class="sxs-lookup"><span data-stu-id="6bfa8-105">Syntax</span></span>  
  
```cpp  
typedef struct _COR_GC_REFERENCE {  
    ICorDebugAppDomain *domain;
    ICorDebugValue *location;  
    CorGCReferenceType type;  
    UINT64 extraData;  
} COR_GC_REFERENCE;  
```  
  
## <a name="members"></a><span data-ttu-id="6bfa8-106">成员</span><span class="sxs-lookup"><span data-stu-id="6bfa8-106">Members</span></span>  
  
|<span data-ttu-id="6bfa8-107">成员</span><span class="sxs-lookup"><span data-stu-id="6bfa8-107">Member</span></span>|<span data-ttu-id="6bfa8-108">说明</span><span class="sxs-lookup"><span data-stu-id="6bfa8-108">Description</span></span>|  
|------------|-----------------|  
|`domain`|<span data-ttu-id="6bfa8-109">指向句柄或对象所属的应用程序域的指针。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-109">A pointer to the application domain to which the handle or object belongs.</span></span> <span data-ttu-id="6bfa8-110">其值可以是 `null` 。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-110">Its value may be `null`.</span></span>|  
|`location`|<span data-ttu-id="6bfa8-111">与要进行垃圾回收的对象相对应的 ICorDebugValue 或 ICorDebugReferenceValue 接口。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-111">Either an ICorDebugValue or an ICorDebugReferenceValue interface that corresponds to the object to be garbage-collected.</span></span>|  
|`type`|<span data-ttu-id="6bfa8-112">一个 [CorGCReferenceType](corgcreferencetype-enumeration.md) 枚举值，该值指示根的来源。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-112">A [CorGCReferenceType](corgcreferencetype-enumeration.md) enumeration value that indicates where the root came from.</span></span> <span data-ttu-id="6bfa8-113">有关详细信息，请参见“备注”部分。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-113">For more information, see the Remarks section.</span></span>|  
|`extraData`|<span data-ttu-id="6bfa8-114">有关要进行垃圾回收的对象的其他数据。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-114">Additional data about the object to be garbage-collected.</span></span> <span data-ttu-id="6bfa8-115">此信息取决于对象的源，如字段所示 `type` 。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-115">This information depends on the source of the object, as indicated by the `type` field.</span></span> <span data-ttu-id="6bfa8-116">有关详细信息，请参见“备注”部分。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-116">For more information, see the Remarks section.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6bfa8-117">备注</span><span class="sxs-lookup"><span data-stu-id="6bfa8-117">Remarks</span></span>  

 <span data-ttu-id="6bfa8-118">该 `type` 字段是一个 [CorGCReferenceType](corgcreferencetype-enumeration.md) 枚举值，该值指示引用来自何处。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-118">The `type` field is a [CorGCReferenceType](corgcreferencetype-enumeration.md) enumeration value that indicates where the reference came from.</span></span> <span data-ttu-id="6bfa8-119">特定 `COR_GC_REFERENCE` 值可以反映以下任意一种类型的托管对象：</span><span class="sxs-lookup"><span data-stu-id="6bfa8-119">A particular `COR_GC_REFERENCE` value can reflect any of the following kinds of managed objects:</span></span>  
  
- <span data-ttu-id="6bfa8-120">所有托管堆栈中的对象 (`CorGCReferenceType.CorReferenceStack`) 。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-120">Objects from all managed stacks (`CorGCReferenceType.CorReferenceStack`).</span></span> <span data-ttu-id="6bfa8-121">这包括托管代码中的实时引用以及由公共语言运行时创建的对象。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-121">This includes live references in managed code, as well as objects created by the common language runtime.</span></span>  
  
- <span data-ttu-id="6bfa8-122">句柄表中的对象 (`CorGCReferenceType.CorHandle*`) 。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-122">Objects from the handle table (`CorGCReferenceType.CorHandle*`).</span></span> <span data-ttu-id="6bfa8-123">这包括 `HNDTYPE_STRONG` 模块中 (和 `HNDTYPE_REFCOUNT`) 和静态变量的强引用。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-123">This includes strong references (`HNDTYPE_STRONG` and `HNDTYPE_REFCOUNT`) and static variables in a module.</span></span>  
  
- <span data-ttu-id="6bfa8-124">终结器队列中的对象 (`CorGCReferenceType.CorReferenceFinalizer`) 。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-124">Objects from the finalizer queue (`CorGCReferenceType.CorReferenceFinalizer`).</span></span> <span data-ttu-id="6bfa8-125">终结器队列根对象，直到终结器运行。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-125">The finalizer queue roots objects until the finalizer has run.</span></span>  
  
 <span data-ttu-id="6bfa8-126">该 `extraData` 字段包含其他数据，具体取决于引用 (或类型) 的源。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-126">The `extraData` field contains extra data depending on the source (or type) of the reference.</span></span> <span data-ttu-id="6bfa8-127">可能的值有：</span><span class="sxs-lookup"><span data-stu-id="6bfa8-127">Possible values are:</span></span>  
  
- <span data-ttu-id="6bfa8-128">`DependentSource`.</span><span class="sxs-lookup"><span data-stu-id="6bfa8-128">`DependentSource`.</span></span> <span data-ttu-id="6bfa8-129">如果 `type` 为 `CorGCREferenceType.CorHandleStrongDependent` ，则此字段为对象，如果为，则此字段为要在其上进行垃圾回收的对象的根 `COR_GC_REFERENCE.Location` 。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-129">If the `type` is `CorGCREferenceType.CorHandleStrongDependent`, this field is the object that, if alive, roots the object to be garbage-collected at `COR_GC_REFERENCE.Location`.</span></span>  
  
- <span data-ttu-id="6bfa8-130">`RefCount`.</span><span class="sxs-lookup"><span data-stu-id="6bfa8-130">`RefCount`.</span></span> <span data-ttu-id="6bfa8-131">如果 `type` 为 `CorGCREferenceType.CorHandleStrongRefCount` ，则此字段是句柄的引用计数。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-131">If the `type` is `CorGCREferenceType.CorHandleStrongRefCount`, this field is the reference count of the handle.</span></span>  
  
- <span data-ttu-id="6bfa8-132">`Size`.</span><span class="sxs-lookup"><span data-stu-id="6bfa8-132">`Size`.</span></span> <span data-ttu-id="6bfa8-133">如果 `type` 为 `CorGCREferenceType.CorHandleStrongSizedByref` ，则此字段是垃圾回收器为其计算对象根的对象树的最后一个大小。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-133">If the `type` is `CorGCREferenceType.CorHandleStrongSizedByref`, this field is the last size of the object tree for which the garbage collector calculated the object roots.</span></span> <span data-ttu-id="6bfa8-134">请注意，此计算不一定是最新的。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-134">Note that this calculation is not necessarily up to date.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6bfa8-135">要求</span><span class="sxs-lookup"><span data-stu-id="6bfa8-135">Requirements</span></span>  

 <span data-ttu-id="6bfa8-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6bfa8-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6bfa8-137">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6bfa8-137">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6bfa8-138">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6bfa8-138">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6bfa8-139">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6bfa8-139">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6bfa8-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="6bfa8-140">See also</span></span>

- [<span data-ttu-id="6bfa8-141">调试结构</span><span class="sxs-lookup"><span data-stu-id="6bfa8-141">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="6bfa8-142">调试</span><span class="sxs-lookup"><span data-stu-id="6bfa8-142">Debugging</span></span>](index.md)
