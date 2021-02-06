---
description: 了解详细信息： COR_PRF_CODEGEN_FLAGS 枚举
title: COR_PRF_CODEGEN_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_CODEGEN_FLAGS
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_CODEGEN_FLAGS
helpviewer_keywords:
- COR_PRF_CODEGEN_FLAGS enumeration [.NET Framework profiling]
ms.assetid: 3e184022-0247-4824-a23d-6b29593d8d01
topic_type:
- apiref
ms.openlocfilehash: 40ddaa77047e0b1daa743b512f21ba7643127230
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649170"
---
# <a name="cor_prf_codegen_flags-enumeration"></a><span data-ttu-id="b732b-103">COR_PRF_CODEGEN_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="b732b-103">COR_PRF_CODEGEN_FLAGS Enumeration</span></span>

<span data-ttu-id="b732b-104">定义可以用 [ICorProfilerFunctionControl：： SetCodegenFlags](icorprofilerfunctioncontrol-setcodegenflags-method.md) 方法设置的代码生成标志。</span><span class="sxs-lookup"><span data-stu-id="b732b-104">Defines the code generation flags that can be set with the [ICorProfilerFunctionControl::SetCodegenFlags](icorprofilerfunctioncontrol-setcodegenflags-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b732b-105">语法</span><span class="sxs-lookup"><span data-stu-id="b732b-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_CODEGEN_DISABLE_INLINING =          0x0001,  
    COR_PRF_CODEGEN_DISABLE_ALL_OPTIMIZATIONS = 0x0002,  
} COR_PRF_CODEGEN_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="b732b-106">成员</span><span class="sxs-lookup"><span data-stu-id="b732b-106">Members</span></span>  
  
|<span data-ttu-id="b732b-107">成员</span><span class="sxs-lookup"><span data-stu-id="b732b-107">Member</span></span>|<span data-ttu-id="b732b-108">说明</span><span class="sxs-lookup"><span data-stu-id="b732b-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_CODEGEN_DISABLE_INLINING`|<span data-ttu-id="b732b-109">不会将任何函数内联到此函数的主体中。</span><span class="sxs-lookup"><span data-stu-id="b732b-109">No functions will be inlined into this function’s body.</span></span> <span data-ttu-id="b732b-110">但是，函数本身可能会内联到其调用方。</span><span class="sxs-lookup"><span data-stu-id="b732b-110">However, the function itself may be inlined into its callers.</span></span>|  
|`COR_PRF_CODEGEN_DISABLE_ALL_OPTIMIZATIONS`|<span data-ttu-id="b732b-111">对于此函数的主体，将禁用所有优化。</span><span class="sxs-lookup"><span data-stu-id="b732b-111">All optimizations will be disabled for this function’s body.</span></span> <span data-ttu-id="b732b-112">但是，该函数本身可能仍会内联到其调用方。</span><span class="sxs-lookup"><span data-stu-id="b732b-112">However, the function itself may still be inlined into its callers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b732b-113">备注</span><span class="sxs-lookup"><span data-stu-id="b732b-113">Remarks</span></span>  

 <span data-ttu-id="b732b-114">`COR_PRF_CODEGEN_FLAGS` [ICorProfilerFunctionControl：： SetCodegenFlags](icorprofilerfunctioncontrol-setcodegenflags-method.md)方法使用枚举来启用探查器，以控制 JIT 重新编译函数的代码生成。</span><span class="sxs-lookup"><span data-stu-id="b732b-114">The `COR_PRF_CODEGEN_FLAGS` enumeration is used by the [ICorProfilerFunctionControl::SetCodegenFlags](icorprofilerfunctioncontrol-setcodegenflags-method.md) method to enable the profiler to control the code generation for the JIT-recompiled function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b732b-115">要求</span><span class="sxs-lookup"><span data-stu-id="b732b-115">Requirements</span></span>  

 <span data-ttu-id="b732b-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b732b-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b732b-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b732b-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b732b-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b732b-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b732b-119">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b732b-119">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b732b-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="b732b-120">See also</span></span>

- [<span data-ttu-id="b732b-121">分析枚举</span><span class="sxs-lookup"><span data-stu-id="b732b-121">Profiling Enumerations</span></span>](profiling-enumerations.md)
