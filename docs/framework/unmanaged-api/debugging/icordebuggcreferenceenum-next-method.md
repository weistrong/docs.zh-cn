---
description: 了解详细信息： ICorDebugGCReferenceEnum：： Next 方法
title: ICorDebugGCReferenceEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugGCReferenceEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGCReferenceEnum::Next
helpviewer_keywords:
- Next method, ICorDebugGCReferenceEnum interface [.NET Framework debugging]
- ICorDebugGCReferenceEnum::Next method [.NET Framework debugging]
ms.assetid: 91b1345c-a94f-4ef8-9696-3823d06c6d05
topic_type:
- apiref
ms.openlocfilehash: aec135fcb737a200d5a267529fa812c0852a24df
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803693"
---
# <a name="icordebuggcreferenceenumnext-method"></a><span data-ttu-id="9c51b-103">ICorDebugGCReferenceEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="9c51b-103">ICorDebugGCReferenceEnum::Next Method</span></span>

<span data-ttu-id="9c51b-104">获取指定数量的 [COR_GC_REFERENCE](cor-gc-reference-structure.md) 实例，这些实例包含有关将进行垃圾回收的对象的信息。</span><span class="sxs-lookup"><span data-stu-id="9c51b-104">Gets the specified number of [COR_GC_REFERENCE](cor-gc-reference-structure.md) instances that contain information about objects that will be garbage-collected.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c51b-105">语法</span><span class="sxs-lookup"><span data-stu-id="9c51b-105">Syntax</span></span>  
  
```cpp  
HRESULT Next(  
    [in] ULONG celt,    [out, size_is(celt), length_is(*pceltFetched)] COR_GC_REFERENCE roots[],
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9c51b-106">参数</span><span class="sxs-lookup"><span data-stu-id="9c51b-106">Parameters</span></span>  

 <span data-ttu-id="9c51b-107">celt</span><span class="sxs-lookup"><span data-stu-id="9c51b-107">celt</span></span>  
 <span data-ttu-id="9c51b-108">中要检索的根的数目。</span><span class="sxs-lookup"><span data-stu-id="9c51b-108">[in] The number of roots to be retrieved.</span></span>  
  
 <span data-ttu-id="9c51b-109">根目录</span><span class="sxs-lookup"><span data-stu-id="9c51b-109">roots</span></span>  
 <span data-ttu-id="9c51b-110">弄指针的数组，其中每个都指向一个 [COR_GC_REFERENCE](cor-gc-reference-structure.md) 对象，该对象表示要进行垃圾回收的对象的根。</span><span class="sxs-lookup"><span data-stu-id="9c51b-110">[out] An array of pointers, each of which points to a [COR_GC_REFERENCE](cor-gc-reference-structure.md) object that represents the root of an object to be garbage-collected.</span></span>  
  
 <span data-ttu-id="9c51b-111">pceltFetched</span><span class="sxs-lookup"><span data-stu-id="9c51b-111">pceltFetched</span></span>  
 <span data-ttu-id="9c51b-112">弄一个指针，指向在中实际返回的 [COR_GC_REFERENCE](cor-gc-reference-structure.md) 对象的数量 `roots` 。</span><span class="sxs-lookup"><span data-stu-id="9c51b-112">[out] A pointer to the number of [COR_GC_REFERENCE](cor-gc-reference-structure.md) objects actually returned in `roots`.</span></span> <span data-ttu-id="9c51b-113">如果 `celt` 为 1，此值可能为 `null`。</span><span class="sxs-lookup"><span data-stu-id="9c51b-113">This value may be `null` if `celt` is 1.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9c51b-114">备注</span><span class="sxs-lookup"><span data-stu-id="9c51b-114">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9c51b-115">要求</span><span class="sxs-lookup"><span data-stu-id="9c51b-115">Requirements</span></span>  

 <span data-ttu-id="9c51b-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9c51b-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9c51b-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9c51b-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9c51b-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9c51b-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9c51b-119">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9c51b-119">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c51b-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="9c51b-120">See also</span></span>

- [<span data-ttu-id="9c51b-121">ICorDebugGCReferenceEnum 接口</span><span class="sxs-lookup"><span data-stu-id="9c51b-121">ICorDebugGCReferenceEnum Interface</span></span>](icordebuggcreferenceenum-interface.md)
- [<span data-ttu-id="9c51b-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="9c51b-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
