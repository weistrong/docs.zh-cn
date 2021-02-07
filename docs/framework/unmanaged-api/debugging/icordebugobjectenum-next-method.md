---
description: 了解详细信息： ICorDebugObjectEnum：： Next 方法
title: ICorDebugObjectEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugObjectEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectEnum::Next
helpviewer_keywords:
- Next method, ICorDebugObjectEnum interface [.NET Framework debugging]
- ICorDebugObjectEnum::Next method [.NET Framework debugging]
ms.assetid: 10093e3d-26b6-4ad7-8ef3-bbf66243fc02
topic_type:
- apiref
ms.openlocfilehash: dd7d4240827e14962edf7573b59b273f65231bcf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729037"
---
# <a name="icordebugobjectenumnext-method"></a><span data-ttu-id="7ffc7-103">ICorDebugObjectEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="7ffc7-103">ICorDebugObjectEnum::Next Method</span></span>

<span data-ttu-id="7ffc7-104">从当前位置开始，获取枚举中指定数目的对象 (Rva) 的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="7ffc7-104">Gets the relative virtual addresses (RVAs) of the specified number of objects from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7ffc7-105">语法</span><span class="sxs-lookup"><span data-stu-id="7ffc7-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]
        CORDB_ADDRESS objects[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7ffc7-106">参数</span><span class="sxs-lookup"><span data-stu-id="7ffc7-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="7ffc7-107">[in] 要检索的对象数。</span><span class="sxs-lookup"><span data-stu-id="7ffc7-107">[in] The number of objects to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="7ffc7-108">弄指针的数组，其中每个都指向一个 CORDB_ADDRESS 对象。</span><span class="sxs-lookup"><span data-stu-id="7ffc7-108">[out] An array of pointers, each of which points to a CORDB_ADDRESS object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="7ffc7-109">弄一个指针，指向实际返回的对象数。</span><span class="sxs-lookup"><span data-stu-id="7ffc7-109">[out] Pointer to the number of objects actually returned.</span></span> <span data-ttu-id="7ffc7-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="7ffc7-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7ffc7-111">要求</span><span class="sxs-lookup"><span data-stu-id="7ffc7-111">Requirements</span></span>  

 <span data-ttu-id="7ffc7-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7ffc7-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7ffc7-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7ffc7-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7ffc7-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7ffc7-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7ffc7-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7ffc7-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7ffc7-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="7ffc7-116">See also</span></span>
