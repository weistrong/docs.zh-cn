---
description: 了解详细信息： ICorDebugCodeEnum：： Next 方法
title: ICorDebugCodeEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCodeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCodeEnum::Next
helpviewer_keywords:
- ICorDebugCodeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugEnum interface [.NET Framework debugging]
ms.assetid: 644ece86-384d-4c63-9fba-52c789616ff7
topic_type:
- apiref
ms.openlocfilehash: 51d46718891ce3df537c675175eacc4e33b92f79
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764744"
---
# <a name="icordebugcodeenumnext-method"></a><span data-ttu-id="d7172-103">ICorDebugCodeEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="d7172-103">ICorDebugCodeEnum::Next Method</span></span>

<span data-ttu-id="d7172-104">从当前位置开始，从枚举中获取指定的 "ICorDebugCode" 实例数。</span><span class="sxs-lookup"><span data-stu-id="d7172-104">Gets the specified number of "ICorDebugCode" instances from the enumeration, starting at the current position.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7172-105">语法</span><span class="sxs-lookup"><span data-stu-id="d7172-105">Syntax</span></span>

```cpp
HRESULT Next (
    [in] ULONG  celt,
    [out, size_is(celt), length_is(*pceltFetched)]
        ICorDebugCode *values[],
    [out] ULONG *pceltFetched
);
```

## <a name="parameters"></a><span data-ttu-id="d7172-106">参数</span><span class="sxs-lookup"><span data-stu-id="d7172-106">Parameters</span></span>

`celt`  
<span data-ttu-id="d7172-107">中 `ICorDebugCode` 要检索的实例数。</span><span class="sxs-lookup"><span data-stu-id="d7172-107">[in] The number of `ICorDebugCode` instances to be retrieved.</span></span>

`values`  
<span data-ttu-id="d7172-108">弄指针的数组，其中每个都指向一个 `ICorDebugCode` 对象。</span><span class="sxs-lookup"><span data-stu-id="d7172-108">[out] An array of pointers, each of which points to an `ICorDebugCode` object.</span></span>

`pceltFetched`  
<span data-ttu-id="d7172-109">弄一个指针，指向 `ICorDebugCode` 实际返回的实例数。</span><span class="sxs-lookup"><span data-stu-id="d7172-109">[out] A pointer to the number of `ICorDebugCode` instances actually returned.</span></span> <span data-ttu-id="d7172-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="d7172-110">This value may be null if `celt` is one.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7172-111">要求</span><span class="sxs-lookup"><span data-stu-id="d7172-111">Requirements</span></span>

<span data-ttu-id="d7172-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d7172-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="d7172-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d7172-113">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="d7172-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d7172-114">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="d7172-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d7172-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
