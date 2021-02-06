---
description: 了解详细信息： COR_PRF_FUNCTION 结构
title: COR_PRF_FUNCTION 结构
ms.date: 03/30/2017
api_name:
- COR_PRF_FUNCTION
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_FUNCTION
helpviewer_keywords:
- COR_PRF_FUNCTION structure [.NET Framework profiling]
ms.assetid: 8bb5acf5-cf4b-4ccb-93f1-46db1f3f8bf3
topic_type:
- apiref
ms.openlocfilehash: 494f3cfe6d1e3641645ef0050c06014e67bf4475
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648969"
---
# <a name="cor_prf_function-structure"></a><span data-ttu-id="e5189-103">COR_PRF_FUNCTION 结构</span><span class="sxs-lookup"><span data-stu-id="e5189-103">COR_PRF_FUNCTION Structure</span></span>

<span data-ttu-id="e5189-104">通过将函数的 ID 与其重新编译的 ID 版本组合起来，提供该函数的唯一表示形式。</span><span class="sxs-lookup"><span data-stu-id="e5189-104">Provides a unique representation of a function by combining its ID with the ID of its recompiled version.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5189-105">语法</span><span class="sxs-lookup"><span data-stu-id="e5189-105">Syntax</span></span>  
  
```cpp  
typedef struct _COR_PRF_FUNCTION {    FunctionID functionId;    ReJITID    reJitId;} COR_PRF_FUNCTION;  
```  
  
## <a name="members"></a><span data-ttu-id="e5189-106">成员</span><span class="sxs-lookup"><span data-stu-id="e5189-106">Members</span></span>  
  
|<span data-ttu-id="e5189-107">成员</span><span class="sxs-lookup"><span data-stu-id="e5189-107">Member</span></span>|<span data-ttu-id="e5189-108">说明</span><span class="sxs-lookup"><span data-stu-id="e5189-108">Description</span></span>|  
|------------|-----------------|  
|`functionId`|<span data-ttu-id="e5189-109">函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="e5189-109">The ID of the function.</span></span>|  
|`reJitId`|<span data-ttu-id="e5189-110">重新编译的函数的 ID。</span><span class="sxs-lookup"><span data-stu-id="e5189-110">The ID of the recompiled function.</span></span> <span data-ttu-id="e5189-111">值 0 (零) 表示函数的原始版本。</span><span class="sxs-lookup"><span data-stu-id="e5189-111">A value of 0 (zero) represents the original version of the function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e5189-112">备注</span><span class="sxs-lookup"><span data-stu-id="e5189-112">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5189-113">要求</span><span class="sxs-lookup"><span data-stu-id="e5189-113">Requirements</span></span>  

 <span data-ttu-id="e5189-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e5189-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5189-115">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="e5189-115">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="e5189-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e5189-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e5189-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5189-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5189-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="e5189-118">See also</span></span>

- [<span data-ttu-id="e5189-119">分析结构</span><span class="sxs-lookup"><span data-stu-id="e5189-119">Profiling Structures</span></span>](profiling-structures.md)
