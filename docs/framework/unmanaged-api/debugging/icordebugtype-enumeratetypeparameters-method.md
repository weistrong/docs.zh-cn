---
description: 了解详细信息： ICorDebugType：： EnumerateTypeParameters 方法
title: ICorDebugType::EnumerateTypeParameters 方法
ms.date: 03/30/2017
api_name:
- ICorDebugType.EnumerateTypeParameters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::EnumerateTypeParameters
helpviewer_keywords:
- EnumerateTypeParameters method, ICorDebugType interface [.NET Framework debugging]
- ICorDebugType::EnumerateTypeParameters method [.NET Framework debugging]
ms.assetid: 1ee1f6e6-1bd7-4ebb-83b8-ff9a08ca03de
topic_type:
- apiref
ms.openlocfilehash: 5189394cbb39cd133ebce494107f4ca65660bb5b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658407"
---
# <a name="icordebugtypeenumeratetypeparameters-method"></a><span data-ttu-id="e8418-103">ICorDebugType::EnumerateTypeParameters 方法</span><span class="sxs-lookup"><span data-stu-id="e8418-103">ICorDebugType::EnumerateTypeParameters Method</span></span>

<span data-ttu-id="e8418-104">获取一个接口指针，该指针指向包含 <xref:System.Type> 此 ICorDebugType 引用的类的参数的 ICorDebugTypeEnum。</span><span class="sxs-lookup"><span data-stu-id="e8418-104">Gets an interface pointer to an ICorDebugTypeEnum that contains the <xref:System.Type> parameters of the class referenced by this ICorDebugType.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8418-105">语法</span><span class="sxs-lookup"><span data-stu-id="e8418-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateTypeParameters (  
    [out] ICorDebugTypeEnum   **ppTyParEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e8418-106">参数</span><span class="sxs-lookup"><span data-stu-id="e8418-106">Parameters</span></span>  

 `ppTyParEnum`  
 <span data-ttu-id="e8418-107">弄指向 `ICorDebugTypeEnum` 包含类型参数的的地址的指针。</span><span class="sxs-lookup"><span data-stu-id="e8418-107">[out] A pointer to the address of an `ICorDebugTypeEnum` that contains the parameters of the type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e8418-108">备注</span><span class="sxs-lookup"><span data-stu-id="e8418-108">Remarks</span></span>  

 <span data-ttu-id="e8418-109">`EnumerateTypeParameters`如果[ICorDebugType：： GetType](icordebugtype-gettype-method.md)返回的 CorElementType 值为 ELEMENT_TYPE_CLASS、ELEMENT_TYPE_VALUETYPE、ELEMENT_TYPE_ARRAY、ELEMENT_TYPE_SZARRAY、ELEMENT_TYPE_BYREF、ELEMENT_TYPE_PTR 或 ELEMENT_TYPE_FNPTR，则可以使用。</span><span class="sxs-lookup"><span data-stu-id="e8418-109">You can use `EnumerateTypeParameters` if the CorElementType value returned by [ICorDebugType::GetType](icordebugtype-gettype-method.md) is ELEMENT_TYPE_CLASS, ELEMENT_TYPE_VALUETYPE, ELEMENT_TYPE_ARRAY, ELEMENT_TYPE_SZARRAY, ELEMENT_TYPE_BYREF, ELEMENT_TYPE_PTR, or ELEMENT_TYPE_FNPTR.</span></span> <span data-ttu-id="e8418-110">参数的数量及其顺序取决于类型：</span><span class="sxs-lookup"><span data-stu-id="e8418-110">The number of parameters and their order depends on the type:</span></span>  
  
- <span data-ttu-id="e8418-111">ELEMENT_TYPE_CLASS 或 ELEMENT_TYPE_VALUETYPE：此方法返回的中包含的类型参数的数量 `ICorDebugTypeEnum` 将取决于相应类的形参数量。</span><span class="sxs-lookup"><span data-stu-id="e8418-111">ELEMENT_TYPE_CLASS or ELEMENT_TYPE_VALUETYPE: The number of type parameters contained in the `ICorDebugTypeEnum` that this method returns, will depend on the number of formal type parameters for the corresponding class.</span></span> <span data-ttu-id="e8418-112">例如，如果类型为 `class Dict<String,int32>` ，则 `EnumerateTypeParameters` 将返回， `ICorDebugTypeEnum` 其中包含 `String` 按顺序表示和的对象 `int32` 。</span><span class="sxs-lookup"><span data-stu-id="e8418-112">For example, if the type is `class Dict<String,int32>`, then `EnumerateTypeParameters` will return an `ICorDebugTypeEnum` that contains objects representing `String` and `int32` in sequence.</span></span>  
  
- <span data-ttu-id="e8418-113">ELEMENT_TYPE_FNPTR：中包含的类型参数的数量 `ICorDebugTypeEnum` 将大于函数接受的参数的数目。</span><span class="sxs-lookup"><span data-stu-id="e8418-113">ELEMENT_TYPE_FNPTR: The number of type parameters contained in the `ICorDebugTypeEnum` will be one greater than the number of arguments accepted by the function.</span></span> <span data-ttu-id="e8418-114">中包含的第一个类型参数 `ICorDebugTypeEnum` 是函数的返回类型，而后续类型参数是函数的参数。</span><span class="sxs-lookup"><span data-stu-id="e8418-114">The first type parameter contained in the `ICorDebugTypeEnum` is the return type for the function, and the subsequent type parameters are the function's parameters.</span></span>  
  
- <span data-ttu-id="e8418-115">ELEMENT_TYPE_ARRAY、ELEMENT_TYPE_SZARRAY、ELEMENT_TYPE_BYREF 或 ELEMENT_TYPE_PTR：将返回一个类型参数。</span><span class="sxs-lookup"><span data-stu-id="e8418-115">ELEMENT_TYPE_ARRAY, ELEMENT_TYPE_SZARRAY, ELEMENT_TYPE_BYREF, or ELEMENT_TYPE_PTR: One type parameter will be returned.</span></span> <span data-ttu-id="e8418-116">例如，如果类型是数组类型（如 `int32[]` ）， `EnumerateTypeParameters` 则将返回一个 `ICorDebugTypeEnum` ，它包含表示的对象 `int32` 。</span><span class="sxs-lookup"><span data-stu-id="e8418-116">For example, if the type is an array type such as `int32[]`,`EnumerateTypeParameters` will return an `ICorDebugTypeEnum` that contains an object representing `int32`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8418-117">要求</span><span class="sxs-lookup"><span data-stu-id="e8418-117">Requirements</span></span>  

 <span data-ttu-id="e8418-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e8418-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8418-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e8418-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e8418-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e8418-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e8418-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8418-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
