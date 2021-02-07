---
description: 了解详细信息： ICorDebugCode：： GetSize 方法
title: ICorDebugCode::GetSize 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetSize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetSize
helpviewer_keywords:
- GetSize method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetSize method [.NET Framework debugging]
ms.assetid: 115bc6de-f5e2-4e8e-bb38-c7cf54045434
topic_type:
- apiref
ms.openlocfilehash: 5a244d649cdcf027aea22ab36ff5d39a77a05e1c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711175"
---
# <a name="icordebugcodegetsize-method"></a><span data-ttu-id="8df93-103">ICorDebugCode::GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="8df93-103">ICorDebugCode::GetSize Method</span></span>

<span data-ttu-id="8df93-104">获取此 "ICorDebugCode" 表示的二进制代码的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="8df93-104">Gets the size, in bytes, of the binary code represented by this "ICorDebugCode".</span></span>

## <a name="syntax"></a><span data-ttu-id="8df93-105">语法</span><span class="sxs-lookup"><span data-stu-id="8df93-105">Syntax</span></span>

```cpp
HRESULT GetSize (
    [out] ULONG32    *pcBytes
);
```

## <a name="parameters"></a><span data-ttu-id="8df93-106">参数</span><span class="sxs-lookup"><span data-stu-id="8df93-106">Parameters</span></span>

`pcBytes`  
<span data-ttu-id="8df93-107">弄一个指针，指向此对象表示的二进制代码的大小（以字节为单位） `ICorDebugCode` 。</span><span class="sxs-lookup"><span data-stu-id="8df93-107">[out] A pointer to the size, in bytes, of the binary code that this `ICorDebugCode` object represents.</span></span>

## <a name="requirements"></a><span data-ttu-id="8df93-108">要求</span><span class="sxs-lookup"><span data-stu-id="8df93-108">Requirements</span></span>

<span data-ttu-id="8df93-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8df93-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="8df93-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8df93-110">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="8df93-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8df93-111">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="8df93-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8df93-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
