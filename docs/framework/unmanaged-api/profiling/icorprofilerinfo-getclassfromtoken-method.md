---
description: 了解详细信息： ICorProfilerInfo：： GetClassFromToken 方法
title: ICorProfilerInfo::GetClassFromToken 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetClassFromToken
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetClassFromToken
helpviewer_keywords:
- ICorProfilerInfo::GetClassFromToken method [.NET Framework profiling]
- GetClassFromToken method, ICorProfilerInfo interface [.NET Framework profiling]
ms.assetid: 0afc1197-2a5b-424f-8b82-9cb59a7e00db
topic_type:
- apiref
ms.openlocfilehash: 0460a9b767f29f108a2b290b848f4cc6b6394ecb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647747"
---
# <a name="icorprofilerinfogetclassfromtoken-method"></a><span data-ttu-id="b23d9-103">ICorProfilerInfo::GetClassFromToken 方法</span><span class="sxs-lookup"><span data-stu-id="b23d9-103">ICorProfilerInfo::GetClassFromToken Method</span></span>

<span data-ttu-id="b23d9-104">给定元数据标记，获取类的 ID。</span><span class="sxs-lookup"><span data-stu-id="b23d9-104">Gets the ID of the class, given the metadata token.</span></span> <span data-ttu-id="b23d9-105">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="b23d9-105">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="b23d9-106">改 [为使用 ICorProfilerInfo2：： GetClassFromTokenAndTypeArgs](icorprofilerinfo2-getclassfromtokenandtypeargs-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="b23d9-106">Use [ICorProfilerInfo2::GetClassFromTokenAndTypeArgs](icorprofilerinfo2-getclassfromtokenandtypeargs-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b23d9-107">语法</span><span class="sxs-lookup"><span data-stu-id="b23d9-107">Syntax</span></span>  
  
```cpp  
HRESULT GetClassFromToken(  
    [in]  ModuleID  moduleId,  
    [in]  mdTypeDef typeDef,  
    [out] ClassID   *pClassId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b23d9-108">参数</span><span class="sxs-lookup"><span data-stu-id="b23d9-108">Parameters</span></span>  

 `moduleID`  
 <span data-ttu-id="b23d9-109">中包含类的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="b23d9-109">[in] The ID of the module that contains the class.</span></span>  
  
 `typeDef`  
 <span data-ttu-id="b23d9-110">中 `mdTypeDef` 引用类的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="b23d9-110">[in] An `mdTypeDef` metadata token that references the class.</span></span>  
  
 `cTypeArgs`  
 <span data-ttu-id="b23d9-111">弄指向类 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="b23d9-111">[out] A pointer to the class ID.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b23d9-112">备注</span><span class="sxs-lookup"><span data-stu-id="b23d9-112">Remarks</span></span>  

 <span data-ttu-id="b23d9-113">此方法已过时;而是将 `ICorProfilerInfo2::GetClassFromTokenAndTypeArgs` 用于所有类型。</span><span class="sxs-lookup"><span data-stu-id="b23d9-113">This method is obsolete; instead, use `ICorProfilerInfo2::GetClassFromTokenAndTypeArgs` for all types.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b23d9-114">要求</span><span class="sxs-lookup"><span data-stu-id="b23d9-114">Requirements</span></span>  

 <span data-ttu-id="b23d9-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b23d9-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b23d9-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b23d9-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b23d9-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b23d9-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b23d9-118">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="b23d9-118">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b23d9-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="b23d9-119">See also</span></span>

- [<span data-ttu-id="b23d9-120">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="b23d9-120">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
