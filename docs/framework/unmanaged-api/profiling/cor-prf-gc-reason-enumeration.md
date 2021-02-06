---
description: 了解详细信息： COR_PRF_GC_REASON 枚举
title: COR_PRF_GC_REASON 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_GC_REASON
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_GC_REASON
helpviewer_keywords:
- COR_PRF_GC_REASON enumeration [.NET Framework profiling]
ms.assetid: 72822b95-a7fb-485e-9d55-1cb016d9a458
topic_type:
- apiref
ms.openlocfilehash: f5c8201f2023e07f9bb9d540f6d5f8fca1c19419
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648787"
---
# <a name="cor_prf_gc_reason-enumeration"></a><span data-ttu-id="1207f-103">COR_PRF_GC_REASON 枚举</span><span class="sxs-lookup"><span data-stu-id="1207f-103">COR_PRF_GC_REASON Enumeration</span></span>

<span data-ttu-id="1207f-104">指示当前发生垃圾回收的原因。</span><span class="sxs-lookup"><span data-stu-id="1207f-104">Indicates the reason that garbage collection is occurring.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1207f-105">语法</span><span class="sxs-lookup"><span data-stu-id="1207f-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_GC_INDUCED = 1,  
    COR_PRF_GC_OTHER = 0  
} COR_PRF_GC_REASON;  
```  
  
## <a name="members"></a><span data-ttu-id="1207f-106">成员</span><span class="sxs-lookup"><span data-stu-id="1207f-106">Members</span></span>  
  
|<span data-ttu-id="1207f-107">成员</span><span class="sxs-lookup"><span data-stu-id="1207f-107">Member</span></span>|<span data-ttu-id="1207f-108">说明</span><span class="sxs-lookup"><span data-stu-id="1207f-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_GC_INDUCED`|<span data-ttu-id="1207f-109">垃圾回收由 <xref:System.GC.Collect%2A> 方法引起。</span><span class="sxs-lookup"><span data-stu-id="1207f-109">The garbage collection was induced by a <xref:System.GC.Collect%2A> method.</span></span>|  
|`COR_PRF_GC_OTHER`|<span data-ttu-id="1207f-110">原因未指定。</span><span class="sxs-lookup"><span data-stu-id="1207f-110">The reason is unspecified.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1207f-111">要求</span><span class="sxs-lookup"><span data-stu-id="1207f-111">Requirements</span></span>  

 <span data-ttu-id="1207f-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1207f-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1207f-113">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="1207f-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="1207f-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1207f-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1207f-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1207f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1207f-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="1207f-116">See also</span></span>

- [<span data-ttu-id="1207f-117">分析枚举</span><span class="sxs-lookup"><span data-stu-id="1207f-117">Profiling Enumerations</span></span>](profiling-enumerations.md)
