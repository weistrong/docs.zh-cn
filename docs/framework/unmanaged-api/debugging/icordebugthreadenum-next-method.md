---
description: 了解详细信息： ICorDebugThreadEnum：： Next 方法
title: ICorDebugThreadEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThreadEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThreadEnum::Next
helpviewer_keywords:
- ICorDebugThreadEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugThreadEnum interface [.NET Framework debugging]
ms.assetid: f967c93d-9a7f-4aaf-99a1-a1317899ff3f
topic_type:
- apiref
ms.openlocfilehash: 2cfb651d65eaf0f5797444ea1bec587cebdde2f4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658420"
---
# <a name="icordebugthreadenumnext-method"></a><span data-ttu-id="55143-103">ICorDebugThreadEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="55143-103">ICorDebugThreadEnum::Next Method</span></span>

<span data-ttu-id="55143-104">从当前位置开始，获取枚举中指定的 ICorDebugThread 实例的数目。</span><span class="sxs-lookup"><span data-stu-id="55143-104">Gets the number of specified ICorDebugThread instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55143-105">语法</span><span class="sxs-lookup"><span data-stu-id="55143-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugThread *threads[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="55143-106">参数</span><span class="sxs-lookup"><span data-stu-id="55143-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="55143-107">中 `ICorDebugThread` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="55143-107">[in] The number of `ICorDebugThread` instances to be retrieved.</span></span>  
  
 `threads`  
 <span data-ttu-id="55143-108">弄指针的数组，其中每个都指向 `ICorDebugThread` 表示线程的对象。</span><span class="sxs-lookup"><span data-stu-id="55143-108">[out] An array of pointers, each of which points to an `ICorDebugThread` object that represents a thread.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="55143-109">弄一个指针，指向 `ICorDebugThread` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="55143-109">[out] Pointer to the number of `ICorDebugThread` instances actually returned.</span></span> <span data-ttu-id="55143-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="55143-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="55143-111">要求</span><span class="sxs-lookup"><span data-stu-id="55143-111">Requirements</span></span>  

 <span data-ttu-id="55143-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="55143-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="55143-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="55143-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="55143-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="55143-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="55143-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="55143-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
