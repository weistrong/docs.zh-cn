---
description: 了解详细信息： ICorDebugFrameEnum：： Next 方法
title: ICorDebugFrameEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrameEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrameEnum::Next
helpviewer_keywords:
- ICorDebugFrameEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugFrameEnum interface [.NET Framework debugging]
ms.assetid: 0bc96acb-6179-4328-a447-cda562ce9e98
topic_type:
- apiref
ms.openlocfilehash: 67b7dd0282c07358f942990f8915150d6449fd32
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692662"
---
# <a name="icordebugframeenumnext-method"></a><span data-ttu-id="a5979-103">ICorDebugFrameEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="a5979-103">ICorDebugFrameEnum::Next Method</span></span>

<span data-ttu-id="a5979-104">从当前位置开始，获取指定数量的 ICorDebugFrame 实例。</span><span class="sxs-lookup"><span data-stu-id="a5979-104">Gets the specified number of ICorDebugFrame instances, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a5979-105">语法</span><span class="sxs-lookup"><span data-stu-id="a5979-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugFrame *frames[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a5979-106">参数</span><span class="sxs-lookup"><span data-stu-id="a5979-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="a5979-107">中 `ICorDebugFrame` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="a5979-107">[in] The number of `ICorDebugFrame` instances to be retrieved.</span></span>  
  
 `frames`  
 <span data-ttu-id="a5979-108">弄指针的数组，其中每个都指向一个 `ICorDebugFrame` 对象。</span><span class="sxs-lookup"><span data-stu-id="a5979-108">[out] An array of pointers, each of which points to an `ICorDebugFrame` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="a5979-109">弄一个指针，指向 `ICorDebugFrame` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="a5979-109">[out] A pointer to the number of `ICorDebugFrame` instances actually returned.</span></span> <span data-ttu-id="a5979-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="a5979-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a5979-111">要求</span><span class="sxs-lookup"><span data-stu-id="a5979-111">Requirements</span></span>  

 <span data-ttu-id="a5979-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a5979-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a5979-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a5979-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a5979-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a5979-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a5979-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a5979-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
