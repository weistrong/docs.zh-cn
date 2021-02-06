---
description: 了解详细信息： ICorProfilerInfo：： SetILFunctionBody 方法
title: ICorProfilerInfo::SetILFunctionBody 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.SetILFunctionBody
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::SetILFunctionBody
helpviewer_keywords:
- ICorProfilerInfo::SetILFunctionBody method [.NET Framework profiling]
- SetILFunctionBody method [.NET Framework profiling]
ms.assetid: b159c712-00f4-4fc7-a990-40bf9f642e8f
topic_type:
- apiref
ms.openlocfilehash: 38e7907080065dc96d72a3d38a67227414637a70
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647162"
---
# <a name="icorprofilerinfosetilfunctionbody-method"></a><span data-ttu-id="c40e8-103">ICorProfilerInfo::SetILFunctionBody 方法</span><span class="sxs-lookup"><span data-stu-id="c40e8-103">ICorProfilerInfo::SetILFunctionBody Method</span></span>

<span data-ttu-id="c40e8-104">替换指定模块中指定函数的主体。</span><span class="sxs-lookup"><span data-stu-id="c40e8-104">Replaces the body of the specified function in the specified module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c40e8-105">语法</span><span class="sxs-lookup"><span data-stu-id="c40e8-105">Syntax</span></span>  
  
```cpp  
HRESULT SetILFunctionBody(  
    [in] ModuleID    moduleId,  
    [in] mdMethodDef methodid,  
    [in] LPCBYTE     pbNewILMethodHeader);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c40e8-106">参数</span><span class="sxs-lookup"><span data-stu-id="c40e8-106">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="c40e8-107">中函数所在模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="c40e8-107">[in] The ID of the module in which the function resides.</span></span>  
  
 `methodid`  
 <span data-ttu-id="c40e8-108">中要替换其正文的函数的标记。</span><span class="sxs-lookup"><span data-stu-id="c40e8-108">[in] The token of the function for which to replace the body.</span></span>  
  
 `pbNewILMethodHeader`  
 <span data-ttu-id="c40e8-109">中函数的新标头。</span><span class="sxs-lookup"><span data-stu-id="c40e8-109">[in] The new header for the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c40e8-110">备注</span><span class="sxs-lookup"><span data-stu-id="c40e8-110">Remarks</span></span>  

 <span data-ttu-id="c40e8-111">`SetILFunctionBody`方法替换元数据中函数的相对虚拟地址，以使其指向新的函数体，并根据需要调整任何内部数据结构。</span><span class="sxs-lookup"><span data-stu-id="c40e8-111">The `SetILFunctionBody` method replaces the relative virtual address of the function in the metadata so that it points to the new function body, and adjusts any internal data structures as required.</span></span>  
  
 <span data-ttu-id="c40e8-112">`SetILFunctionBody`仅可对从未由实时 (JIT) 编译器编译的函数调用方法。。</span><span class="sxs-lookup"><span data-stu-id="c40e8-112">The `SetILFunctionBody` method can be called on only those functions that have never been compiled by a just-in-time (JIT) compiler.</span></span>  
  
 <span data-ttu-id="c40e8-113">使用 [ICorProfilerInfo：： GetILFunctionBodyAllocator](icorprofilerinfo-getilfunctionbodyallocator-method.md) 方法为新方法分配空间，以确保缓冲区兼容。</span><span class="sxs-lookup"><span data-stu-id="c40e8-113">Use the [ICorProfilerInfo::GetILFunctionBodyAllocator](icorprofilerinfo-getilfunctionbodyallocator-method.md) method to allocate space for the new method to ensure that the buffer is compatible.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c40e8-114">要求</span><span class="sxs-lookup"><span data-stu-id="c40e8-114">Requirements</span></span>  

 <span data-ttu-id="c40e8-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c40e8-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c40e8-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c40e8-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c40e8-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c40e8-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c40e8-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c40e8-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c40e8-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="c40e8-119">See also</span></span>

- [<span data-ttu-id="c40e8-120">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="c40e8-120">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
