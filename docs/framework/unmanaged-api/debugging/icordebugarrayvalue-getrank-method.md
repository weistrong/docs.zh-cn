---
description: 了解详细信息： ICorDebugArrayValue：： GetRank 方法
title: ICorDebugArrayValue::GetRank 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetRank
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetRank
helpviewer_keywords:
- ICorDebugArrayValue::GetRank method [.NET Framework debugging]
- GetRank method, ICorDebugArrayValue interface [.NET Framework debugging]
ms.assetid: 5e83c82c-593d-4691-90b0-383d218b415e
topic_type:
- apiref
ms.openlocfilehash: b84cc8fd49cbb7f7d4aa6fa7fa41b1c6cf8daf29
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722992"
---
# <a name="icordebugarrayvaluegetrank-method"></a><span data-ttu-id="2e8bf-103">ICorDebugArrayValue::GetRank 方法</span><span class="sxs-lookup"><span data-stu-id="2e8bf-103">ICorDebugArrayValue::GetRank Method</span></span>

<span data-ttu-id="2e8bf-104">获取数组中的维度数。</span><span class="sxs-lookup"><span data-stu-id="2e8bf-104">Gets the number of dimensions in the array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2e8bf-105">语法</span><span class="sxs-lookup"><span data-stu-id="2e8bf-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRank (  
    [out] ULONG32   *pnRank  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2e8bf-106">参数</span><span class="sxs-lookup"><span data-stu-id="2e8bf-106">Parameters</span></span>  

 `pnRank`  
 <span data-ttu-id="2e8bf-107">弄一个指针，指向该对象中的维度数 `ICorDebugArrayValue` 。</span><span class="sxs-lookup"><span data-stu-id="2e8bf-107">[out] A pointer to the number of dimensions in this `ICorDebugArrayValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2e8bf-108">要求</span><span class="sxs-lookup"><span data-stu-id="2e8bf-108">Requirements</span></span>  

 <span data-ttu-id="2e8bf-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2e8bf-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2e8bf-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2e8bf-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2e8bf-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2e8bf-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2e8bf-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2e8bf-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
