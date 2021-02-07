---
description: 了解详细信息： ICorDebugClass2：： GetParameterizedType 方法
title: ICorDebugClass2::GetParameterizedType 方法
ms.date: 03/30/2017
api_name:
- ICorDebugClass2.GetParameterizedType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass2::GetParameterizedType
helpviewer_keywords:
- GetParameterizedType method [.NET Framework debugging]
- ICorDebugClass2::GetParameterizedType method [.NET Framework debugging]
ms.assetid: 94b591c4-9302-4af2-a510-089496afb036
topic_type:
- apiref
ms.openlocfilehash: 4810e10e88af9256a466579ee607c0ef314d984b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99765017"
---
# <a name="icordebugclass2getparameterizedtype-method"></a><span data-ttu-id="10bfd-103">ICorDebugClass2::GetParameterizedType 方法</span><span class="sxs-lookup"><span data-stu-id="10bfd-103">ICorDebugClass2::GetParameterizedType Method</span></span>

<span data-ttu-id="10bfd-104">获取此类的类型声明。</span><span class="sxs-lookup"><span data-stu-id="10bfd-104">Gets the type declaration for this class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="10bfd-105">语法</span><span class="sxs-lookup"><span data-stu-id="10bfd-105">Syntax</span></span>  
  
```cpp  
HRESULT GetParameterizedType (  
    [in] CorElementType                      elementType,  
    [in] ULONG32                             nTypeArgs,  
    [in, size_is(nTypeArgs)] ICorDebugType  *ppTypeArgs[],  
    [out] ICorDebugType                    **ppType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="10bfd-106">参数</span><span class="sxs-lookup"><span data-stu-id="10bfd-106">Parameters</span></span>  

 `elementType`  
 <span data-ttu-id="10bfd-107">中为此类指定元素类型的 CorElementType 枚举的值：如果此 ICorDebugClass2 表示值类型，请将此值设置为 ELEMENT_TYPE_VALUETYPE。</span><span class="sxs-lookup"><span data-stu-id="10bfd-107">[in] A value of the CorElementType enumeration that specifies the element type for this class: Set this value to ELEMENT_TYPE_VALUETYPE if this ICorDebugClass2 represents a value type.</span></span> <span data-ttu-id="10bfd-108">如果此表示复杂类型，则将此值设置为 ELEMENT_TYPE_CLASS `ICorDebugClass2` 。</span><span class="sxs-lookup"><span data-stu-id="10bfd-108">Set this value to ELEMENT_TYPE_CLASS if this `ICorDebugClass2` represents a complex type.</span></span>  
  
 `nTypeArgs`  
 <span data-ttu-id="10bfd-109">中如果类型为泛型，则为类型参数的数目。</span><span class="sxs-lookup"><span data-stu-id="10bfd-109">[in] The number of type parameters, if the type is generic.</span></span> <span data-ttu-id="10bfd-110">如果任何) 必须与类所需的数目相匹配，则 (类型参数的数目。</span><span class="sxs-lookup"><span data-stu-id="10bfd-110">The number of type parameters (if any) must match the number required by the class.</span></span>  
  
 `ppTypeArgs`  
 <span data-ttu-id="10bfd-111">中指针的数组，其中每个都指向表示类型参数的 ICorDebugType 对象。</span><span class="sxs-lookup"><span data-stu-id="10bfd-111">[in] An array of pointers, each of which points to an ICorDebugType object that represents a type parameter.</span></span> <span data-ttu-id="10bfd-112">如果类为非泛型类，则此值为 null。</span><span class="sxs-lookup"><span data-stu-id="10bfd-112">If the class is non-generic, this value is null.</span></span>  
  
 `ppType`  
 <span data-ttu-id="10bfd-113">弄指向表示类型声明的对象的地址的指针 `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="10bfd-113">[out] A pointer to the address of an `ICorDebugType` object that represents the type declaration.</span></span> <span data-ttu-id="10bfd-114">此对象等效于 <xref:System.Type> 托管代码中的对象。</span><span class="sxs-lookup"><span data-stu-id="10bfd-114">This object is equivalent to a <xref:System.Type> object in managed code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="10bfd-115">备注</span><span class="sxs-lookup"><span data-stu-id="10bfd-115">Remarks</span></span>  

 <span data-ttu-id="10bfd-116">如果类是非泛型类（即，如果它没有类型参数）， `GetParameterizedType` 只需获取与类相对应的运行时类型对象。</span><span class="sxs-lookup"><span data-stu-id="10bfd-116">If the class is non-generic, that is, if it has no type parameters, `GetParameterizedType` simply gets the runtime type object corresponding to the class.</span></span> <span data-ttu-id="10bfd-117">`elementType`如果类是值类型，则应将参数设置为类的正确元素类型： ELEMENT_TYPE_VALUETYPE; 否则 ELEMENT_TYPE_CLASS。</span><span class="sxs-lookup"><span data-stu-id="10bfd-117">The `elementType` parameter should be set to the correct element type for the class: ELEMENT_TYPE_VALUETYPE if the class is a value type; otherwise, ELEMENT_TYPE_CLASS.</span></span>  
  
 <span data-ttu-id="10bfd-118">如果类接受类型参数 (例如 `ArrayList<T>`) ，则可以使用 `GetParameterizedType` 为实例化的类型（如）构造类型对象 `ArrayList<int>` 。</span><span class="sxs-lookup"><span data-stu-id="10bfd-118">If the class accepts type parameters (for example, `ArrayList<T>`), you can use `GetParameterizedType` to construct a type object for an instantiated type such as `ArrayList<int>`.</span></span>  
  
## <a name="background-information"></a><span data-ttu-id="10bfd-119">背景信息</span><span class="sxs-lookup"><span data-stu-id="10bfd-119">Background Information</span></span>  

 <span data-ttu-id="10bfd-120">在 .NET Framework 版本1.0 和1.1 中，元数据中的每个类型都可以直接映射到正在运行的进程中的类型。</span><span class="sxs-lookup"><span data-stu-id="10bfd-120">In the .NET Framework versions 1.0 and 1.1, every type in the metadata could be directly mapped to a type in the running process.</span></span> <span data-ttu-id="10bfd-121">因此，元数据类型和运行时类型在正在运行的进程中具有单个表示形式。</span><span class="sxs-lookup"><span data-stu-id="10bfd-121">Thus, a metadata type and a runtime type had a single representation in the running process.</span></span> <span data-ttu-id="10bfd-122">但是，元数据中的一种泛型类型可以映射到正在运行的进程中类型的许多不同的实例化。</span><span class="sxs-lookup"><span data-stu-id="10bfd-122">However, one generic type in metadata can be mapped to many different instantiations of the type in the running process.</span></span> <span data-ttu-id="10bfd-123">例如，元数据类型 `SortedList<K,V>` 可以映射到、、等 `SortedList<String, EmployeeRecord>` `SortedList<Int32, String>` `SortedList<String,Array<Int32>>` 。</span><span class="sxs-lookup"><span data-stu-id="10bfd-123">For example, the metadata type `SortedList<K,V>` can map to `SortedList<String, EmployeeRecord>`, `SortedList<Int32, String>`, `SortedList<String,Array<Int32>>`, and so on.</span></span> <span data-ttu-id="10bfd-124">因此，您需要一种方法来处理类型实例化。</span><span class="sxs-lookup"><span data-stu-id="10bfd-124">Thus, you need a way to handle type instantiation.</span></span>  
  
 <span data-ttu-id="10bfd-125">.NET Framework 版本2.0 引入了 `ICorDebugType` 接口。</span><span class="sxs-lookup"><span data-stu-id="10bfd-125">The .NET Framework version 2.0 introduces the `ICorDebugType` interface.</span></span> <span data-ttu-id="10bfd-126">对于泛型类型， `ICorDebugClass` 或 `ICorDebugClass2` 对象表示未实例化的类型 (`SortedList<K,V>`) ，而 `ICorDebugType` 对象表示各种实例化的类型。</span><span class="sxs-lookup"><span data-stu-id="10bfd-126">For a generic type, an `ICorDebugClass` or `ICorDebugClass2` object represents the uninstantiated type (`SortedList<K,V>`), and an `ICorDebugType` object represents the various instantiated types.</span></span> <span data-ttu-id="10bfd-127">给定 `ICorDebugClass` 或 `ICorDebugClass2` 对象，可以 `ICorDebugType` 通过调用方法为任何实例化创建对象 `ICorDebugClass2::GetParameterizedType` 。</span><span class="sxs-lookup"><span data-stu-id="10bfd-127">Given an `ICorDebugClass` or `ICorDebugClass2` object, you can create an `ICorDebugType` object for any instantiation by calling the `ICorDebugClass2::GetParameterizedType` method.</span></span> <span data-ttu-id="10bfd-128">还可以为 `ICorDebugType` 简单类型（如 Int32）或非泛型类型创建对象。</span><span class="sxs-lookup"><span data-stu-id="10bfd-128">You can also create an `ICorDebugType` object for a simple type, such as Int32, or for a non-generic type.</span></span>  
  
 <span data-ttu-id="10bfd-129">引入 `ICorDebugType` 对象来表示类型的运行时概念会在整个 API 中产生波纹效果。</span><span class="sxs-lookup"><span data-stu-id="10bfd-129">The introduction of the `ICorDebugType` object to represent the run-time notion of a type has a ripple effect throughout the API.</span></span> <span data-ttu-id="10bfd-130">以前用过 `ICorDebugClass` 或 `ICorDebugClass2` 对象甚至值的函数 `CorElementType` 被通用化为采用 `ICorDebugType` 对象。</span><span class="sxs-lookup"><span data-stu-id="10bfd-130">Functions that previously took an `ICorDebugClass` or `ICorDebugClass2` object or even a `CorElementType` value are generalized to take an `ICorDebugType` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="10bfd-131">要求</span><span class="sxs-lookup"><span data-stu-id="10bfd-131">Requirements</span></span>  

 <span data-ttu-id="10bfd-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="10bfd-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="10bfd-133">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="10bfd-133">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="10bfd-134">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="10bfd-134">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="10bfd-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="10bfd-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
