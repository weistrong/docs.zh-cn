---
description: 了解详细信息： ICorProfilerInfo2：： GetClassFromTokenAndTypeArgs 方法
title: ICorProfilerInfo2::GetClassFromTokenAndTypeArgs 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetClassFromTokenAndTypeArgs
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetClassFromTokenAndTypeArgs
helpviewer_keywords:
- GetClassFromTokenAndTypeArgs method [.NET Framework profiling]
- ICorProfilerInfo2::GetClassFromTokenAndTypeArgs method [.NET Framework profiling]
ms.assetid: b25c88f0-71b9-443b-8eea-1c94db0a44b9
topic_type:
- apiref
ms.openlocfilehash: 810445d2617beff55e00df6bb30130d81c740ba4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760457"
---
# <a name="icorprofilerinfo2getclassfromtokenandtypeargs-method"></a><span data-ttu-id="2abdc-103">ICorProfilerInfo2::GetClassFromTokenAndTypeArgs 方法</span><span class="sxs-lookup"><span data-stu-id="2abdc-103">ICorProfilerInfo2::GetClassFromTokenAndTypeArgs Method</span></span>

<span data-ttu-id="2abdc-104">`ClassID`使用指定的元数据标记和 `ClassID` 任何类型参数的值获取类型的。</span><span class="sxs-lookup"><span data-stu-id="2abdc-104">Gets the `ClassID` of a type by using the specified metadata token and the `ClassID` values of any type arguments.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2abdc-105">语法</span><span class="sxs-lookup"><span data-stu-id="2abdc-105">Syntax</span></span>  
  
```cpp  
HRESULT GetClassFromTokenAndTypeArgs(  
    [in] ModuleID moduleID,  
    [in] mdTypeDef typeDef,  
    [in] ULONG32 cTypeArgs,  
    [in, size_is(cTypeArgs)] ClassID typeArgs[],  
    [out] ClassID* pClassID);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2abdc-106">参数</span><span class="sxs-lookup"><span data-stu-id="2abdc-106">Parameters</span></span>  

 `moduleID`  
 <span data-ttu-id="2abdc-107">中类型所在的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="2abdc-107">[in] The ID of the module in which the type resides.</span></span>  
  
 `typeDef`  
 <span data-ttu-id="2abdc-108">中 `mdTypeDef` 引用类型的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="2abdc-108">[in] An `mdTypeDef` metadata token that references the type.</span></span>  
  
 `cTypeArgs`  
 <span data-ttu-id="2abdc-109">中给定类型的类型参数的数目。</span><span class="sxs-lookup"><span data-stu-id="2abdc-109">[in] The number of type parameters for the given type.</span></span> <span data-ttu-id="2abdc-110">对于非泛型类型，此值必须为零。</span><span class="sxs-lookup"><span data-stu-id="2abdc-110">This value must be zero for non-generic types.</span></span>  
  
 `typeArgs`  
 <span data-ttu-id="2abdc-111">中值的数组 `ClassID` ，其中每个值都是类型的参数。</span><span class="sxs-lookup"><span data-stu-id="2abdc-111">[in] An array of `ClassID` values, each of which is an argument of the type.</span></span> <span data-ttu-id="2abdc-112">如果设置为零，则的值 `typeArgs` 可以为 NULL `cTypeArgs` 。</span><span class="sxs-lookup"><span data-stu-id="2abdc-112">The value of `typeArgs` can be NULL if `cTypeArgs` is set to zero.</span></span>  
  
 `pClassID`  
 <span data-ttu-id="2abdc-113">弄指向指定类型的的指针 `ClassID` 。</span><span class="sxs-lookup"><span data-stu-id="2abdc-113">[out] A pointer to the `ClassID` of the specified type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2abdc-114">备注</span><span class="sxs-lookup"><span data-stu-id="2abdc-114">Remarks</span></span>  

 <span data-ttu-id="2abdc-115">`GetClassFromTokenAndTypeArgs`使用 `mdTypeRef` 而不是 `mdTypeDef` 元数据标记调用方法可能会产生不可预知的结果; 调用方应在 `mdTypeRef` 传递时将解析为 `mdTypeDef` 。</span><span class="sxs-lookup"><span data-stu-id="2abdc-115">Calling the `GetClassFromTokenAndTypeArgs` method with an `mdTypeRef` instead of an `mdTypeDef` metadata token can have unpredictable results; callers should resolve the `mdTypeRef` to an `mdTypeDef` when passing it.</span></span>  
  
 <span data-ttu-id="2abdc-116">如果尚未加载该类型，则调用 `GetClassFromTokenAndTypeArgs` 会触发加载，这在许多上下文中是一个危险操作。</span><span class="sxs-lookup"><span data-stu-id="2abdc-116">If the type is not already loaded, calling `GetClassFromTokenAndTypeArgs` will trigger loading, which is a dangerous operation in many contexts.</span></span> <span data-ttu-id="2abdc-117">例如，在加载模块或其他类型期间调用此方法可能会导致无限循环，因为运行时尝试循环加载某些功能。</span><span class="sxs-lookup"><span data-stu-id="2abdc-117">For example, calling this method during loading of modules or other types could lead to an infinite loop as the runtime attempts to circularly load things.</span></span>  
  
 <span data-ttu-id="2abdc-118">通常， `GetClassFromTokenAndTypeArgs` 不建议使用。</span><span class="sxs-lookup"><span data-stu-id="2abdc-118">In general, use of `GetClassFromTokenAndTypeArgs` is discouraged.</span></span> <span data-ttu-id="2abdc-119">如果探查器对特定类型的事件感兴趣，则它们应存储 `ModuleID` `mdTypeDef` 该类型的和，并使用 [ICorProfilerInfo2：： GetClassIDInfo2](icorprofilerinfo2-getclassidinfo2-method.md) 来检查给定的是否 `ClassID` 为所需的类型。</span><span class="sxs-lookup"><span data-stu-id="2abdc-119">If profilers are interested in events for a particular type, they should store the `ModuleID` and `mdTypeDef` of that type, and use [ICorProfilerInfo2::GetClassIDInfo2](icorprofilerinfo2-getclassidinfo2-method.md) to check whether a given `ClassID` is that of the desired type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2abdc-120">要求</span><span class="sxs-lookup"><span data-stu-id="2abdc-120">Requirements</span></span>  

 <span data-ttu-id="2abdc-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2abdc-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2abdc-122">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2abdc-122">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2abdc-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2abdc-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2abdc-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2abdc-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2abdc-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="2abdc-125">See also</span></span>

- [<span data-ttu-id="2abdc-126">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="2abdc-126">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="2abdc-127">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="2abdc-127">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
