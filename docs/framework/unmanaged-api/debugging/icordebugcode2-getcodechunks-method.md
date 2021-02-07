---
description: 了解详细信息： ICorDebugCode2：： GetCodeChunks 方法
title: ICorDebugCode2::GetCodeChunks 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode2.GetCodeChunks
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode2::GetCodeChunks
helpviewer_keywords:
- GetCodeChunks method [.NET Framework debugging]
- ICorDebugCode2::GetCodeChunks method [.NET Framework debugging]
ms.assetid: 210a2f02-2678-4555-bc4a-78a0408764c8
topic_type:
- apiref
ms.openlocfilehash: 371d077466ff2390293d9d4e320d4c95a992fe54
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764952"
---
# <a name="icordebugcode2getcodechunks-method"></a><span data-ttu-id="f0ce6-103">ICorDebugCode2::GetCodeChunks 方法</span><span class="sxs-lookup"><span data-stu-id="f0ce6-103">ICorDebugCode2::GetCodeChunks Method</span></span>

<span data-ttu-id="f0ce6-104">获取包含此代码对象的代码块。</span><span class="sxs-lookup"><span data-stu-id="f0ce6-104">Gets the chunks of code that this code object is composed of.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ce6-105">语法</span><span class="sxs-lookup"><span data-stu-id="f0ce6-105">Syntax</span></span>

```cpp
HRESULT GetCodeChunks (
    [in]  ULONG32     cbufSize,
    [out] ULONG32     *pcnumChunks,
    [out, size_is(cbufSize), length_is(*pcnumChunks)]
        CodeChunkInfo chunks[]
);
```

## <a name="parameters"></a><span data-ttu-id="f0ce6-106">参数</span><span class="sxs-lookup"><span data-stu-id="f0ce6-106">Parameters</span></span>

`cbufSize`  
<span data-ttu-id="f0ce6-107">中数组的大小 `chunks` 。</span><span class="sxs-lookup"><span data-stu-id="f0ce6-107">[in] Size of the `chunks` array.</span></span>

`pcnumChunks`  
<span data-ttu-id="f0ce6-108">弄数组中返回的块的数目 `chunks` 。</span><span class="sxs-lookup"><span data-stu-id="f0ce6-108">[out] The number of chunks returned in the `chunks` array.</span></span>

`chunks`  
<span data-ttu-id="f0ce6-109">弄"CodeChunkInfo" 结构的数组，其中每个结构都表示一个代码块。</span><span class="sxs-lookup"><span data-stu-id="f0ce6-109">[out] An array of "CodeChunkInfo" structures, each of which represents a single chunk of code.</span></span> <span data-ttu-id="f0ce6-110">如果的值 `cbufSize` 为0，则此参数可以为 null。</span><span class="sxs-lookup"><span data-stu-id="f0ce6-110">If the value of `cbufSize` is 0, this parameter can be null.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0ce6-111">备注</span><span class="sxs-lookup"><span data-stu-id="f0ce6-111">Remarks</span></span>

<span data-ttu-id="f0ce6-112">代码块将永远不会重叠，它们将遵循 [ICorDebugCode：： GetCode](icordebugcode-getcode-method.md)连接的顺序。</span><span class="sxs-lookup"><span data-stu-id="f0ce6-112">The code chunks will never overlap, and they will follow the order in which they would have been concatenated by [ICorDebugCode::GetCode](icordebugcode-getcode-method.md).</span></span> <span data-ttu-id="f0ce6-113">.NET Framework 版本2.0 中的 Microsoft 中间语言 (MSIL) code 对象将包含一个代码块。</span><span class="sxs-lookup"><span data-stu-id="f0ce6-113">A Microsoft intermediate language (MSIL) code object in the .NET Framework version 2.0 will comprise a single code chunk.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ce6-114">要求</span><span class="sxs-lookup"><span data-stu-id="f0ce6-114">Requirements</span></span>

<span data-ttu-id="f0ce6-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f0ce6-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="f0ce6-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f0ce6-116">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="f0ce6-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f0ce6-117">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="f0ce6-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0ce6-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
