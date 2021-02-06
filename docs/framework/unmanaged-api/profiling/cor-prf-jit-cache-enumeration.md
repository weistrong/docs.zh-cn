---
description: 了解详细信息： COR_PRF_JIT_CACHE 枚举
title: COR_PRF_JIT_CACHE 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_JIT_CACHE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_JIT_CACHE
helpviewer_keywords:
- COR_PRF_JIT_CACHE enumeration [.NET Framework profiling]
ms.assetid: e7b8f6b4-95bc-4ba5-b9eb-f5590a7326a4
topic_type:
- apiref
ms.openlocfilehash: 94b04b42504760be826f78cee0da3066f1936f32
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648748"
---
# <a name="cor_prf_jit_cache-enumeration"></a><span data-ttu-id="8b175-103">COR_PRF_JIT_CACHE 枚举</span><span class="sxs-lookup"><span data-stu-id="8b175-103">COR_PRF_JIT_CACHE Enumeration</span></span>

<span data-ttu-id="8b175-104">指示缓存的函数搜索的结果。</span><span class="sxs-lookup"><span data-stu-id="8b175-104">Indicates the result of a cached function search.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="8b175-105">`COR_PRF_CACHED_FUNCTION_FOUND` 的值为零，因此 `COR_PRF_JIT_CACHE` 不能用作布尔代理项。</span><span class="sxs-lookup"><span data-stu-id="8b175-105">`COR_PRF_CACHED_FUNCTION_FOUND` has a value of zero, so `COR_PRF_JIT_CACHE` cannot be used as a Boolean surrogate.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b175-106">语法</span><span class="sxs-lookup"><span data-stu-id="8b175-106">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_CACHED_FUNCTION_FOUND,  
    COR_PRF_CACHED_FUNCTION_NOT_FOUND  
} COR_PRF_JIT_CACHE;  
```  
  
## <a name="members"></a><span data-ttu-id="8b175-107">成员</span><span class="sxs-lookup"><span data-stu-id="8b175-107">Members</span></span>  
  
|<span data-ttu-id="8b175-108">成员</span><span class="sxs-lookup"><span data-stu-id="8b175-108">Member</span></span>|<span data-ttu-id="8b175-109">说明</span><span class="sxs-lookup"><span data-stu-id="8b175-109">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_FUNCTION_FOUND`|<span data-ttu-id="8b175-110">搜索找到函数。</span><span class="sxs-lookup"><span data-stu-id="8b175-110">The search found the function.</span></span>|  
|`COR_PRF_FUNCTION_NOT_FOUND`|<span data-ttu-id="8b175-111">搜索找不到函数。</span><span class="sxs-lookup"><span data-stu-id="8b175-111">The search did not find the function.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8b175-112">要求</span><span class="sxs-lookup"><span data-stu-id="8b175-112">Requirements</span></span>  

 <span data-ttu-id="8b175-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8b175-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8b175-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8b175-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8b175-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8b175-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8b175-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8b175-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b175-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="8b175-117">See also</span></span>

- [<span data-ttu-id="8b175-118">分析枚举</span><span class="sxs-lookup"><span data-stu-id="8b175-118">Profiling Enumerations</span></span>](profiling-enumerations.md)
