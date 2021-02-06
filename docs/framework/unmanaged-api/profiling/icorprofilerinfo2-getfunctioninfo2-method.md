---
description: 了解详细信息： ICorProfilerInfo2：： GetFunctionInfo2 方法
title: ICorProfilerInfo2::GetFunctionInfo2 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetFunctionInfo2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetFunctionInfo2
helpviewer_keywords:
- GetFunctionInfo2 method [.NET Framework profiling]
- ICorProfilerInfo2::GetFunctionInfo2 method [.NET Framework profiling]
ms.assetid: 0aa60f24-8bbd-4c83-83c5-86ad191b1d82
topic_type:
- apiref
ms.openlocfilehash: f0534a2e8cc8a9ce24f2c2b3deaade6215e15b5a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657068"
---
# <a name="icorprofilerinfo2getfunctioninfo2-method"></a><span data-ttu-id="d553b-103">ICorProfilerInfo2::GetFunctionInfo2 方法</span><span class="sxs-lookup"><span data-stu-id="d553b-103">ICorProfilerInfo2::GetFunctionInfo2 Method</span></span>

<span data-ttu-id="d553b-104">获取每个类型参数或某个函数（如果存在）的父类、元数据标记和 `ClassID`。</span><span class="sxs-lookup"><span data-stu-id="d553b-104">Gets the parent class, the metadata token, and the `ClassID` of each type argument, if present, of a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d553b-105">语法</span><span class="sxs-lookup"><span data-stu-id="d553b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFunctionInfo2(  
    [in]  FunctionID funcId,  
    [in]  COR_PRF_FRAME_INFO frameInfo,  
    [out] ClassID *pClassId,  
    [out] ModuleID *pModuleId,  
    [out] mdToken *pToken,  
    [in]  ULONG32 cTypeArgs,  
    [out] ULONG32 *pcTypeArgs,  
    [out] ClassID typeArgs[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d553b-106">参数</span><span class="sxs-lookup"><span data-stu-id="d553b-106">Parameters</span></span>  

 `funcId`  
 <span data-ttu-id="d553b-107">[in] 要获取其父类和其他信息的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="d553b-107">[in] The ID of the function for which to get the parent class and other information.</span></span>  
  
 `frameInfo`  
 <span data-ttu-id="d553b-108">[in] 一个 `COR_PRF_FRAME_INFO` 值，该值指向有关堆栈帧的信息。</span><span class="sxs-lookup"><span data-stu-id="d553b-108">[in] A `COR_PRF_FRAME_INFO` value that points to information about a stack frame.</span></span>  
  
 `pClassId`  
 <span data-ttu-id="d553b-109">[out] 一个指向函数的父类的指针。</span><span class="sxs-lookup"><span data-stu-id="d553b-109">[out] A pointer to the parent class of the function.</span></span>  
  
 `pModuleId`  
 <span data-ttu-id="d553b-110">[out] 一个指向在其中定义函数父类的模块的指针。</span><span class="sxs-lookup"><span data-stu-id="d553b-110">[out] A pointer to the module in which the function's parent class is defined.</span></span>  
  
 `pToken`  
 <span data-ttu-id="d553b-111">[out] 指向函数的元数据标记的指针。</span><span class="sxs-lookup"><span data-stu-id="d553b-111">[out] A pointer to the metadata token for the function.</span></span>  
  
 `cTypeArgs`  
 <span data-ttu-id="d553b-112">[in] `typeArgs` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="d553b-112">[in] The size of the `typeArgs` array.</span></span>  
  
 `pcTypeArgs`  
 <span data-ttu-id="d553b-113">[out] 一个指向 `ClassID` 值的总数的指针。</span><span class="sxs-lookup"><span data-stu-id="d553b-113">[out] A pointer to the total number of `ClassID` values.</span></span>  
  
 `typeArgs`  
 <span data-ttu-id="d553b-114">[out] 一个由 `ClassID` 值构成的数组，其中的每个值都是函数的类型参数的 ID。</span><span class="sxs-lookup"><span data-stu-id="d553b-114">[out] An array of `ClassID` values, each of which is the ID of a type argument of the function.</span></span> <span data-ttu-id="d553b-115">方法返回时，`typeArgs` 将包含部分或全部 `ClassID` 值。</span><span class="sxs-lookup"><span data-stu-id="d553b-115">When the method returns, `typeArgs` will contain some or all of the `ClassID` values.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d553b-116">备注</span><span class="sxs-lookup"><span data-stu-id="d553b-116">Remarks</span></span>  

 <span data-ttu-id="d553b-117">探查器代码可调用 [ICorProfilerInfo：： GetModuleMetaData](icorprofilerinfo-getmodulemetadata-method.md) 以获取给定模块的 [元数据](../metadata/index.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="d553b-117">The profiler code can call [ICorProfilerInfo::GetModuleMetaData](icorprofilerinfo-getmodulemetadata-method.md) to obtain a [metadata](../metadata/index.md) interface for a given module.</span></span> <span data-ttu-id="d553b-118">然后，返回到 `pToken` 所引用位置的元数据标记便可用于访问该函数的元数据。</span><span class="sxs-lookup"><span data-stu-id="d553b-118">The metadata token that is returned to the location referenced by `pToken` can then be used to access the metadata for the function.</span></span>  
  
 <span data-ttu-id="d553b-119">通过 `pClassId` 和 `typeArgs` 参数返回的类 ID 和类型参数取决于传入 `frameInfo` 参数的值，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="d553b-119">The class ID and type arguments that are returned through the `pClassId` and `typeArgs` parameters depend on the value that is passed in the `frameInfo` parameter, as shown in the following table.</span></span>  
  
|<span data-ttu-id="d553b-120">`frameInfo` 参数的值</span><span class="sxs-lookup"><span data-stu-id="d553b-120">Value of the `frameInfo` parameter</span></span>|<span data-ttu-id="d553b-121">结果</span><span class="sxs-lookup"><span data-stu-id="d553b-121">Result</span></span>|  
|----------------------------------------|------------|  
|<span data-ttu-id="d553b-122">从 `FunctionEnter2` 回调中获得的 `COR_PRF_FRAME_INFO` 值</span><span class="sxs-lookup"><span data-stu-id="d553b-122">A `COR_PRF_FRAME_INFO` value that was obtained from a `FunctionEnter2` callback</span></span>|<span data-ttu-id="d553b-123">在 `pClassId` 所引用位置中返回的 `ClassID` 以及在 `typeArgs` 数组中返回的所有类型参数都将是准确的。</span><span class="sxs-lookup"><span data-stu-id="d553b-123">The `ClassID`, returned in the location referenced by `pClassId`, and all type arguments, returned in the `typeArgs` array, will be exact.</span></span>|  
|<span data-ttu-id="d553b-124">从 `FunctionEnter2` 回调以外的源中获得的 `COR_PRF_FRAME_INFO`</span><span class="sxs-lookup"><span data-stu-id="d553b-124">A `COR_PRF_FRAME_INFO` that was obtained from a source other than a `FunctionEnter2` callback</span></span>|<span data-ttu-id="d553b-125">无法确定准确的 `ClassID` 和类型参数。</span><span class="sxs-lookup"><span data-stu-id="d553b-125">The exact `ClassID` and type arguments cannot be determined.</span></span> <span data-ttu-id="d553b-126">也就是说，`ClassID` 可能为 NULL，并且某些类型参数可能作为 <xref:System.Object> 返回。</span><span class="sxs-lookup"><span data-stu-id="d553b-126">That is, the `ClassID` might be null and some type arguments might come back as <xref:System.Object>.</span></span>|  
|<span data-ttu-id="d553b-127">零</span><span class="sxs-lookup"><span data-stu-id="d553b-127">Zero</span></span>|<span data-ttu-id="d553b-128">无法确定准确的 `ClassID` 和类型参数。</span><span class="sxs-lookup"><span data-stu-id="d553b-128">The exact `ClassID` and type arguments cannot be determined.</span></span> <span data-ttu-id="d553b-129">也就是说，`ClassID` 可能为 NULL，并且某些类型参数可能作为 <xref:System.Object> 返回。</span><span class="sxs-lookup"><span data-stu-id="d553b-129">That is, the `ClassID` might be null and some type arguments might come back as <xref:System.Object>.</span></span>|  
  
 <span data-ttu-id="d553b-130">`GetFunctionInfo2` 返回后，必须验证 `typeArgs` 缓冲区是否足够大，可包含所有 `ClassID` 值。</span><span class="sxs-lookup"><span data-stu-id="d553b-130">After `GetFunctionInfo2` returns, you must verify that the `typeArgs` buffer was large enough to contain all the `ClassID` values.</span></span> <span data-ttu-id="d553b-131">为此，请比较 `pcTypeArgs` 指向的值和 `cTypeArgs` 参数的值。</span><span class="sxs-lookup"><span data-stu-id="d553b-131">To do this, compare the value that `pcTypeArgs` points to with the value of the `cTypeArgs` parameter.</span></span> <span data-ttu-id="d553b-132">如果 `pcTypeArgs` 指向大于`cTypeArgs` 除以 `ClassID` 值大小的值，请分配更大的 `pcTypeArgs` 缓冲区，使用新的、更大的大小更新 `cTypeArgs`，然后再次调用 `GetFunctionInfo2`。</span><span class="sxs-lookup"><span data-stu-id="d553b-132">If `pcTypeArgs` points to a value that is larger than `cTypeArgs` divided by the size of a `ClassID` value, allocate a larger `pcTypeArgs` buffer, update `cTypeArgs` with the new, larger size, and call `GetFunctionInfo2` again.</span></span>  
  
 <span data-ttu-id="d553b-133">或者，可以先用长度为零的 `pcTypeArgs` 缓冲区调用 `GetFunctionInfo2` 以获取正确的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="d553b-133">Alternatively, you can first call `GetFunctionInfo2` with a zero-length `pcTypeArgs` buffer to obtain the correct buffer size.</span></span> <span data-ttu-id="d553b-134">然后，可将缓冲区大小设置为 `pcTypeArgs` 中返回的值除以 `ClassID` 值的大小，然后再次调用 `GetFunctionInfo2`。</span><span class="sxs-lookup"><span data-stu-id="d553b-134">You can then set the buffer size to the value returned in `pcTypeArgs` divided by the size of a `ClassID` value, and call `GetFunctionInfo2` again.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d553b-135">要求</span><span class="sxs-lookup"><span data-stu-id="d553b-135">Requirements</span></span>  

 <span data-ttu-id="d553b-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d553b-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d553b-137">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d553b-137">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d553b-138">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d553b-138">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d553b-139">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d553b-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d553b-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="d553b-140">See also</span></span>

- [<span data-ttu-id="d553b-141">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="d553b-141">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="d553b-142">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="d553b-142">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
- [<span data-ttu-id="d553b-143">分析接口</span><span class="sxs-lookup"><span data-stu-id="d553b-143">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="d553b-144">分析</span><span class="sxs-lookup"><span data-stu-id="d553b-144">Profiling</span></span>](index.md)
