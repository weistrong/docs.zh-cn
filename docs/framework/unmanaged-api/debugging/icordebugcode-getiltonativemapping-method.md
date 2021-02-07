---
description: 了解详细信息： ICorDebugCode：： GetILToNativeMapping 方法
title: ICorDebugCode::GetILToNativeMapping 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetILToNativeMapping
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetILToNativeMapping
helpviewer_keywords:
- GetILToNativeMapping method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetILToNativeMapping method [.NET Framework debugging]
ms.assetid: a8ecd8c8-9627-4356-9c6f-bd05e24637c0
topic_type:
- apiref
ms.openlocfilehash: 808ed450fced8afecc2b637a3b990a894897b350
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711188"
---
# <a name="icordebugcodegetiltonativemapping-method"></a><span data-ttu-id="26621-103">ICorDebugCode::GetILToNativeMapping 方法</span><span class="sxs-lookup"><span data-stu-id="26621-103">ICorDebugCode::GetILToNativeMapping Method</span></span>

<span data-ttu-id="26621-104">获取 "COR_DEBUG_IL_TO_NATIVE_MAP" 实例的数组，这些实例表示从 Microsoft 中间语言 (MSIL 到本机偏移量) 偏移量的映射。</span><span class="sxs-lookup"><span data-stu-id="26621-104">Gets an array of "COR_DEBUG_IL_TO_NATIVE_MAP" instances that represent mappings from Microsoft intermediate language (MSIL) offsets to native offsets.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26621-105">语法</span><span class="sxs-lookup"><span data-stu-id="26621-105">Syntax</span></span>  
  
```cpp  
HRESULT GetILToNativeMapping (  
    [in]  ULONG32    cMap,  
    [out] ULONG32    *pcMap,  
    [out, size_is(cMap), length_is(*pcMap)]  
        COR_DEBUG_IL_TO_NATIVE_MAP map[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="26621-106">参数</span><span class="sxs-lookup"><span data-stu-id="26621-106">Parameters</span></span>  

 `cMap`  
 <span data-ttu-id="26621-107">[in] `map` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="26621-107">[in] The size of the `map` array.</span></span>  
  
 `pcMap`  
 <span data-ttu-id="26621-108">弄一个指针，它指向数组中返回的元素的实际数目 `map` 。</span><span class="sxs-lookup"><span data-stu-id="26621-108">[out] A pointer to the actual number of elements returned in the `map` array.</span></span>  
  
 `map`  
 <span data-ttu-id="26621-109">弄结构的数组 `COR_DEBUG_IL_TO_NATIVE_MAP` ，其中每个结构都表示从 MSIL 偏移量到本机偏移量的映射。</span><span class="sxs-lookup"><span data-stu-id="26621-109">[out] An array of `COR_DEBUG_IL_TO_NATIVE_MAP` structures, each of which represents a mapping from an MSIL offset to a native offset.</span></span>  
  
 <span data-ttu-id="26621-110">返回的元素数组没有排序。</span><span class="sxs-lookup"><span data-stu-id="26621-110">There is no ordering to the array of elements returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="26621-111">备注</span><span class="sxs-lookup"><span data-stu-id="26621-111">Remarks</span></span>  

 <span data-ttu-id="26621-112">`GetILToNativeMapping`仅当此 "ICorDebugCode" 实例表示实时 (JIT) 从 MSIL 代码编译的本机代码时，此方法才会返回有意义的结果。</span><span class="sxs-lookup"><span data-stu-id="26621-112">The `GetILToNativeMapping` method returns meaningful results only if this "ICorDebugCode" instance represents native code that was just-in-time (JIT) compiled from MSIL code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26621-113">要求</span><span class="sxs-lookup"><span data-stu-id="26621-113">Requirements</span></span>  

 <span data-ttu-id="26621-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="26621-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="26621-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="26621-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="26621-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="26621-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="26621-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="26621-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26621-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="26621-118">See also</span></span>

- [<span data-ttu-id="26621-119">ICorDebugCode 接口</span><span class="sxs-lookup"><span data-stu-id="26621-119">ICorDebugCode Interface</span></span>](icordebugcode-interface1.md)
