---
description: 了解详细信息： COR_PRF_GC_ROOT_KIND 枚举
title: COR_PRF_GC_ROOT_KIND 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_GC_ROOT_KIND
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_GC_ROOT_KIND
helpviewer_keywords:
- COR_PRF_GC_ROOT_KIND enumeration [.NET Framework profiling]
ms.assetid: b9fb1c03-417f-41d4-aed4-02cb4ade8def
topic_type:
- apiref
ms.openlocfilehash: 148d48458c906974d76b9e0ec0cb6b4d15ee49ef
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648774"
---
# <a name="cor_prf_gc_root_kind-enumeration"></a><span data-ttu-id="ddd1a-103">COR_PRF_GC_ROOT_KIND 枚举</span><span class="sxs-lookup"><span data-stu-id="ddd1a-103">COR_PRF_GC_ROOT_KIND Enumeration</span></span>

<span data-ttu-id="ddd1a-104">指示由 [ICorProfilerCallback2：： RootReferences2](icorprofilercallback2-rootreferences2-method.md) 回调公开的垃圾回收根的类型。</span><span class="sxs-lookup"><span data-stu-id="ddd1a-104">Indicates the kind of garbage collection root that is exposed by the [ICorProfilerCallback2::RootReferences2](icorprofilercallback2-rootreferences2-method.md) callback.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ddd1a-105">语法</span><span class="sxs-lookup"><span data-stu-id="ddd1a-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_GC_ROOT_STACK = 1,  
    COR_PRF_GC_ROOT_FINALIZER = 2,  
    COR_PRF_GC_ROOT_HANDLE = 3,  
    COR_PRF_GC_ROOT_OTHER = 0  
} COR_PRF_GC_ROOT_KIND;  
```  
  
## <a name="members"></a><span data-ttu-id="ddd1a-106">成员</span><span class="sxs-lookup"><span data-stu-id="ddd1a-106">Members</span></span>  
  
|<span data-ttu-id="ddd1a-107">成员</span><span class="sxs-lookup"><span data-stu-id="ddd1a-107">Member</span></span>|<span data-ttu-id="ddd1a-108">说明</span><span class="sxs-lookup"><span data-stu-id="ddd1a-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_GC_ROOT_STACK`|<span data-ttu-id="ddd1a-109">根是堆栈上的变量。</span><span class="sxs-lookup"><span data-stu-id="ddd1a-109">The root is a variable on the stack.</span></span>|  
|`COR_PRF_GC_ROOT_FINALIZER`|<span data-ttu-id="ddd1a-110">根是终结器队列中的条目。</span><span class="sxs-lookup"><span data-stu-id="ddd1a-110">The root is an entry in the finalizer queue.</span></span>|  
|`COR_PRF_GC_ROOT_HANDLE`|<span data-ttu-id="ddd1a-111">根为垃圾回收句柄。</span><span class="sxs-lookup"><span data-stu-id="ddd1a-111">The root is a garbage collection handle.</span></span>|  
|`COR_PRF_GC_ROOT_OTHER`|<span data-ttu-id="ddd1a-112">根的类型未指定。</span><span class="sxs-lookup"><span data-stu-id="ddd1a-112">The kind of root is unspecified.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ddd1a-113">要求</span><span class="sxs-lookup"><span data-stu-id="ddd1a-113">Requirements</span></span>  

 <span data-ttu-id="ddd1a-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ddd1a-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ddd1a-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ddd1a-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ddd1a-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ddd1a-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ddd1a-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ddd1a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ddd1a-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="ddd1a-118">See also</span></span>

- [<span data-ttu-id="ddd1a-119">分析枚举</span><span class="sxs-lookup"><span data-stu-id="ddd1a-119">Profiling Enumerations</span></span>](profiling-enumerations.md)
