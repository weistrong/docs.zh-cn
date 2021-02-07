---
description: 了解详细信息： ICorDebugModule2：： ResolveAssembly 方法
title: ICorDebugModule2::ResolveAssembly 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule2.ResolveAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2::ResolveAssembly
helpviewer_keywords:
- ICorDebugModule2::ResolveAssembly method [.NET Framework debugging]
- ResolveAssembly method [.NET Framework debugging]
ms.assetid: ddf9085c-7161-44bd-9609-cd2732b9009f
topic_type:
- apiref
ms.openlocfilehash: fba53b8ff76e4d3deb1876d2a20a7a2edc20bd06
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722589"
---
# <a name="icordebugmodule2resolveassembly-method"></a><span data-ttu-id="dac3a-103">ICorDebugModule2::ResolveAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="dac3a-103">ICorDebugModule2::ResolveAssembly Method</span></span>

<span data-ttu-id="dac3a-104">解析指定的元数据标记所引用的程序集。</span><span class="sxs-lookup"><span data-stu-id="dac3a-104">Resolves the assembly referenced by the specified metadata token.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac3a-105">语法</span><span class="sxs-lookup"><span data-stu-id="dac3a-105">Syntax</span></span>

```cpp
HRESULT ResolveAssembly (
    [in]  mdToken             tkAssemblyRef,
    [out] ICorDebugAssembly   **ppAssembly
);
```

## <a name="parameters"></a><span data-ttu-id="dac3a-106">参数</span><span class="sxs-lookup"><span data-stu-id="dac3a-106">Parameters</span></span>

`tkAssemblyRef`\
<span data-ttu-id="dac3a-107">中一个 `mdToken` 引用程序集的值。</span><span class="sxs-lookup"><span data-stu-id="dac3a-107">[in] An `mdToken` value that references the assembly.</span></span>

`ppAssembly`\
<span data-ttu-id="dac3a-108">弄指向表示程序集的 ICorDebugAssembly 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="dac3a-108">[out] A pointer to the address of an ICorDebugAssembly object that represents the assembly.</span></span>

## <a name="remarks"></a><span data-ttu-id="dac3a-109">备注</span><span class="sxs-lookup"><span data-stu-id="dac3a-109">Remarks</span></span>

<span data-ttu-id="dac3a-110">如果在调用时尚未加载该程序集 `ResolveAssembly` ，则将返回 CORDBG_E_CANNOT_RESOLVE_ASSEMBLY 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="dac3a-110">If the assembly is not already loaded when `ResolveAssembly` is called, an HRESULT value of CORDBG_E_CANNOT_RESOLVE_ASSEMBLY is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="dac3a-111">要求</span><span class="sxs-lookup"><span data-stu-id="dac3a-111">Requirements</span></span>

<span data-ttu-id="dac3a-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dac3a-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="dac3a-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="dac3a-113">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="dac3a-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dac3a-114">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="dac3a-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dac3a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
