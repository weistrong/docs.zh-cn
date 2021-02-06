---
description: 了解详细信息： ICorProfilerInfo：： GetILFunctionBodyAllocator 方法
title: ICorProfilerInfo::GetILFunctionBodyAllocator 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetILFunctionBodyAllocator
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetILFunctionBodyAllocator
helpviewer_keywords:
- GetILFunctionBodyAllocator method [.NET Framework profiling]
- ICorProfilerInfo::GetILFunctionBodyAllocator method [.NET Framework profiling]
ms.assetid: 5da1bf3d-dddf-4892-b266-578ee54d570b
topic_type:
- apiref
ms.openlocfilehash: 25d059d784fe64231d4d2ff3d23b4820443873cf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647422"
---
# <a name="icorprofilerinfogetilfunctionbodyallocator-method"></a><span data-ttu-id="fa686-103">ICorProfilerInfo::GetILFunctionBodyAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="fa686-103">ICorProfilerInfo::GetILFunctionBodyAllocator Method</span></span>

<span data-ttu-id="fa686-104">获取一个接口，该接口提供一种方法，用于分配内存，以用于在 Microsoft 中间语言 (MSIL) 代码中交换方法体。</span><span class="sxs-lookup"><span data-stu-id="fa686-104">Gets an interface that provides a method to allocate memory to be used for swapping out the body of a method in Microsoft intermediate language (MSIL) code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa686-105">语法</span><span class="sxs-lookup"><span data-stu-id="fa686-105">Syntax</span></span>  
  
```cpp  
HRESULT GetILFunctionBodyAllocator(  
    [in]  ModuleID      moduleId,  
    [out] IMethodMalloc **ppMalloc);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fa686-106">参数</span><span class="sxs-lookup"><span data-stu-id="fa686-106">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="fa686-107">中方法所在的模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="fa686-107">[in] The ID of the module in which the method resides.</span></span>  
  
 `ppMalloc`  
 <span data-ttu-id="fa686-108">弄指向 [IMethodMalloc](imethodmalloc-interface.md) 接口的指针，该接口提供分配内存的方法。</span><span class="sxs-lookup"><span data-stu-id="fa686-108">[out] A pointer to an [IMethodMalloc](imethodmalloc-interface.md) interface that provides a method to allocate the memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fa686-109">备注</span><span class="sxs-lookup"><span data-stu-id="fa686-109">Remarks</span></span>  

 <span data-ttu-id="fa686-110">MSIL 代码中的方法体必须位于 RVA)  (RVA 上（相对于已加载的模块），这意味着它遵循 4 GB 内的模块。</span><span class="sxs-lookup"><span data-stu-id="fa686-110">A method body in MSIL code must be located as a relative virtual address (RVA), relative to the loaded module, which means that it follows the module within 4 GB.</span></span> <span data-ttu-id="fa686-111">为了使工具能够更轻松地调换方法的主体， `GetILFunctionBodyAllocator` 方法可确保在该范围内分配内存。</span><span class="sxs-lookup"><span data-stu-id="fa686-111">To make it easier for a tool to swap out the body of a method, the `GetILFunctionBodyAllocator` method ensures that memory is allocated within that range.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fa686-112">要求</span><span class="sxs-lookup"><span data-stu-id="fa686-112">Requirements</span></span>  

 <span data-ttu-id="fa686-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fa686-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa686-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fa686-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fa686-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fa686-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fa686-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa686-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa686-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="fa686-117">See also</span></span>

- [<span data-ttu-id="fa686-118">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="fa686-118">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
