---
description: 了解详细信息： ICorDebugArrayValue：： GetCount 方法
title: ICorDebugArrayValue::GetCount 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetCount
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetCount
helpviewer_keywords:
- ICorDebugArrayValue::GetCount method [.NET Framework debugging]
- GetCount method, ICorDebugArrayValue interface [.NET Framework debugging]
ms.assetid: 44cd98cf-2127-4d46-8c6a-da4e857bb6b0
topic_type:
- apiref
ms.openlocfilehash: 7b1422714ed9c6f89c65c310165b8cdaa6566360
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723109"
---
# <a name="icordebugarrayvaluegetcount-method"></a><span data-ttu-id="107d4-103">ICorDebugArrayValue::GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="107d4-103">ICorDebugArrayValue::GetCount Method</span></span>

<span data-ttu-id="107d4-104">获取数组中的元素总数。</span><span class="sxs-lookup"><span data-stu-id="107d4-104">Gets the total number of elements in the array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="107d4-105">语法</span><span class="sxs-lookup"><span data-stu-id="107d4-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCount (  
    [out] ULONG32 *pnCount  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="107d4-106">参数</span><span class="sxs-lookup"><span data-stu-id="107d4-106">Parameters</span></span>  

 `pnCount`  
 <span data-ttu-id="107d4-107">弄指向数组中元素总数的指针。</span><span class="sxs-lookup"><span data-stu-id="107d4-107">[out] A pointer to the total number of elements in the array.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="107d4-108">要求</span><span class="sxs-lookup"><span data-stu-id="107d4-108">Requirements</span></span>  

 <span data-ttu-id="107d4-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="107d4-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="107d4-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="107d4-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="107d4-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="107d4-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="107d4-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="107d4-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
