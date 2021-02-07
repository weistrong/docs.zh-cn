---
description: 了解详细信息： ICorDebugProcess5：： EnumerateHeap 方法
title: ICorDebugProcess5::EnumerateHeap 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.EnumerateHeap
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::EnumerateHeap
helpviewer_keywords:
- EnumerateHeap method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::EnumerateHeap method [.NET Framework debugging]
ms.assetid: b0192104-6073-4089-a4df-dc29ee033074
topic_type:
- apiref
ms.openlocfilehash: b43e7993b114ed64d009f91746ea987198edde74
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722030"
---
# <a name="icordebugprocess5enumerateheap-method"></a><span data-ttu-id="32474-103">ICorDebugProcess5::EnumerateHeap 方法</span><span class="sxs-lookup"><span data-stu-id="32474-103">ICorDebugProcess5::EnumerateHeap Method</span></span>

<span data-ttu-id="32474-104">获取托管堆上的对象的枚举器。</span><span class="sxs-lookup"><span data-stu-id="32474-104">Gets an enumerator for the objects on the managed heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="32474-105">语法</span><span class="sxs-lookup"><span data-stu-id="32474-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateHeap(  
    [out] ICorDebugHeapEnum **ppObjects  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="32474-106">参数</span><span class="sxs-lookup"><span data-stu-id="32474-106">Parameters</span></span>  

 `ppObject`  
 <span data-ttu-id="32474-107">弄指向 [ICorDebugHeapEnum](icordebugheapenum-interface.md) 接口对象地址的指针，该接口对象是驻留在托管堆上的对象的枚举器。</span><span class="sxs-lookup"><span data-stu-id="32474-107">[out] A pointer to the address of an [ICorDebugHeapEnum](icordebugheapenum-interface.md) interface object that is an enumerator for the objects that reside on the managed heap.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="32474-108">备注</span><span class="sxs-lookup"><span data-stu-id="32474-108">Remarks</span></span>  

 <span data-ttu-id="32474-109">在调用 `ICorDebugProcess5::EnumerateHeap` 方法之前，应调用 [ICorDebugProcess5：： GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) 方法，并检查 `areGCStructuresValid` 返回 [COR_HEAPINFO](cor-heapinfo-structure.md) 对象的字段值，以确保其当前状态的垃圾回收堆可枚举。</span><span class="sxs-lookup"><span data-stu-id="32474-109">Before calling the `ICorDebugProcess5::EnumerateHeap` method, you should call the [ICorDebugProcess5::GetGCHeapInformation](icordebugprocess5-getgcheapinformation-method.md) method and examine the value of the `areGCStructuresValid` field of the returned [COR_HEAPINFO](cor-heapinfo-structure.md) object to ensure that the garbage collection heap in its current state is enumerable.</span></span> <span data-ttu-id="32474-110">此外，如果在 `ICorDebugProcess5::EnumerateHeap` `E_FAIL` 进程的生存期内附加过早，则在分配托管堆的内存之前，返回。</span><span class="sxs-lookup"><span data-stu-id="32474-110">In addition, the `ICorDebugProcess5::EnumerateHeap` returns `E_FAIL` if you attach too early in the lifetime of the process, before memory for the managed heap is allocated.</span></span>  
  
 <span data-ttu-id="32474-111">[ICorDebugHeapEnum](icordebugheapenum-interface.md)接口对象是从 ICorDebugEnum 接口派生的标准枚举器，该枚举器可用于枚举[COR_HEAPOBJECT](cor-heapobject-structure.md)的对象。</span><span class="sxs-lookup"><span data-stu-id="32474-111">The [ICorDebugHeapEnum](icordebugheapenum-interface.md) interface object is a standard enumerator derived from the ICorDebugEnum interface that allows you to enumerate [COR_HEAPOBJECT](cor-heapobject-structure.md) objects.</span></span> <span data-ttu-id="32474-112">此方法用提供所有对象的相关信息[COR_HEAPOBJECT](cor-heapobject-structure.md)实例填充[ICorDebugHeapEnum](icordebugheapenum-interface.md)集合对象。</span><span class="sxs-lookup"><span data-stu-id="32474-112">This method populates the [ICorDebugHeapEnum](icordebugheapenum-interface.md) collection object with [COR_HEAPOBJECT](cor-heapobject-structure.md) instances that provide information about all objects.</span></span> <span data-ttu-id="32474-113">集合还可以包含 [COR_HEAPOBJECT](cor-heapobject-structure.md) 实例，这些实例提供有关非对象的根对象，但未被垃圾回收器收集的对象的信息。</span><span class="sxs-lookup"><span data-stu-id="32474-113">The collection may also include [COR_HEAPOBJECT](cor-heapobject-structure.md) instances that provide information about objects that are not rooted by any object but have not yet been collected by the garbage collector.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="32474-114">要求</span><span class="sxs-lookup"><span data-stu-id="32474-114">Requirements</span></span>  

 <span data-ttu-id="32474-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="32474-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="32474-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="32474-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="32474-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="32474-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="32474-118">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="32474-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="32474-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="32474-119">See also</span></span>

- [<span data-ttu-id="32474-120">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="32474-120">ICorDebugProcess5 Interface</span></span>](icordebugprocess5-interface.md)
- [<span data-ttu-id="32474-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="32474-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
