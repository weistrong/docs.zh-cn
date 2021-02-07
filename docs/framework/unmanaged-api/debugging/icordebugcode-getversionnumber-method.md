---
description: 了解详细信息： ICorDebugCode：： GetVersionNumber 方法
title: ICorDebugCode::GetVersionNumber 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetVersionNumber
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetVersionNumber
helpviewer_keywords:
- GetVersionNumber method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetVersionNumber method [.NET Framework debugging]
ms.assetid: c8e02518-679f-4e9f-8a28-ba4a89a3876f
topic_type:
- apiref
ms.openlocfilehash: 901342333bea3d455407602dde78bdccd0140d77
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764900"
---
# <a name="icordebugcodegetversionnumber-method"></a><span data-ttu-id="94133-103">ICorDebugCode::GetVersionNumber 方法</span><span class="sxs-lookup"><span data-stu-id="94133-103">ICorDebugCode::GetVersionNumber Method</span></span>

<span data-ttu-id="94133-104">获取一个从1开始的数字，该数字标识此 "ICorDebugCode" 表示的代码版本。</span><span class="sxs-lookup"><span data-stu-id="94133-104">Gets the one-based number that identifies the version of the code that this "ICorDebugCode" represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="94133-105">语法</span><span class="sxs-lookup"><span data-stu-id="94133-105">Syntax</span></span>

```cpp
HRESULT GetVersionNumber (
    [out] ULONG32    *nVersion
);
```

## <a name="parameters"></a><span data-ttu-id="94133-106">参数</span><span class="sxs-lookup"><span data-stu-id="94133-106">Parameters</span></span>

 `nVersion`  
 <span data-ttu-id="94133-107">弄指向代码版本号的指针。</span><span class="sxs-lookup"><span data-stu-id="94133-107">[out] A pointer to the version number of the code.</span></span>

## <a name="remarks"></a><span data-ttu-id="94133-108">备注</span><span class="sxs-lookup"><span data-stu-id="94133-108">Remarks</span></span>

 <span data-ttu-id="94133-109">每次对代码执行 "编辑并继续" (EnC) 操作时，版本号将递增。</span><span class="sxs-lookup"><span data-stu-id="94133-109">The version number is incremented each time an edit-and-continue (EnC) operation is performed on the code.</span></span>

## <a name="requirements"></a><span data-ttu-id="94133-110">要求</span><span class="sxs-lookup"><span data-stu-id="94133-110">Requirements</span></span>

 <span data-ttu-id="94133-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="94133-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="94133-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="94133-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="94133-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="94133-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="94133-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="94133-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
