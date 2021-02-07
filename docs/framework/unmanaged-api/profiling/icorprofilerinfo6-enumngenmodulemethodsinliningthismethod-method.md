---
description: 了解详细信息： ICorProfilerInfo6：： EnumNgenModuleMethodsInliningThisMethod 方法
title: ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod 方法
ms.date: 03/30/2017
ms.assetid: b933dfe6-7833-40cb-aad8-40842dc3034f
ms.openlocfilehash: bd43dcecabe9a75f7ce3a94996727b192574e321
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737163"
---
# <a name="icorprofilerinfo6enumngenmodulemethodsinliningthismethod-method"></a><span data-ttu-id="d6456-103">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod 方法</span><span class="sxs-lookup"><span data-stu-id="d6456-103">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod Method</span></span>

<span data-ttu-id="d6456-104">返回一个枚举器，该枚举器指向给定的 NGen 模块中定义的所有方法，并内联给定方法。</span><span class="sxs-lookup"><span data-stu-id="d6456-104">Returns an enumerator to all the methods that are defined in a given NGen module and inline a given method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6456-105">语法</span><span class="sxs-lookup"><span data-stu-id="d6456-105">Syntax</span></span>

```cpp
HRESULT EnumNgenModuleMethodsInliningThisMethod(
        [in] ModuleID inlinersModuleId,
        [in] ModuleID inlineeModuleId,
        [in] mdMethodDef inlineeMethodId,
        [out] BOOL *incompleteData,
        [out] ICorProfilerMethodEnum** ppEnum
);
```

## <a name="parameters"></a><span data-ttu-id="d6456-106">参数</span><span class="sxs-lookup"><span data-stu-id="d6456-106">Parameters</span></span>

`inlinersModuleId`\
<span data-ttu-id="d6456-107">中NGen 模块的标识符。</span><span class="sxs-lookup"><span data-stu-id="d6456-107">[in] The identifier of an NGen module.</span></span>

`inlineeModuleId`\
<span data-ttu-id="d6456-108">中定义的模块的标识符 `inlineeMethodId` 。</span><span class="sxs-lookup"><span data-stu-id="d6456-108">[in] The identifier of a module that defines `inlineeMethodId`.</span></span> <span data-ttu-id="d6456-109">有关详细信息，请参阅备注部分。</span><span class="sxs-lookup"><span data-stu-id="d6456-109">See the Remarks section for more information.</span></span>

`inlineeMethodId`\
<span data-ttu-id="d6456-110">中内联方法的标识符。</span><span class="sxs-lookup"><span data-stu-id="d6456-110">[in] The identifier of an inlined method.</span></span> <span data-ttu-id="d6456-111">有关详细信息，请参阅备注部分。</span><span class="sxs-lookup"><span data-stu-id="d6456-111">See the Remarks section for more information.</span></span>

`incompleteData`\
<span data-ttu-id="d6456-112">弄一个标志，该标志指示是否 `ppEnum` 将所有方法内联到给定方法。</span><span class="sxs-lookup"><span data-stu-id="d6456-112">[out] A flag that indicates whether `ppEnum` contains all methods inlining a given method.</span></span>  <span data-ttu-id="d6456-113">有关详细信息，请参阅备注部分。</span><span class="sxs-lookup"><span data-stu-id="d6456-113">See the Remarks section for more information.</span></span>

`ppEnum`\
<span data-ttu-id="d6456-114">弄指向枚举器地址的指针</span><span class="sxs-lookup"><span data-stu-id="d6456-114">[out] A pointer to the address of an enumerator</span></span>

## <a name="remarks"></a><span data-ttu-id="d6456-115">备注</span><span class="sxs-lookup"><span data-stu-id="d6456-115">Remarks</span></span>

<span data-ttu-id="d6456-116">`inlineeModuleId` 和 `inlineeMethodId` 共同构成了可能内联的方法的完整标识符。</span><span class="sxs-lookup"><span data-stu-id="d6456-116">`inlineeModuleId` and `inlineeMethodId` together form the full identifier for the method that might be inlined.</span></span> <span data-ttu-id="d6456-117">例如，假设 module `A` 定义方法 `Simple.Add` ：</span><span class="sxs-lookup"><span data-stu-id="d6456-117">For example, assume module `A` defines a method `Simple.Add`:</span></span>

```csharp
Simple.Add(int a, int b)
{ return a + b; }
```

<span data-ttu-id="d6456-118">和模块 B 定义 `Fancy.AddTwice` ：</span><span class="sxs-lookup"><span data-stu-id="d6456-118">and module B defines `Fancy.AddTwice`:</span></span>

```csharp
Fancy.AddTwice(int a, int b)
{ return Simple.Add(a,b) + Simple.Add(a,b); }
```

<span data-ttu-id="d6456-119">还假定 `Fancy.AddTwice` inlines 调用 `SimpleAdd` 。</span><span class="sxs-lookup"><span data-stu-id="d6456-119">Lets also assume that `Fancy.AddTwice` inlines the call to `SimpleAdd`.</span></span> <span data-ttu-id="d6456-120">探查器可以使用此枚举器查找在模块 B 中定义的内联的所有方法 `Simple.Add` ，并将枚举结果 `AddTwice` 。</span><span class="sxs-lookup"><span data-stu-id="d6456-120">A profiler could use this enumerator to find all methods defined in module B which inline `Simple.Add`, and the result would enumerate `AddTwice`.</span></span>  <span data-ttu-id="d6456-121">`inlineeModuleId` 是模块的标识符 `A` ，是的 `inlineeMethodId` 标识符 `Simple.Add(int a, int b)` 。</span><span class="sxs-lookup"><span data-stu-id="d6456-121">`inlineeModuleId` is the identifier of module `A`, and `inlineeMethodId` is the identifier of `Simple.Add(int a, int b)`.</span></span>

<span data-ttu-id="d6456-122">如果在 `incompleteData` 函数返回后为 true，则枚举器不包含内联给定方法的所有方法。</span><span class="sxs-lookup"><span data-stu-id="d6456-122">If `incompleteData` is true after the function returns, the enumerator does not contain all methods inlining a given method.</span></span> <span data-ttu-id="d6456-123">如果尚未加载 inliners 模块的一个或多个直接或间接依赖项，则可能会发生这种情况。</span><span class="sxs-lookup"><span data-stu-id="d6456-123">This can happen when one or more direct or indirect dependencies of inliners module haven't been loaded yet.</span></span> <span data-ttu-id="d6456-124">如果探查器需要准确的数据，则应在加载更多模块时重试，最好是在每个模块加载时重试。</span><span class="sxs-lookup"><span data-stu-id="d6456-124">If a profiler needs accurate data, it should retry later when more modules are loaded, preferably on each module load.</span></span>

<span data-ttu-id="d6456-125">`EnumNgenModuleMethodsInliningThisMethod`方法可用于解决 ReJIT 的内联限制。</span><span class="sxs-lookup"><span data-stu-id="d6456-125">The `EnumNgenModuleMethodsInliningThisMethod` method can be used to work around limitations on inlining for ReJIT.</span></span> <span data-ttu-id="d6456-126">ReJIT 使探查器可以更改方法的实现，然后动态为其创建新代码。</span><span class="sxs-lookup"><span data-stu-id="d6456-126">ReJIT lets a profiler change the implementation of a method and then create new code for it on the fly.</span></span> <span data-ttu-id="d6456-127">例如，我们可以 `Simple.Add` 按如下所示进行更改：</span><span class="sxs-lookup"><span data-stu-id="d6456-127">For example, we could change `Simple.Add` as follows:</span></span>

```csharp
Simple.Add(int a, int b)
{ return 42; }
```

<span data-ttu-id="d6456-128">但是 `Fancy.AddTwice` ，因为已内联 `Simple.Add` ，所以它的行为与以前相同。</span><span class="sxs-lookup"><span data-stu-id="d6456-128">However because `Fancy.AddTwice` has already inlined `Simple.Add`, it continues to have the same behavior as before.</span></span> <span data-ttu-id="d6456-129">若要解决此限制，调用方必须搜索所有在这些方法中内联和使用的模块中的所有方法 `Simple.Add` `ICorProfilerInfo5::RequestRejit` 。</span><span class="sxs-lookup"><span data-stu-id="d6456-129">To work around that limitation, the caller has to search for all methods in all modules that inline `Simple.Add` and use `ICorProfilerInfo5::RequestRejit` on each of those methods.</span></span> <span data-ttu-id="d6456-130">重新编译这些方法时，它们将具有新的行为， `Simple.Add` 而不是旧的行为。</span><span class="sxs-lookup"><span data-stu-id="d6456-130">When the methods are re-compiled, they will have the new behavior of `Simple.Add` instead of the old behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6456-131">要求</span><span class="sxs-lookup"><span data-stu-id="d6456-131">Requirements</span></span>

<span data-ttu-id="d6456-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d6456-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="d6456-133">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d6456-133">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="d6456-134">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d6456-134">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="d6456-135">**.NET Framework 版本：**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d6456-135">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="d6456-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="d6456-136">See also</span></span>

- [<span data-ttu-id="d6456-137">ICorProfilerInfo6 接口</span><span class="sxs-lookup"><span data-stu-id="d6456-137">ICorProfilerInfo6 Interface</span></span>](icorprofilerinfo6-interface.md)
