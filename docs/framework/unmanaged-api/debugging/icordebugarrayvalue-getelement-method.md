---
description: 了解详细信息： ICorDebugArrayValue：： GetElement 方法
title: ICorDebugArrayValue::GetElement 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetElement
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetElement
helpviewer_keywords:
- GetElement method [.NET Framework debugging]
- ICorDebugArrayValue::GetElement method [.NET Framework debugging]
ms.assetid: 7ac3cba5-c282-402e-b7ef-b46634f5176b
topic_type:
- apiref
ms.openlocfilehash: dfae074b78735934d1e71b13ce01c24741a5f2ed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723057"
---
# <a name="icordebugarrayvaluegetelement-method"></a><span data-ttu-id="9233f-103">ICorDebugArrayValue::GetElement 方法</span><span class="sxs-lookup"><span data-stu-id="9233f-103">ICorDebugArrayValue::GetElement Method</span></span>

<span data-ttu-id="9233f-104">获取给定数组元素的值。</span><span class="sxs-lookup"><span data-stu-id="9233f-104">Gets the value of the given array element.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9233f-105">语法</span><span class="sxs-lookup"><span data-stu-id="9233f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetElement (  
    [in]  ULONG32          cdim,  
    [in, size_is(cdim), length_is(cdim)]
         ULONG32           indices[],  
    [out] ICorDebugValue   **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9233f-106">参数</span><span class="sxs-lookup"><span data-stu-id="9233f-106">Parameters</span></span>  

 `cdim`  
 <span data-ttu-id="9233f-107">中此对象的维度数 `ICorDebugArrayValue` 。</span><span class="sxs-lookup"><span data-stu-id="9233f-107">[in] The number of dimensions of this `ICorDebugArrayValue` object.</span></span>  
  
 <span data-ttu-id="9233f-108">此值也是数组的大小， `indices` 因为其大小等于对象的维度数 `ICorDebugArrayValue` 。</span><span class="sxs-lookup"><span data-stu-id="9233f-108">This value is also the size of the `indices` array because its size is equal to the number of dimensions of the `ICorDebugArrayValue` object.</span></span>  
  
 `indices`  
 <span data-ttu-id="9233f-109">中索引值的数组，其中每个值指定对象的维度内的位置 `ICorDebugArrayValue` 。</span><span class="sxs-lookup"><span data-stu-id="9233f-109">[in] An array of index values, each of which specifies a position within a dimension of the `ICorDebugArrayValue` object.</span></span>  
  
 <span data-ttu-id="9233f-110">此值不得为 Null。</span><span class="sxs-lookup"><span data-stu-id="9233f-110">This value must not be null.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="9233f-111">弄指向 ICorDebugValue 对象的地址的指针，该对象表示指定元素的值。</span><span class="sxs-lookup"><span data-stu-id="9233f-111">[out] A pointer to the address of an ICorDebugValue object that represents the value of the specified element.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9233f-112">要求</span><span class="sxs-lookup"><span data-stu-id="9233f-112">Requirements</span></span>  

 <span data-ttu-id="9233f-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9233f-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9233f-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9233f-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9233f-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9233f-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9233f-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9233f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
