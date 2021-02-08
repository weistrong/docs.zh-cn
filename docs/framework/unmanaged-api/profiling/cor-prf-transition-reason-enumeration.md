---
description: 了解详细信息： COR_PRF_TRANSITION_REASON 枚举
title: COR_PRF_TRANSITION_REASON 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_TRANSITION_REASON
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_TRANSITION_REASON
helpviewer_keywords:
- COR_PRF_TRANSITION_REASON enumeration [.NET Framework profiling]
ms.assetid: da941118-01b7-4197-ae5b-9f2f8adcd623
topic_type:
- apiref
ms.openlocfilehash: 8d0b7852f80f80a47f910e9f1240a5315772cd23
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788990"
---
# <a name="cor_prf_transition_reason-enumeration"></a><span data-ttu-id="bfb59-103">COR_PRF_TRANSITION_REASON 枚举</span><span class="sxs-lookup"><span data-stu-id="bfb59-103">COR_PRF_TRANSITION_REASON Enumeration</span></span>

<span data-ttu-id="bfb59-104">指示从托管代码向非托管代码转换或从非托管代码向托管代码转换的原因。</span><span class="sxs-lookup"><span data-stu-id="bfb59-104">Indicates the reason for a transition from managed to unmanaged code, or vice versa.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bfb59-105">语法</span><span class="sxs-lookup"><span data-stu-id="bfb59-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_TRANSITION_CALL,  
    COR_PRF_TRANSITION_RETURN  
} COR_PRF_TRANSITION_REASON;  
```  
  
## <a name="members"></a><span data-ttu-id="bfb59-106">成员</span><span class="sxs-lookup"><span data-stu-id="bfb59-106">Members</span></span>  
  
|<span data-ttu-id="bfb59-107">成员</span><span class="sxs-lookup"><span data-stu-id="bfb59-107">Member</span></span>|<span data-ttu-id="bfb59-108">说明</span><span class="sxs-lookup"><span data-stu-id="bfb59-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_TRANSITION_CALL`|<span data-ttu-id="bfb59-109">由于调用了函数，因此转换。</span><span class="sxs-lookup"><span data-stu-id="bfb59-109">The transition is due to a call into a function.</span></span>|  
|`COR_PRF_TRANSITION_RETURN`|<span data-ttu-id="bfb59-110">由于从函数返回，因此转换。</span><span class="sxs-lookup"><span data-stu-id="bfb59-110">The transition is due to a return from a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bfb59-111">备注</span><span class="sxs-lookup"><span data-stu-id="bfb59-111">Remarks</span></span>  

 <span data-ttu-id="bfb59-112">发生转换时，探查器会接收 [ICorProfilerCallback：： ManagedToUnmanagedTransition](icorprofilercallback-managedtounmanagedtransition-method.md) 或 [ICorProfilerCallback：： UnmanagedToManagedTransition](icorprofilercallback-unmanagedtomanagedtransition-method.md) 回调，其中任何一个都提供枚举的值， `COR_PRF_TRANSITION_REASON` 以指示转换的原因。</span><span class="sxs-lookup"><span data-stu-id="bfb59-112">When a transition occurs, the profiler receives an [ICorProfilerCallback::ManagedToUnmanagedTransition](icorprofilercallback-managedtounmanagedtransition-method.md) or [ICorProfilerCallback::UnmanagedToManagedTransition](icorprofilercallback-unmanagedtomanagedtransition-method.md) callback, either of which provides a value of the `COR_PRF_TRANSITION_REASON` enumeration to indicate the reason for the transition.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bfb59-113">要求</span><span class="sxs-lookup"><span data-stu-id="bfb59-113">Requirements</span></span>  

 <span data-ttu-id="bfb59-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bfb59-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bfb59-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="bfb59-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="bfb59-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bfb59-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bfb59-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bfb59-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
