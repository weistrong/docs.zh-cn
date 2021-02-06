---
description: 了解详细信息： ICorProfilerInfo8：： GetDynamicFunctionInfo 方法
title: ICorProfilerInfo8::GetDynamicFunctionInfo
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo8.GetDynamicFunctionInfo
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: 48c8dbe20ccafb3fb23e9e289f728d5e3370613a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646577"
---
# <a name="icorprofilerinfo8getdynamicfunctioninfo-method"></a><span data-ttu-id="2489d-103">ICorProfilerInfo8：： GetDynamicFunctionInfo 方法</span><span class="sxs-lookup"><span data-stu-id="2489d-103">ICorProfilerInfo8::GetDynamicFunctionInfo Method</span></span>

<span data-ttu-id="2489d-104">检索有关动态方法的信息。</span><span class="sxs-lookup"><span data-stu-id="2489d-104">Retrieves information about dynamic methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="2489d-105">语法</span><span class="sxs-lookup"><span data-stu-id="2489d-105">Syntax</span></span>

```cpp
HRESULT GetDynamicFunctionInfo( [in]  FunctionID              functionId,
                                [out] ModuleID                *moduleId,
                                [out] PCCOR_SIGNATURE         *ppvSig,
                                [out] ULONG                   *pbSig,
                                [in]  ULONG                   cchName,
                                [out] ULONG                   *pcchName,
                                [out] WCHAR                   wszName[]);
```

## <a name="parameters"></a><span data-ttu-id="2489d-106">参数</span><span class="sxs-lookup"><span data-stu-id="2489d-106">Parameters</span></span>

- `functionId`

  <span data-ttu-id="2489d-107">\[in] 要为其检索信息的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="2489d-107">\[in] The ID of the function for which to retrieve information.</span></span>

- `moduleId`

  <span data-ttu-id="2489d-108">\[in] 一个指针，指向在其中定义函数父类的模块。</span><span class="sxs-lookup"><span data-stu-id="2489d-108">\[in] A pointer to the module in which the function's parent class is defined.</span></span>

- `ppvSig`

  <span data-ttu-id="2489d-109">\[out] 指向函数的签名的指针。</span><span class="sxs-lookup"><span data-stu-id="2489d-109">\[out] A pointer to the signature for the function.</span></span>

- `pbSig`

  <span data-ttu-id="2489d-110">\[out] 指向函数签名的字节计数的指针。</span><span class="sxs-lookup"><span data-stu-id="2489d-110">\[out] A pointer to the count of bytes for the function signature.</span></span>

- `cchName`

  <span data-ttu-id="2489d-111">\[in] 数组的最大大小 `wszName` 。</span><span class="sxs-lookup"><span data-stu-id="2489d-111">\[in] The maximum size of the `wszName` array.</span></span>

- `pcchName`

  <span data-ttu-id="2489d-112">\[out] 数组中的字符数 `wszName` 。</span><span class="sxs-lookup"><span data-stu-id="2489d-112">\[out] The number of characters in the `wszName` array.</span></span>

- `wszName`

  <span data-ttu-id="2489d-113">\[out] 作为 `WCHAR` 函数名称（如果存在）的数组。</span><span class="sxs-lookup"><span data-stu-id="2489d-113">\[out] An array of `WCHAR` which is the name of the function, if one exists.</span></span>

## <a name="remarks"></a><span data-ttu-id="2489d-114">备注</span><span class="sxs-lookup"><span data-stu-id="2489d-114">Remarks</span></span>

<span data-ttu-id="2489d-115">某些方法（如 IL 存根或 LCG）没有关联的元数据，可以使用 [IMetaDataImport](../metadata/imetadataimport-interface.md) 和 [IMetaDataImport2](../metadata/imetadataimport2-interface.md) api 来检索这些元数据。</span><span class="sxs-lookup"><span data-stu-id="2489d-115">Certain methods like IL Stubs or LCG do not have associated metadata that can be retrieved using the [IMetaDataImport](../metadata/imetadataimport-interface.md) and [IMetaDataImport2](../metadata/imetadataimport2-interface.md) APIs.</span></span> <span data-ttu-id="2489d-116">探查器可以通过指令指针或通过侦听 [ICorProfilerCallback8：:D ynamicmethodjitcompilationstarted](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)来遇到此类方法。</span><span class="sxs-lookup"><span data-stu-id="2489d-116">Such methods can be encountered by profilers through instruction pointers or by listening to [ICorProfilerCallback8::DynamicMethodJITCompilationStarted](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md).</span></span>

<span data-ttu-id="2489d-117">此 API 可用于检索有关动态方法的信息，包括友好名称（如果可用）。</span><span class="sxs-lookup"><span data-stu-id="2489d-117">This API can be used to retrieve information about dynamic methods, including a friendly name, if available.</span></span>

## <a name="requirements"></a><span data-ttu-id="2489d-118">要求</span><span class="sxs-lookup"><span data-stu-id="2489d-118">Requirements</span></span>

<span data-ttu-id="2489d-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2489d-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="2489d-120">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2489d-120">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="2489d-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2489d-121">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="2489d-122">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="2489d-122">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="2489d-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="2489d-123">See also</span></span>

- [<span data-ttu-id="2489d-124">ICorProfilerInfo8 接口</span><span class="sxs-lookup"><span data-stu-id="2489d-124">ICorProfilerInfo8 Interface</span></span>](icorprofilerinfo8-interface.md)
