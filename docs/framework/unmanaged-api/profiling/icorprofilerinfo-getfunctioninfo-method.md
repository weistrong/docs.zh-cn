---
description: 了解详细信息： ICorProfilerInfo：： GetFunctionInfo 方法
title: ICorProfilerInfo::GetFunctionInfo 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetFunctionInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetFunctionInfo
helpviewer_keywords:
- ICorProfilerInfo::GetFunctionInfo method [.NET Framework profiling]
- GetFunctionInfo method [.NET Framework profiling]
ms.assetid: c42b5891-019d-46b3-b551-4606295b75b8
topic_type:
- apiref
ms.openlocfilehash: e6ad1112f0e6938fc6de549d3a1d2f0901150025
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647514"
---
# <a name="icorprofilerinfogetfunctioninfo-method"></a><span data-ttu-id="ed5c6-103">ICorProfilerInfo::GetFunctionInfo 方法</span><span class="sxs-lookup"><span data-stu-id="ed5c6-103">ICorProfilerInfo::GetFunctionInfo Method</span></span>

<span data-ttu-id="ed5c6-104">获取指定函数的父类和元数据标记。</span><span class="sxs-lookup"><span data-stu-id="ed5c6-104">Gets the parent class and metadata token for the specified function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed5c6-105">语法</span><span class="sxs-lookup"><span data-stu-id="ed5c6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFunctionInfo(  
    [in]  FunctionID functionId,  
    [out] ClassID    *pClassId,  
    [out] ModuleID   *pModuleId,  
    [out] mdToken    *pToken);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ed5c6-106">参数</span><span class="sxs-lookup"><span data-stu-id="ed5c6-106">Parameters</span></span>  

 `functionId`  
 <span data-ttu-id="ed5c6-107">中要获取其父类和元数据标记的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="ed5c6-107">[in] The ID of the function for which to get the parent class and metadata token.</span></span>  
  
 `pClassId`  
 <span data-ttu-id="ed5c6-108">[out] 一个指向函数的父类的指针。</span><span class="sxs-lookup"><span data-stu-id="ed5c6-108">[out] A pointer to the parent class of the function.</span></span>  
  
 `pModuleId`  
 <span data-ttu-id="ed5c6-109">[out] 一个指向在其中定义函数父类的模块的指针。</span><span class="sxs-lookup"><span data-stu-id="ed5c6-109">[out] A pointer to the module in which the function's parent class is defined.</span></span>  
  
 `pToken`  
 <span data-ttu-id="ed5c6-110">[out] 指向函数的元数据标记的指针。</span><span class="sxs-lookup"><span data-stu-id="ed5c6-110">[out] A pointer to the metadata token for the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ed5c6-111">备注</span><span class="sxs-lookup"><span data-stu-id="ed5c6-111">Remarks</span></span>  

 <span data-ttu-id="ed5c6-112">探查器代码可调用 [ICorProfilerInfo：： GetModuleMetaData](icorprofilerinfo-getmodulemetadata-method.md) 以获取给定模块的元数据接口。</span><span class="sxs-lookup"><span data-stu-id="ed5c6-112">The profiler code can call [ICorProfilerInfo::GetModuleMetaData](icorprofilerinfo-getmodulemetadata-method.md) to obtain a metadata interface for a given module.</span></span> <span data-ttu-id="ed5c6-113">然后，返回到 `pToken` 所引用位置的元数据标记便可用于访问该函数的元数据。</span><span class="sxs-lookup"><span data-stu-id="ed5c6-113">The metadata token that is returned to the location referenced by `pToken` can then be used to access the metadata for the function.</span></span>  
  
 <span data-ttu-id="ed5c6-114">对于 `ClassID` 泛型类中的函数，如果没有关于函数使用的更多上下文信息，则可能无法获得。</span><span class="sxs-lookup"><span data-stu-id="ed5c6-114">The `ClassID` of a function on a generic class might not be obtainable without more contextual information about the use of the function.</span></span> <span data-ttu-id="ed5c6-115">在这种情况下， `pClassId` 将为0。</span><span class="sxs-lookup"><span data-stu-id="ed5c6-115">In this case, `pClassId` will be 0.</span></span> <span data-ttu-id="ed5c6-116">探查器代码应将 [ICorProfilerInfo2：： GetFunctionInfo2](icorprofilerinfo2-getfunctioninfo2-method.md) 与 COR_PRF_FRAME_INFO 值一起使用，以提供更多上下文。</span><span class="sxs-lookup"><span data-stu-id="ed5c6-116">Profiler code should use [ICorProfilerInfo2::GetFunctionInfo2](icorprofilerinfo2-getfunctioninfo2-method.md) with a COR_PRF_FRAME_INFO value to provide more context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ed5c6-117">要求</span><span class="sxs-lookup"><span data-stu-id="ed5c6-117">Requirements</span></span>  

 <span data-ttu-id="ed5c6-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ed5c6-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ed5c6-119">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ed5c6-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ed5c6-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ed5c6-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ed5c6-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed5c6-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed5c6-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed5c6-122">See also</span></span>

- [<span data-ttu-id="ed5c6-123">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="ed5c6-123">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
