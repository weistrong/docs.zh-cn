---
description: 了解详细信息： ICorDebugStringValue：： GetString 方法
title: ICorDebugStringValue::GetString 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStringValue.GetString
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStringValue::GetString
helpviewer_keywords:
- ICorDebugStringValue::GetString method [.NET Framework debugging]
- GetString method, ICorDebugStringValue interface [.NET Framework debugging]
ms.assetid: 2b94bda7-09ee-435d-91b9-c4e31af1896c
topic_type:
- apiref
ms.openlocfilehash: 06e8e039c8b0afb7753a398302a9b32eb3ba7213
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717335"
---
# <a name="icordebugstringvaluegetstring-method"></a><span data-ttu-id="d5db3-103">ICorDebugStringValue::GetString 方法</span><span class="sxs-lookup"><span data-stu-id="d5db3-103">ICorDebugStringValue::GetString Method</span></span>

<span data-ttu-id="d5db3-104">获取此 ICorDebugStringValue 引用的字符串。</span><span class="sxs-lookup"><span data-stu-id="d5db3-104">Gets the string referenced by this ICorDebugStringValue.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5db3-105">语法</span><span class="sxs-lookup"><span data-stu-id="d5db3-105">Syntax</span></span>  
  
```cpp  
HRESULT GetString (  
    [in] ULONG32    cchString,  
    [out] ULONG32   *pcchString,  
    [out, size_is(cchString), length_is(*pcchString)]
        WCHAR       szString[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d5db3-106">参数</span><span class="sxs-lookup"><span data-stu-id="d5db3-106">Parameters</span></span>  

 `cchString`  
 <span data-ttu-id="d5db3-107">[in] `szString` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="d5db3-107">[in] The size of the `szString` array.</span></span>  
  
 `pcchString`  
 <span data-ttu-id="d5db3-108">弄一个指针，指向数组中返回的字符数 `szString` 。</span><span class="sxs-lookup"><span data-stu-id="d5db3-108">[out] A pointer to the number of characters returned in the `szString` array.</span></span>  
  
 `szString`  
 <span data-ttu-id="d5db3-109">弄存储检索的字符串的数组。</span><span class="sxs-lookup"><span data-stu-id="d5db3-109">[out] An array that stores the retrieved string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d5db3-110">要求</span><span class="sxs-lookup"><span data-stu-id="d5db3-110">Requirements</span></span>  

 <span data-ttu-id="d5db3-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d5db3-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d5db3-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d5db3-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d5db3-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d5db3-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d5db3-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d5db3-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
