---
description: 了解详细信息： ICorDebugStringValue：： GetLength 方法
title: ICorDebugStringValue::GetLength 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStringValue.GetLength
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStringValue::GetLength
helpviewer_keywords:
- ICorDebugStringValue::GetLength method [.NET Framework debugging]
- GetLength method [.NET Framework debugging]
ms.assetid: a1ebfc69-46a6-4225-8788-b7cfb2f15e1d
topic_type:
- apiref
ms.openlocfilehash: ae4d42b5b65e5f80e884415a5acfc7f894ffe11e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717376"
---
# <a name="icordebugstringvaluegetlength-method"></a><span data-ttu-id="b69dc-103">ICorDebugStringValue::GetLength 方法</span><span class="sxs-lookup"><span data-stu-id="b69dc-103">ICorDebugStringValue::GetLength Method</span></span>

<span data-ttu-id="b69dc-104">获取此 ICorDebugStringValue 引用的字符串中的字符数。</span><span class="sxs-lookup"><span data-stu-id="b69dc-104">Gets the number of characters in the string referenced by this ICorDebugStringValue.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b69dc-105">语法</span><span class="sxs-lookup"><span data-stu-id="b69dc-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLength (  
    [out] ULONG32   *pcchString  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b69dc-106">参数</span><span class="sxs-lookup"><span data-stu-id="b69dc-106">Parameters</span></span>  

 `pcchString`  
 <span data-ttu-id="b69dc-107">弄一个指向值的指针，该值指定此对象所引用的字符串的长度 `ICorDebugStringValue` 。</span><span class="sxs-lookup"><span data-stu-id="b69dc-107">[out] A pointer to a value that specifies the length of the string referenced by this `ICorDebugStringValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b69dc-108">要求</span><span class="sxs-lookup"><span data-stu-id="b69dc-108">Requirements</span></span>  

 <span data-ttu-id="b69dc-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b69dc-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b69dc-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b69dc-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b69dc-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b69dc-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b69dc-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b69dc-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
