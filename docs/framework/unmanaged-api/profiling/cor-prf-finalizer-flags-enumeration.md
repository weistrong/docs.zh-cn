---
description: 了解详细信息： COR_PRF_FINALIZER_FLAGS 枚举
title: COR_PRF_FINALIZER_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_FINALIZER_FLAGS
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_FINALIZER_FLAGS
helpviewer_keywords:
- COR_PRF_FINALIZER_FLAGS enumeration [.NET Framework profiling]
ms.assetid: 297d7721-3911-4f36-9e34-d9da0c33e22a
topic_type:
- apiref
ms.openlocfilehash: 96430b1ba3a38cce2801ed55f030395154c78dab
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649164"
---
# <a name="cor_prf_finalizer_flags-enumeration"></a><span data-ttu-id="06a5e-103">COR_PRF_FINALIZER_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="06a5e-103">COR_PRF_FINALIZER_FLAGS Enumeration</span></span>

<span data-ttu-id="06a5e-104">描述对象的终结器。</span><span class="sxs-lookup"><span data-stu-id="06a5e-104">Describes the finalizer for an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06a5e-105">语法</span><span class="sxs-lookup"><span data-stu-id="06a5e-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_FINALIZER_CRITICAL = 0x1  
} COR_PRF_FINALIZER_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="06a5e-106">成员</span><span class="sxs-lookup"><span data-stu-id="06a5e-106">Members</span></span>  
  
|<span data-ttu-id="06a5e-107">成员</span><span class="sxs-lookup"><span data-stu-id="06a5e-107">Member</span></span>|<span data-ttu-id="06a5e-108">说明</span><span class="sxs-lookup"><span data-stu-id="06a5e-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_FINALIZER_CRITICAL`|<span data-ttu-id="06a5e-109">终结器至关重要。</span><span class="sxs-lookup"><span data-stu-id="06a5e-109">The finalizer is critical.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="06a5e-110">备注</span><span class="sxs-lookup"><span data-stu-id="06a5e-110">Remarks</span></span>  

 <span data-ttu-id="06a5e-111">`COR_PRF_FINALIZER_FLAGS` [ICorProfilerCallback2：： FinalizeableObjectQueued](icorprofilercallback2-finalizeableobjectqueued-method.md)方法使用枚举来描述对象的终结器。</span><span class="sxs-lookup"><span data-stu-id="06a5e-111">The `COR_PRF_FINALIZER_FLAGS` enumeration is used by the [ICorProfilerCallback2::FinalizeableObjectQueued](icorprofilercallback2-finalizeableobjectqueued-method.md) method to describe the finalizer for an object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="06a5e-112">要求</span><span class="sxs-lookup"><span data-stu-id="06a5e-112">Requirements</span></span>  

 <span data-ttu-id="06a5e-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="06a5e-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="06a5e-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="06a5e-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="06a5e-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="06a5e-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="06a5e-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="06a5e-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06a5e-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="06a5e-117">See also</span></span>

- [<span data-ttu-id="06a5e-118">分析枚举</span><span class="sxs-lookup"><span data-stu-id="06a5e-118">Profiling Enumerations</span></span>](profiling-enumerations.md)
