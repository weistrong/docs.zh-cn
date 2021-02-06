---
description: 了解详细信息： ICorDebugModuleEnum：： Next 方法
title: ICorDebugModuleEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModuleEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleEnum::Next
helpviewer_keywords:
- ICorDebugModuleEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugModuleEnum interface [.NET Framework debugging]
ms.assetid: 9ff3fcd6-38fe-41f8-bfd3-f0ab6c7d77ca
topic_type:
- apiref
ms.openlocfilehash: ed9558edad80c67e7bf3febb10c3adcd027e180a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650256"
---
# <a name="icordebugmoduleenumnext-method"></a><span data-ttu-id="c678e-103">ICorDebugModuleEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="c678e-103">ICorDebugModuleEnum::Next Method</span></span>

<span data-ttu-id="c678e-104">从当前位置开始，获取由枚举指定的 "ICorDebugModule" 实例的数目 `celt` 。</span><span class="sxs-lookup"><span data-stu-id="c678e-104">Gets the number of "ICorDebugModule" instances specified by `celt` from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c678e-105">语法</span><span class="sxs-lookup"><span data-stu-id="c678e-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in]  ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugModule *modules[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c678e-106">参数</span><span class="sxs-lookup"><span data-stu-id="c678e-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="c678e-107">中 `ICorDebugModule` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="c678e-107">[in] The number of `ICorDebugModule` instances to be retrieved.</span></span>  
  
 `modules`  
 <span data-ttu-id="c678e-108">弄指针的数组，其中每个都指向一个 `ICorDebugModule` 对象。</span><span class="sxs-lookup"><span data-stu-id="c678e-108">[out] An array of pointers, each of which points to an `ICorDebugModule` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="c678e-109">弄一个指针，指向 `ICorDebugModule` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="c678e-109">[out] Pointer to the number of `ICorDebugModule` instances actually returned.</span></span> <span data-ttu-id="c678e-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="c678e-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c678e-111">要求</span><span class="sxs-lookup"><span data-stu-id="c678e-111">Requirements</span></span>  

 <span data-ttu-id="c678e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c678e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c678e-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c678e-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c678e-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c678e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c678e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c678e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c678e-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="c678e-116">See also</span></span>
