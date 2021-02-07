---
description: 了解详细信息： ICorDebugCode：： IsIL 方法
title: ICorDebugCode::IsIL 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.IsIL
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::IsIL
helpviewer_keywords:
- ICorDebugCode::IsIL method [.NET Framework debugging]
- IsIL method [.NET Framework debugging]
ms.assetid: 132ef8cc-d938-43f3-b8f2-e3b97c0ceb33
topic_type:
- apiref
ms.openlocfilehash: db41f9ebaa6a6403b21e10d1daa0e8b167c7cb96
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711117"
---
# <a name="icordebugcodeisil-method"></a><span data-ttu-id="6e7b4-103">ICorDebugCode::IsIL 方法</span><span class="sxs-lookup"><span data-stu-id="6e7b4-103">ICorDebugCode::IsIL Method</span></span>

<span data-ttu-id="6e7b4-104">获取一个值，该值指示此 "ICorDebugCode" 是否表示使用 Microsoft 中间语言 (MSIL) 编译的代码。</span><span class="sxs-lookup"><span data-stu-id="6e7b4-104">Gets a value that indicates whether this "ICorDebugCode" represents code that was compiled in Microsoft intermediate language (MSIL).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e7b4-105">语法</span><span class="sxs-lookup"><span data-stu-id="6e7b4-105">Syntax</span></span>

```cpp
HRESULT IsIL (
    [out] BOOL       *pbIL
);
```

## <a name="parameters"></a><span data-ttu-id="6e7b4-106">参数</span><span class="sxs-lookup"><span data-stu-id="6e7b4-106">Parameters</span></span>

`pbIL`  
<span data-ttu-id="6e7b4-107">[out] `true` 如果这 `ICorDebugCode` 表示在 MSIL 中编译的代码，则为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="6e7b4-107">[out] `true` if this `ICorDebugCode` represents code that was compiled in MSIL; otherwise, `false`.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e7b4-108">要求</span><span class="sxs-lookup"><span data-stu-id="6e7b4-108">Requirements</span></span>

<span data-ttu-id="6e7b4-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6e7b4-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="6e7b4-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6e7b4-110">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="6e7b4-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6e7b4-111">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="6e7b4-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6e7b4-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
