---
description: 了解详细信息： COR_PRF_EX_CLAUSE_INFO 结构
title: COR_PRF_EX_CLAUSE_INFO 结构
ms.date: 03/30/2017
api_name:
- COR_PRF_EX_CLAUSE_INFO
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_EX_CLAUSE_INFO
helpviewer_keywords:
- COR_PRF_EX_CLAUSE_INFO structure [.NET Framework profiling]
ms.assetid: 7d0d6fb7-bc9d-40f0-8163-c0d162eaba7d
topic_type:
- apiref
ms.openlocfilehash: af8d404e55a8996abc69923924e87c95e3c5eae8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649187"
---
# <a name="cor_prf_ex_clause_info-structure"></a><span data-ttu-id="86aad-103">COR_PRF_EX_CLAUSE_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="86aad-103">COR_PRF_EX_CLAUSE_INFO Structure</span></span>

<span data-ttu-id="86aad-104">存储有关特定的异常子句实例及其关联的帧的信息。</span><span class="sxs-lookup"><span data-stu-id="86aad-104">Stores information about a specific exception clause instance and its associated frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86aad-105">语法</span><span class="sxs-lookup"><span data-stu-id="86aad-105">Syntax</span></span>  
  
```cpp  
typedef struct COR_PRF_EX_CLAUSE_INFO {  
    COR_PRF_CLAUSE_TYPE clauseType;  
    UINT_PTR programCounter;  
    UINT_PTR framePointer;  
    UINT_PTR shadowStackPointer;  
} COR_PRF_EX_CLAUSE_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="86aad-106">成员</span><span class="sxs-lookup"><span data-stu-id="86aad-106">Members</span></span>  
  
|<span data-ttu-id="86aad-107">成员</span><span class="sxs-lookup"><span data-stu-id="86aad-107">Member</span></span>|<span data-ttu-id="86aad-108">说明</span><span class="sxs-lookup"><span data-stu-id="86aad-108">Description</span></span>|  
|------------|-----------------|  
|`clauseType`|<span data-ttu-id="86aad-109">一个 [COR_PRF_CLAUSE_TYPE](cor-prf-clause-type-enumeration.md) 枚举的值，该值指定代码刚刚进入或离开的异常子句的类型。</span><span class="sxs-lookup"><span data-stu-id="86aad-109">A value of the [COR_PRF_CLAUSE_TYPE](cor-prf-clause-type-enumeration.md) enumeration that specifies the type of exception clause the code just entered or left.</span></span>|  
|`programCounter`|<span data-ttu-id="86aad-110">子句处理程序的本地入口点（例如 X86 EIP 寄存器的内容）。</span><span class="sxs-lookup"><span data-stu-id="86aad-110">The native entry point of the clause handler — for example, the contents of the X86 EIP register.</span></span>|  
|`framePointer`|<span data-ttu-id="86aad-111">指向子句处理程序的逻辑帧的指针，例如 X86 EBP 寄存器的内容。</span><span class="sxs-lookup"><span data-stu-id="86aad-111">The pointer to the logical frame for the clause handler — for example, the contents of the X86 EBP register.</span></span>|  
|`shadowStackPointer`|<span data-ttu-id="86aad-112">指向阴影堆栈的指针。</span><span class="sxs-lookup"><span data-stu-id="86aad-112">The pointer to the shadow stack.</span></span> <span data-ttu-id="86aad-113">此值为 BSP 寄存器的内容，并且仅适用于 IA64。</span><span class="sxs-lookup"><span data-stu-id="86aad-113">This value is the contents of the BSP register and applies only to IA64.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="86aad-114">备注</span><span class="sxs-lookup"><span data-stu-id="86aad-114">Remarks</span></span>  

 <span data-ttu-id="86aad-115">收到异常通知时， [ICorProfilerInfo2：： GetNotifiedExceptionClauseInfo](icorprofilerinfo2-getnotifiedexceptionclauseinfo-method.md)可用于获取异常子句的本机地址和帧信息， (要 `catch` / `finally` 运行或刚刚运行的/filter) 。</span><span class="sxs-lookup"><span data-stu-id="86aad-115">When an exception notification is received, [ICorProfilerInfo2::GetNotifiedExceptionClauseInfo](icorprofilerinfo2-getnotifiedexceptionclauseinfo-method.md) can be used to get the native address and frame information for the exception clause (`catch`/`finally`/filter) that is about to be run or has just been run.</span></span>  
  
 <span data-ttu-id="86aad-116">执行 exception 子句涉及到公共语言运行时 (CLR) 的回调：</span><span class="sxs-lookup"><span data-stu-id="86aad-116">Execution of an exception clause involves these callbacks from the common language runtime (CLR):</span></span>  
  
- [<span data-ttu-id="86aad-117">ICorProfilerCallback：： ExceptionCatcherEnter</span><span class="sxs-lookup"><span data-stu-id="86aad-117">ICorProfilerCallback::ExceptionCatcherEnter</span></span>](icorprofilercallback-exceptioncatcherenter-method.md)  
  
- [<span data-ttu-id="86aad-118">ICorProfilerCallback：： ExceptionUnwindFinallyEnter</span><span class="sxs-lookup"><span data-stu-id="86aad-118">ICorProfilerCallback::ExceptionUnwindFinallyEnter</span></span>](icorprofilercallback-exceptionunwindfinallyenter-method.md)  
  
- [<span data-ttu-id="86aad-119">ICorProfilerCallback：： ExceptionSearchFilterEnter</span><span class="sxs-lookup"><span data-stu-id="86aad-119">ICorProfilerCallback::ExceptionSearchFilterEnter</span></span>](icorprofilercallback-exceptionsearchfilterenter-method.md)  
  
- [<span data-ttu-id="86aad-120">ICorProfilerCallback：： ExceptionCatcherLeave</span><span class="sxs-lookup"><span data-stu-id="86aad-120">ICorProfilerCallback::ExceptionCatcherLeave</span></span>](icorprofilercallback-exceptioncatcherleave-method.md)  
  
- [<span data-ttu-id="86aad-121">ICorProfilerCallback：： ExceptionUnwindFinallyLeave</span><span class="sxs-lookup"><span data-stu-id="86aad-121">ICorProfilerCallback::ExceptionUnwindFinallyLeave</span></span>](icorprofilercallback-exceptionunwindfinallyleave-method.md)  
  
- [<span data-ttu-id="86aad-122">ICorProfilerCallback：： ExceptionSearchFilterLeave</span><span class="sxs-lookup"><span data-stu-id="86aad-122">ICorProfilerCallback::ExceptionSearchFilterLeave</span></span>](icorprofilercallback-exceptionsearchfilterleave-method.md)  
  
## <a name="requirements"></a><span data-ttu-id="86aad-123">要求</span><span class="sxs-lookup"><span data-stu-id="86aad-123">Requirements</span></span>  

 <span data-ttu-id="86aad-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="86aad-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86aad-125">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="86aad-125">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="86aad-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="86aad-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="86aad-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="86aad-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86aad-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="86aad-128">See also</span></span>

- [<span data-ttu-id="86aad-129">分析结构</span><span class="sxs-lookup"><span data-stu-id="86aad-129">Profiling Structures</span></span>](profiling-structures.md)
