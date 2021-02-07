---
description: 了解详细信息： ICorDebugArrayValue：： GetDimensions 方法
title: ICorDebugArrayValue::GetDimensions 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetDimensions
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetDimensions
helpviewer_keywords:
- ICorDebugArrayValue::GetDimensions method [.NET Framework debugging]
- GetDimensions method [.NET Framework debugging]
ms.assetid: 6c116592-134b-4ef2-a319-680e92d013aa
topic_type:
- apiref
ms.openlocfilehash: 007a48891a01e5779e3f9ef10cec720d6647c8f3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723096"
---
# <a name="icordebugarrayvaluegetdimensions-method"></a><span data-ttu-id="d23fc-103">ICorDebugArrayValue::GetDimensions 方法</span><span class="sxs-lookup"><span data-stu-id="d23fc-103">ICorDebugArrayValue::GetDimensions Method</span></span>

<span data-ttu-id="d23fc-104">获取此数组的每个维度中的元素数。</span><span class="sxs-lookup"><span data-stu-id="d23fc-104">Gets the number of elements in each dimension of this array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d23fc-105">语法</span><span class="sxs-lookup"><span data-stu-id="d23fc-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDimensions (  
    [in] ULONG32         cdim,  
    [out, size_is(cdim), length_is(cdim)]
        ULONG32          dims[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d23fc-106">参数</span><span class="sxs-lookup"><span data-stu-id="d23fc-106">Parameters</span></span>  

 `cdim`  
 <span data-ttu-id="d23fc-107">中此 ICorDebugArrayValue 对象的维度数。</span><span class="sxs-lookup"><span data-stu-id="d23fc-107">[in] The number of dimensions of this ICorDebugArrayValue object.</span></span>  
  
 <span data-ttu-id="d23fc-108">此值也是数组的大小， `dims` 因为其大小等于对象的维度数 `ICorDebugArrayValue` 。</span><span class="sxs-lookup"><span data-stu-id="d23fc-108">This value is also the size of the `dims` array because its size is equal to the number of dimensions of the `ICorDebugArrayValue` object.</span></span>  
  
 `dims`  
 <span data-ttu-id="d23fc-109">弄一个整数数组，其中每个整数指定了此对象的维度中的元素数目 `ICorDebugArrayValue` 。</span><span class="sxs-lookup"><span data-stu-id="d23fc-109">[out] An array of integers, each of which specifies the number of elements in a dimension in this `ICorDebugArrayValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d23fc-110">要求</span><span class="sxs-lookup"><span data-stu-id="d23fc-110">Requirements</span></span>  

 <span data-ttu-id="d23fc-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d23fc-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d23fc-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d23fc-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d23fc-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d23fc-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d23fc-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d23fc-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
