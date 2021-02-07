---
description: 了解详细信息： ICorDebugTypeEnum：： Next 方法
title: ICorDebugTypeEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugTypeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugTypeEnum::Next
helpviewer_keywords:
- ICorDebugTypeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugTypeEnum interface [.NET Framework debugging]
ms.assetid: d0fdeba3-c195-4ece-8caf-79b1f40025d2
topic_type:
- apiref
ms.openlocfilehash: 9260f5f2d1a2d6943a705f7e7ef1ead3d2924cdc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690582"
---
# <a name="icordebugtypeenumnext-method"></a><span data-ttu-id="70d7c-103">ICorDebugTypeEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="70d7c-103">ICorDebugTypeEnum::Next Method</span></span>

<span data-ttu-id="70d7c-104">从当前位置开始，获取由枚举指定的 "ICorDebugType" 实例的数目 `celt` 。</span><span class="sxs-lookup"><span data-stu-id="70d7c-104">Gets the number of "ICorDebugType" instances specified by `celt` from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70d7c-105">语法</span><span class="sxs-lookup"><span data-stu-id="70d7c-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in]  ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugType *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="70d7c-106">参数</span><span class="sxs-lookup"><span data-stu-id="70d7c-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="70d7c-107">中 `ICorDebugType` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="70d7c-107">[in] The number of `ICorDebugType` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="70d7c-108">弄指针的数组，其中每个都指向一个 `ICorDebugType` 对象。</span><span class="sxs-lookup"><span data-stu-id="70d7c-108">[out] An array of pointers, each of which points to an `ICorDebugType` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="70d7c-109">弄一个指针，指向 `ICorDebugType` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="70d7c-109">[out] Pointer to the number of `ICorDebugType` instances actually returned.</span></span> <span data-ttu-id="70d7c-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="70d7c-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="70d7c-111">要求</span><span class="sxs-lookup"><span data-stu-id="70d7c-111">Requirements</span></span>  

 <span data-ttu-id="70d7c-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="70d7c-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="70d7c-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="70d7c-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="70d7c-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="70d7c-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="70d7c-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="70d7c-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70d7c-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="70d7c-116">See also</span></span>
