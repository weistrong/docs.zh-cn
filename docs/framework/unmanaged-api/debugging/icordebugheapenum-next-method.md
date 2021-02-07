---
description: 了解详细信息： ICorDebugHeapEnum：： Next 方法
title: ICorDebugHeapEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugHeapEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapEnum::Next
helpviewer_keywords:
- ICorDebugHeapEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugHeapEnum interface [.NET Framework debugging]
ms.assetid: 2221fd06-9e27-4113-972e-2530db8c3594
topic_type:
- apiref
ms.openlocfilehash: 22e81b9b0c4ac2027f932187b6f860d08adf6f97
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691936"
---
# <a name="icordebugheapenumnext-method"></a><span data-ttu-id="94710-103">ICorDebugHeapEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="94710-103">ICorDebugHeapEnum::Next Method</span></span>

<span data-ttu-id="94710-104">获取指定数量的 [COR_HEAPOBJECT](cor-heapobject-structure.md) 实例，这些实例包含有关托管堆上的对象的信息。</span><span class="sxs-lookup"><span data-stu-id="94710-104">Gets the specified number of [COR_HEAPOBJECT](cor-heapobject-structure.md) instances that contain information about objects on the managed heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94710-105">语法</span><span class="sxs-lookup"><span data-stu-id="94710-105">Syntax</span></span>  
  
```cpp  
HRESULT Next(  
    [in] ULONG celt,    [out, size_is(celt), length_is(*pceltFetched)] COR_HEAPOBJECT  objects[],
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="94710-106">参数</span><span class="sxs-lookup"><span data-stu-id="94710-106">Parameters</span></span>  

 <span data-ttu-id="94710-107">celt</span><span class="sxs-lookup"><span data-stu-id="94710-107">celt</span></span>  
 <span data-ttu-id="94710-108">[in] 要检索的对象数。</span><span class="sxs-lookup"><span data-stu-id="94710-108">[in] The number of objects to be retrieved.</span></span>  
  
 <span data-ttu-id="94710-109">对象</span><span class="sxs-lookup"><span data-stu-id="94710-109">objects</span></span>  
 <span data-ttu-id="94710-110">弄指针数组，其中每个都指向一个 [COR_HEAPOBJECT](cor-heapobject-structure.md) 对象，该对象提供有关托管堆上的对象的信息。</span><span class="sxs-lookup"><span data-stu-id="94710-110">[out] An array of pointers, each of which points to a [COR_HEAPOBJECT](cor-heapobject-structure.md) object that provides information about an object on the managed heap.</span></span>  
  
 <span data-ttu-id="94710-111">pceltFetched</span><span class="sxs-lookup"><span data-stu-id="94710-111">pceltFetched</span></span>  
 <span data-ttu-id="94710-112">弄一个指针，指向在中实际返回的 [COR_HEAPOBJECT](cor-heapobject-structure.md) 对象的数量 `objects` 。</span><span class="sxs-lookup"><span data-stu-id="94710-112">[out] A pointer to the number of [COR_HEAPOBJECT](cor-heapobject-structure.md) objects actually returned in `objects`.</span></span> <span data-ttu-id="94710-113">如果 `celt` 为 1，此值可能为 `null`。</span><span class="sxs-lookup"><span data-stu-id="94710-113">This value may be `null` if `celt` is 1.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="94710-114">备注</span><span class="sxs-lookup"><span data-stu-id="94710-114">Remarks</span></span>  

 <span data-ttu-id="94710-115">`COR_HEAPOBJECT.type` 字段是嵌套的引用计数 COM 接口的标识符。</span><span class="sxs-lookup"><span data-stu-id="94710-115">The `COR_HEAPOBJECT.type` field is the identifier of a nested reference-counted COM interface.</span></span> <span data-ttu-id="94710-116">此引用必须由 `ICorDebugHeapEnum::Next` 的调用方释放。</span><span class="sxs-lookup"><span data-stu-id="94710-116">This reference must be released by the caller of `ICorDebugHeapEnum::Next`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="94710-117">要求</span><span class="sxs-lookup"><span data-stu-id="94710-117">Requirements</span></span>  

 <span data-ttu-id="94710-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="94710-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="94710-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="94710-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="94710-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="94710-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="94710-121">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="94710-121">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94710-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="94710-122">See also</span></span>

- [<span data-ttu-id="94710-123">ICorDebugHeapEnum 接口</span><span class="sxs-lookup"><span data-stu-id="94710-123">ICorDebugHeapEnum Interface</span></span>](icordebugheapenum-interface.md)
- [<span data-ttu-id="94710-124">调试接口</span><span class="sxs-lookup"><span data-stu-id="94710-124">Debugging Interfaces</span></span>](debugging-interfaces.md)
