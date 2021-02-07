---
description: 了解详细信息： ICorDebugProcessEnum：： Next 方法
title: ICorDebugProcessEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcessEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcessEnum::Next
helpviewer_keywords:
- Next method, ICorDebugProcessEnum interface [.NET Framework debugging]
- ICorDebugProcessEnum::Next method [.NET Framework debugging]
ms.assetid: 4ac7077c-8d88-49c4-b360-b3af0c541c63
topic_type:
- apiref
ms.openlocfilehash: e32ff2e67f3f8a0242e0a0f93ed00229fee9cc26
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691167"
---
# <a name="icordebugprocessenumnext-method"></a><span data-ttu-id="ce605-103">ICorDebugProcessEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="ce605-103">ICorDebugProcessEnum::Next Method</span></span>

<span data-ttu-id="ce605-104">从当前位置开始，从枚举中获取指定数量的 ICorDebugProcess 实例。</span><span class="sxs-lookup"><span data-stu-id="ce605-104">Gets the specified number of ICorDebugProcess instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce605-105">语法</span><span class="sxs-lookup"><span data-stu-id="ce605-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in]  ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugProcess *processes[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ce605-106">参数</span><span class="sxs-lookup"><span data-stu-id="ce605-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="ce605-107">中 `ICorDebugProcess` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="ce605-107">[in] The number of `ICorDebugProcess` instances to be retrieved.</span></span>  
  
 `processes`  
 <span data-ttu-id="ce605-108">弄一个指针数组，其中每个指针指向一个 `ICorDebugProcess` 表示进程的对象。</span><span class="sxs-lookup"><span data-stu-id="ce605-108">[out] An array of pointers, each of which points to an `ICorDebugProcess` object that represents a process.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="ce605-109">弄一个指针，指向 `ICorDebugProcess` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="ce605-109">[out] Pointer to the number of `ICorDebugProcess` instances actually returned.</span></span> <span data-ttu-id="ce605-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="ce605-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ce605-111">要求</span><span class="sxs-lookup"><span data-stu-id="ce605-111">Requirements</span></span>  

 <span data-ttu-id="ce605-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ce605-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ce605-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ce605-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ce605-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ce605-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ce605-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ce605-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
