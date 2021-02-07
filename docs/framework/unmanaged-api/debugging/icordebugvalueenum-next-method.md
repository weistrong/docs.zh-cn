---
description: 了解详细信息： ICorDebugValueEnum：： Next 方法
title: ICorDebugValueEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugValueEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueEnum::Next
helpviewer_keywords:
- ICorDebugValueEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugValueEnum interface [.NET Framework debugging]
ms.assetid: f5ef94dd-dfee-49d3-a398-b110f8906dd8
topic_type:
- apiref
ms.openlocfilehash: 9a02c769f69651227669eb4b3f8c5ce41b670a73
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690101"
---
# <a name="icordebugvalueenumnext-method"></a><span data-ttu-id="f07bf-103">ICorDebugValueEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="f07bf-103">ICorDebugValueEnum::Next Method</span></span>

<span data-ttu-id="f07bf-104">从当前位置开始，从枚举中获取指定的 "ICorDebugValue" 实例数。</span><span class="sxs-lookup"><span data-stu-id="f07bf-104">Gets the specified number of "ICorDebugValue" instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f07bf-105">语法</span><span class="sxs-lookup"><span data-stu-id="f07bf-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in]  ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugValue *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f07bf-106">参数</span><span class="sxs-lookup"><span data-stu-id="f07bf-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="f07bf-107">中 `ICorDebugValue` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="f07bf-107">[in] The number of `ICorDebugValue` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="f07bf-108">弄指针的数组，其中每个都指向一个 `ICorDebugValue` 对象。</span><span class="sxs-lookup"><span data-stu-id="f07bf-108">[out] An array of pointers, each of which points to an `ICorDebugValue` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="f07bf-109">弄一个指针，指向 `ICorDebugValue` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="f07bf-109">[out] Pointer to the number of `ICorDebugValue` instances actually returned.</span></span> <span data-ttu-id="f07bf-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="f07bf-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f07bf-111">要求</span><span class="sxs-lookup"><span data-stu-id="f07bf-111">Requirements</span></span>  

 <span data-ttu-id="f07bf-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f07bf-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f07bf-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f07bf-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f07bf-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f07bf-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f07bf-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f07bf-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f07bf-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="f07bf-116">See also</span></span>
