---
description: 了解详细信息： ICorDebugVariableHome：： GetArgumentIndex 方法
title: ICorDebugVariableHome：： GetArgumentIndex 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetArgumentIndex
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetArgumentIndex
helpviewer_keywords:
- ICorDebugVariableHome::GetArgumentIndex method [.NET Framework debugging]
- GetArgumentIndex method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: e86fcc72-388d-4009-ab21-8f9c3323e9a3
topic_type:
- apiref
ms.openlocfilehash: 827ef55d3e3509cbfbfc8213ef5b53fbe2e2220e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690036"
---
# <a name="icordebugvariablehomegetargumentindex-method"></a><span data-ttu-id="cdce8-103">ICorDebugVariableHome：： GetArgumentIndex 方法</span><span class="sxs-lookup"><span data-stu-id="cdce8-103">ICorDebugVariableHome::GetArgumentIndex Method</span></span>

<span data-ttu-id="cdce8-104">获取函数参数的索引。</span><span class="sxs-lookup"><span data-stu-id="cdce8-104">Gets the index of a function argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdce8-105">语法</span><span class="sxs-lookup"><span data-stu-id="cdce8-105">Syntax</span></span>

```cpp
HRESULT GetArgumentIndex(
    [out] ULONG32* pArgumentIndex
);
```

## <a name="parameters"></a><span data-ttu-id="cdce8-106">参数</span><span class="sxs-lookup"><span data-stu-id="cdce8-106">Parameters</span></span>

`pArgumentIndex`\
<span data-ttu-id="cdce8-107">弄指向参数索引的指针。</span><span class="sxs-lookup"><span data-stu-id="cdce8-107">[out] A pointer to the argument index.</span></span>

## <a name="return-value"></a><span data-ttu-id="cdce8-108">返回值</span><span class="sxs-lookup"><span data-stu-id="cdce8-108">Return Value</span></span>

<span data-ttu-id="cdce8-109">方法返回以下值。</span><span class="sxs-lookup"><span data-stu-id="cdce8-109">The method returns the following values.</span></span>

|<span data-ttu-id="cdce8-110">值</span><span class="sxs-lookup"><span data-stu-id="cdce8-110">Value</span></span>|<span data-ttu-id="cdce8-111">说明</span><span class="sxs-lookup"><span data-stu-id="cdce8-111">Description</span></span>|
|-----------|-----------------|
|`S_OK`|<span data-ttu-id="cdce8-112">方法调用返回有效的参数索引。</span><span class="sxs-lookup"><span data-stu-id="cdce8-112">The method call returned a valid argument index.</span></span>|
|`E_FAIL`|<span data-ttu-id="cdce8-113">当前 [ICorDebugVariableHome](icordebugvariablehome-interface.md) 实例表示局部变量。</span><span class="sxs-lookup"><span data-stu-id="cdce8-113">The current [ICorDebugVariableHome](icordebugvariablehome-interface.md) instance represents a local variable.</span></span>|

## <a name="remarks"></a><span data-ttu-id="cdce8-114">备注</span><span class="sxs-lookup"><span data-stu-id="cdce8-114">Remarks</span></span>

<span data-ttu-id="cdce8-115">参数索引可用于检索此参数的元数据。</span><span class="sxs-lookup"><span data-stu-id="cdce8-115">The argument index can be used to retrieve metadata for this argument.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdce8-116">要求</span><span class="sxs-lookup"><span data-stu-id="cdce8-116">Requirements</span></span>

<span data-ttu-id="cdce8-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cdce8-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="cdce8-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cdce8-118">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="cdce8-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cdce8-119">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="cdce8-120">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cdce8-120">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="cdce8-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="cdce8-121">See also</span></span>

- [<span data-ttu-id="cdce8-122">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="cdce8-122">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
