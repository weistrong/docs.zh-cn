---
description: 了解详细信息： ICorDebugChainEnum：： Next 方法
title: ICorDebugChainEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChainEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChainEnum::Next
helpviewer_keywords:
- ICorDebugChainEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugChainEnum interface [.NET Framework debugging]
ms.assetid: 6b791351-bcc5-4ddd-9cab-eff2f7dd5142
topic_type:
- apiref
ms.openlocfilehash: 5ab6665eb5af6d9f145f9aab67aeb75b4769e7e3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711565"
---
# <a name="icordebugchainenumnext-method"></a><span data-ttu-id="3aebb-103">ICorDebugChainEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="3aebb-103">ICorDebugChainEnum::Next Method</span></span>

<span data-ttu-id="3aebb-104">从当前位置开始，从枚举中获取指定数量的 ICorDebugChain 实例。</span><span class="sxs-lookup"><span data-stu-id="3aebb-104">Gets the specified number of ICorDebugChain instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3aebb-105">语法</span><span class="sxs-lookup"><span data-stu-id="3aebb-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugChain *chains[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3aebb-106">参数</span><span class="sxs-lookup"><span data-stu-id="3aebb-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="3aebb-107">中 `ICorDebugChain` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="3aebb-107">[in] The number of `ICorDebugChain` instances to be retrieved.</span></span>  
  
 `chains`  
 <span data-ttu-id="3aebb-108">弄一个指针数组，其中每个指针指向一个 `ICorDebugChain` 表示链的对象。</span><span class="sxs-lookup"><span data-stu-id="3aebb-108">[out] An array of pointers, each of which points to an `ICorDebugChain` object that represents a chain.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="3aebb-109">弄一个指针，指向 `ICorDebugChain` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="3aebb-109">[out] A pointer to the number of `ICorDebugChain` instances actually returned.</span></span> <span data-ttu-id="3aebb-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="3aebb-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3aebb-111">要求</span><span class="sxs-lookup"><span data-stu-id="3aebb-111">Requirements</span></span>  

 <span data-ttu-id="3aebb-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3aebb-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3aebb-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3aebb-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3aebb-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3aebb-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3aebb-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3aebb-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
