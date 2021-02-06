---
description: 了解详细信息： ICorProfilerInfo：： GetFunctionFromToken 方法
title: ICorProfilerInfo::GetFunctionFromToken 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetFunctionFromToken
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetFunctionFromToken
helpviewer_keywords:
- ICorProfilerInfo::GetFunctionFromToken method [.NET Framework profiling]
- GetFunctionFromToken method, ICorProfilerInfo interface [.NET Framework profiling]
ms.assetid: 0eed759f-cce8-405d-88dc-9ee293a38928
topic_type:
- apiref
ms.openlocfilehash: 58dea413539d6e3a625f515aa7e8d5123152c90a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647448"
---
# <a name="icorprofilerinfogetfunctionfromtoken-method"></a><span data-ttu-id="a933a-103">ICorProfilerInfo::GetFunctionFromToken 方法</span><span class="sxs-lookup"><span data-stu-id="a933a-103">ICorProfilerInfo::GetFunctionFromToken Method</span></span>

<span data-ttu-id="a933a-104">获取函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="a933a-104">Gets the ID of a function.</span></span> <span data-ttu-id="a933a-105">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="a933a-105">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="a933a-106">改为使用 [ICorProfilerInfo2：： GetFunctionFromTokenAndTypeArgs](icorprofilerinfo2-getfunctionfromtokenandtypeargs-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a933a-106">Use the [ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs](icorprofilerinfo2-getfunctionfromtokenandtypeargs-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a933a-107">语法</span><span class="sxs-lookup"><span data-stu-id="a933a-107">Syntax</span></span>  
  
```cpp  
HRESULT GetFunctionFromToken(  
    [in]  ModuleID   moduleId,  
    [in]  mdToken    token,  
    [out] FunctionID *pFunctionId);  
```  
  
## <a name="remarks"></a><span data-ttu-id="a933a-108">备注</span><span class="sxs-lookup"><span data-stu-id="a933a-108">Remarks</span></span>  

 <span data-ttu-id="a933a-109">此 `GetFunctionFromToken` 方法不适用于泛型函数或泛型类型中的函数; 它现在已过时。</span><span class="sxs-lookup"><span data-stu-id="a933a-109">The `GetFunctionFromToken` method will not work for generic functions or functions in generic types; it is now obsolete.</span></span> <span data-ttu-id="a933a-110">用于 `ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs` 所有函数。</span><span class="sxs-lookup"><span data-stu-id="a933a-110">Use `ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs` for all functions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a933a-111">要求</span><span class="sxs-lookup"><span data-stu-id="a933a-111">Requirements</span></span>  

 <span data-ttu-id="a933a-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a933a-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a933a-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a933a-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a933a-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a933a-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a933a-115">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="a933a-115">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a933a-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="a933a-116">See also</span></span>

- [<span data-ttu-id="a933a-117">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="a933a-117">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
