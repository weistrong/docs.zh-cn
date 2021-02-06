---
description: 了解详细信息： ICorDebugProcess5：： EnumerateHandles 方法
title: ICorDebugProcess5::EnumerateHandles 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.EnumerateHandles
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::EnumerateHandles
helpviewer_keywords:
- EnumerateHandles method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::EnumerateHandles method [.NET Framework debugging]
ms.assetid: 7d7fa796-0dc6-4ee8-9d56-40166246d91d
topic_type:
- apiref
ms.openlocfilehash: 62ca1390ceec634e6651dc013345688fe5892bcd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649905"
---
# <a name="icordebugprocess5enumeratehandles-method"></a><span data-ttu-id="4064a-103">ICorDebugProcess5::EnumerateHandles 方法</span><span class="sxs-lookup"><span data-stu-id="4064a-103">ICorDebugProcess5::EnumerateHandles Method</span></span>

<span data-ttu-id="4064a-104">获取进程中的对象句柄的枚举器。</span><span class="sxs-lookup"><span data-stu-id="4064a-104">Gets an enumerator for object handles in a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4064a-105">语法</span><span class="sxs-lookup"><span data-stu-id="4064a-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateHandles(     [in] CorGCReferenceType types,  
    [out] ICorDebugGCReferenceEnum **ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4064a-106">参数</span><span class="sxs-lookup"><span data-stu-id="4064a-106">Parameters</span></span>  

 `types`  
 <span data-ttu-id="4064a-107">中 [CorGCReferenceType](corgcreferencetype-enumeration.md) 值的按位组合，用于指定要包括在集合中的句柄的类型。</span><span class="sxs-lookup"><span data-stu-id="4064a-107">[in] A bitwise combination of [CorGCReferenceType](corgcreferencetype-enumeration.md) values that specifies the type of handles to include in the collection.</span></span>  
  
 `ppENum`  
 <span data-ttu-id="4064a-108">弄一个指针，指向 [ICorDebugGCReferenceEnum](icordebuggcreferenceenum-interface.md) 的地址，该地址是要进行垃圾回收的对象的枚举器。</span><span class="sxs-lookup"><span data-stu-id="4064a-108">[out] A pointer to the address of an [ICorDebugGCReferenceEnum](icordebuggcreferenceenum-interface.md) that is an enumerator for the objects to be garbage-collected.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4064a-109">备注</span><span class="sxs-lookup"><span data-stu-id="4064a-109">Remarks</span></span>  

 <span data-ttu-id="4064a-110">`EnumerateHandles` 是支持对句柄表的检查的 helper 函数。</span><span class="sxs-lookup"><span data-stu-id="4064a-110">`EnumerateHandles` is a helper function that supports inspection of the handle table.</span></span> <span data-ttu-id="4064a-111">它类似于 [ICorDebugProcess5：： EnumerateGCReferences](icordebugprocess5-enumerategcreferences-method.md) 方法，不同之处在于，它不是用所有要进行垃圾回收的对象填充 [ICorDebugGCReferenceEnum](icordebuggcreferenceenum-interface.md) 集合，只包括具有句柄表中的句柄的对象。</span><span class="sxs-lookup"><span data-stu-id="4064a-111">It is similar to the [ICorDebugProcess5::EnumerateGCReferences](icordebugprocess5-enumerategcreferences-method.md) method, except that rather than populating an [ICorDebugGCReferenceEnum](icordebuggcreferenceenum-interface.md) collection with all objects to be garbage-collected, it includes only objects that have handles from the handle table.</span></span>  
  
 <span data-ttu-id="4064a-112">`types`参数指定要包括在集合中的句柄类型。</span><span class="sxs-lookup"><span data-stu-id="4064a-112">The `types` parameter specifies the handle types to include in the collection.</span></span> <span data-ttu-id="4064a-113">`types` 可以是 [CorGCReferenceType](corgcreferencetype-enumeration.md) 枚举的以下三个成员之一：</span><span class="sxs-lookup"><span data-stu-id="4064a-113">`types` can be any of the following three members of the [CorGCReferenceType](corgcreferencetype-enumeration.md) enumeration:</span></span>  
  
- <span data-ttu-id="4064a-114">`CorHandleStrongOnly` 仅)  (句柄。</span><span class="sxs-lookup"><span data-stu-id="4064a-114">`CorHandleStrongOnly` (handles to strong references only).</span></span>  
  
- <span data-ttu-id="4064a-115">`CorHandleWeakOnly` 仅)  (句柄到弱引用。</span><span class="sxs-lookup"><span data-stu-id="4064a-115">`CorHandleWeakOnly` (handles to weak references only).</span></span>  
  
- <span data-ttu-id="4064a-116">`CorHandleAll` (所有) 的句柄。</span><span class="sxs-lookup"><span data-stu-id="4064a-116">`CorHandleAll` (all handles).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4064a-117">要求</span><span class="sxs-lookup"><span data-stu-id="4064a-117">Requirements</span></span>  

 <span data-ttu-id="4064a-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4064a-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4064a-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4064a-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4064a-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4064a-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4064a-121">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4064a-121">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4064a-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="4064a-122">See also</span></span>

- [<span data-ttu-id="4064a-123">调试结构</span><span class="sxs-lookup"><span data-stu-id="4064a-123">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="4064a-124">调试</span><span class="sxs-lookup"><span data-stu-id="4064a-124">Debugging</span></span>](index.md)
