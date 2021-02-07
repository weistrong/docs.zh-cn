---
description: 了解详细信息： ICorDebugCode2：： GetCompilerFlags 方法
title: ICorDebugCode2::GetCompilerFlags 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode2.GetCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode2::GetCompilerFlags
helpviewer_keywords:
- GetCompilerFlags method [.NET Framework debugging]
- ICorDebugCode2::GetCompilerFlags method [.NET Framework debugging]
ms.assetid: 532e9dfd-d114-4c75-b952-1accce102643
topic_type:
- apiref
ms.openlocfilehash: 820b6d2392b2b91bbfc8a85b165c4d73a2546859
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711110"
---
# <a name="icordebugcode2getcompilerflags-method"></a><span data-ttu-id="28111-103">ICorDebugCode2::GetCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="28111-103">ICorDebugCode2::GetCompilerFlags Method</span></span>

<span data-ttu-id="28111-104">获取一些标志，这些标志指定此代码对象是实时 (JIT) 使用本机映像)  ( 生成器编译或生成的。</span><span class="sxs-lookup"><span data-stu-id="28111-104">Gets the flags that specify the conditions under which this code object was either just-in-time (JIT) compiled or generated using the native image generator (Ngen.exe).</span></span>

## <a name="syntax"></a><span data-ttu-id="28111-105">语法</span><span class="sxs-lookup"><span data-stu-id="28111-105">Syntax</span></span>

```cpp
HRESULT GetCompilerFlags (
    [out] DWORD *pdwFlags
);
```

## <a name="parameters"></a><span data-ttu-id="28111-106">参数</span><span class="sxs-lookup"><span data-stu-id="28111-106">Parameters</span></span>

`pdwFlags`  
<span data-ttu-id="28111-107">弄指向 [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) 枚举的值的指针，该枚举指定 JIT 编译器或本机图像生成器的行为。</span><span class="sxs-lookup"><span data-stu-id="28111-107">[out] A pointer to a value of the [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) enumeration that specifies the behavior of the JIT compiler or the native image generator.</span></span>

## <a name="requirements"></a><span data-ttu-id="28111-108">要求</span><span class="sxs-lookup"><span data-stu-id="28111-108">Requirements</span></span>

<span data-ttu-id="28111-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="28111-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="28111-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="28111-110">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="28111-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="28111-111">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="28111-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="28111-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
