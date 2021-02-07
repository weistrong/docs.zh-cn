---
description: 了解详细信息： ICorDebugArrayValue：： GetElementType 方法
title: ICorDebugArrayValue::GetElementType 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetElementType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetElementType
helpviewer_keywords:
- ICorDebugArrayValue::GetElementType method [.NET Framework debugging]
- GetElementType method [.NET Framework debugging]
ms.assetid: ed71961e-ae9b-4dfc-9554-06637696d697
topic_type:
- apiref
ms.openlocfilehash: 97c01a9c8ae7a1d73a1a15b97d3ce3e9aa079365
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723018"
---
# <a name="icordebugarrayvaluegetelementtype-method"></a><span data-ttu-id="2a36b-103">ICorDebugArrayValue::GetElementType 方法</span><span class="sxs-lookup"><span data-stu-id="2a36b-103">ICorDebugArrayValue::GetElementType Method</span></span>

<span data-ttu-id="2a36b-104">获取一个值，该值指示数组中元素的简单类型。</span><span class="sxs-lookup"><span data-stu-id="2a36b-104">Gets a value that indicates the simple type of the elements in the array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a36b-105">语法</span><span class="sxs-lookup"><span data-stu-id="2a36b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetElementType (  
    [out] CorElementType  *pType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2a36b-106">参数</span><span class="sxs-lookup"><span data-stu-id="2a36b-106">Parameters</span></span>  

 `pType`  
 <span data-ttu-id="2a36b-107">弄一个指针，指向指示类型的 CorElementType 枚举的值。</span><span class="sxs-lookup"><span data-stu-id="2a36b-107">[out] A pointer to a value of the CorElementType enumeration that indicates the type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2a36b-108">要求</span><span class="sxs-lookup"><span data-stu-id="2a36b-108">Requirements</span></span>  

 <span data-ttu-id="2a36b-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2a36b-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2a36b-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2a36b-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2a36b-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2a36b-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2a36b-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2a36b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
