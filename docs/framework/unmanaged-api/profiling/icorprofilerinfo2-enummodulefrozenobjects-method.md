---
description: 了解详细信息： ICorProfilerInfo2：： EnumModuleFrozenObjects 方法
title: ICorProfilerInfo2::EnumModuleFrozenObjects 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.EnumModuleFrozenObjects
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::EnumModuleFrozenObjects
helpviewer_keywords:
- EnumModuleFrozenObjects method [.NET Framework profiling]
- ICorProfilerInfo2::EnumModuleFrozenObjects method [.NET Framework profiling]
ms.assetid: 920b6483-7064-4d64-8613-fcc38ccf9b1e
topic_type:
- apiref
ms.openlocfilehash: b68571544c00c8c234a73404a95433e91f0cfdcf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753206"
---
# <a name="icorprofilerinfo2enummodulefrozenobjects-method"></a><span data-ttu-id="e8110-103">ICorProfilerInfo2::EnumModuleFrozenObjects 方法</span><span class="sxs-lookup"><span data-stu-id="e8110-103">ICorProfilerInfo2::EnumModuleFrozenObjects Method</span></span>

<span data-ttu-id="e8110-104">获取一个枚举器，该枚举数允许对指定模块中的冻结对象进行迭代。此方法已过时。</span><span class="sxs-lookup"><span data-stu-id="e8110-104">Gets an enumerator that allows iteration over the frozen objects in the specified module.This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8110-105">语法</span><span class="sxs-lookup"><span data-stu-id="e8110-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumModuleFrozenObjects(  
    [in] ModuleID moduleID,  
    [out] ICorProfilerObjectEnum** ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e8110-106">参数</span><span class="sxs-lookup"><span data-stu-id="e8110-106">Parameters</span></span>  

 `moduleID`  
 <span data-ttu-id="e8110-107">中包含要枚举的冻结对象的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="e8110-107">[in] The ID of the module that contains the frozen objects to be enumerated.</span></span>  
  
 `ppEnum`  
 <span data-ttu-id="e8110-108">弄一个指针，指向用于枚举冻结对象的 [ICorProfilerObjectEnum](icorprofilerobjectenum-interface.md) 接口的地址。</span><span class="sxs-lookup"><span data-stu-id="e8110-108">[out] A pointer to the address of an [ICorProfilerObjectEnum](icorprofilerobjectenum-interface.md) interface, which enumerates the frozen objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8110-109">要求</span><span class="sxs-lookup"><span data-stu-id="e8110-109">Requirements</span></span>  

 <span data-ttu-id="e8110-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e8110-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8110-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e8110-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e8110-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e8110-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e8110-113">**.NET Framework 版本：** 3.5、3.0 SP1、3.0、2.0 SP1、2。0</span><span class="sxs-lookup"><span data-stu-id="e8110-113">**.NET Framework Versions:** 3.5, 3.0 SP1, 3.0, 2.0 SP1, 2.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8110-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="e8110-114">See also</span></span>

- [<span data-ttu-id="e8110-115">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="e8110-115">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="e8110-116">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="e8110-116">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
