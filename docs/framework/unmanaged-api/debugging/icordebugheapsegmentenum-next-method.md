---
description: 了解详细信息： ICorDebugHeapSegmentEnum：： Next 方法
title: ICorDebugHeapSegmentEnum::Next 方法
ms.date: 03/30/2017
api_name:
- Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapSegmentEnum::Next
helpviewer_keywords:
- ICorDebugHeapSegmentEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugHeapSegmentEnum interface [.NET Framework debugging]
ms.assetid: 51625fd0-7399-49c7-b22b-5dfb05451fe6
topic_type:
- apiref
ms.openlocfilehash: 8d2ddfb4df82969fa9cf580ed8a7f903f9d6c260
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803670"
---
# <a name="icordebugheapsegmentenumnext-method"></a><span data-ttu-id="20398-103">ICorDebugHeapSegmentEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="20398-103">ICorDebugHeapSegmentEnum::Next Method</span></span>

<span data-ttu-id="20398-104">获取指定数量的 [COR_SEGMENT](cor-segment-structure.md) 实例，这些实例包含有关托管堆的内存区域的信息。</span><span class="sxs-lookup"><span data-stu-id="20398-104">Gets the specified number of [COR_SEGMENT](cor-segment-structure.md) instances that contain information about memory regions of the managed heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20398-105">语法</span><span class="sxs-lookup"><span data-stu-id="20398-105">Syntax</span></span>  
  
```cpp  
HRESULT Next(  
    [in] ULONG celt,    [out, size_is(celt), length_is(*pceltFetched)] COR_SEGMENT segments[],
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="20398-106">参数</span><span class="sxs-lookup"><span data-stu-id="20398-106">Parameters</span></span>  

 <span data-ttu-id="20398-107">celt</span><span class="sxs-lookup"><span data-stu-id="20398-107">celt</span></span>  
 <span data-ttu-id="20398-108">中要检索的段数。</span><span class="sxs-lookup"><span data-stu-id="20398-108">[in] The number of segments to be retrieved.</span></span>  
  
 <span data-ttu-id="20398-109">段</span><span class="sxs-lookup"><span data-stu-id="20398-109">segments</span></span>  
 <span data-ttu-id="20398-110">弄指针数组，其中每个都指向一个 [COR_SEGMENT](cor-segment-structure.md) 对象，该对象提供有关托管堆中的内存区域的信息。</span><span class="sxs-lookup"><span data-stu-id="20398-110">[out] An array of pointers, each of which points to a [COR_SEGMENT](cor-segment-structure.md) object that provides information about a region of memory in the managed heap.</span></span>  
  
 <span data-ttu-id="20398-111">pceltFetched</span><span class="sxs-lookup"><span data-stu-id="20398-111">pceltFetched</span></span>  
 <span data-ttu-id="20398-112">弄一个指针，指向在中实际返回的 [COR_SEGMENT](cor-segment-structure.md) 对象的数量 `segments` 。</span><span class="sxs-lookup"><span data-stu-id="20398-112">[out] A pointer to the number of [COR_SEGMENT](cor-segment-structure.md) objects actually returned in `segments`.</span></span> <span data-ttu-id="20398-113">如果 `celt` 为 1，此值可能为 `null`。</span><span class="sxs-lookup"><span data-stu-id="20398-113">This value may be `null` if `celt` is 1.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="20398-114">备注</span><span class="sxs-lookup"><span data-stu-id="20398-114">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20398-115">要求</span><span class="sxs-lookup"><span data-stu-id="20398-115">Requirements</span></span>  

 <span data-ttu-id="20398-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="20398-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20398-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="20398-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="20398-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="20398-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="20398-119">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20398-119">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20398-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="20398-120">See also</span></span>

- [<span data-ttu-id="20398-121">ICorDebugHeapSegmentEnum 接口</span><span class="sxs-lookup"><span data-stu-id="20398-121">ICorDebugHeapSegmentEnum Interface</span></span>](icordebugheapsegmentenum-interface.md)
- [<span data-ttu-id="20398-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="20398-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
