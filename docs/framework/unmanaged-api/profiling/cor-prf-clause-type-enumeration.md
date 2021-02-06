---
description: 了解详细信息： COR_PRF_CLAUSE_TYPE 枚举
title: COR_PRF_CLAUSE_TYPE 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_CLAUSE_TYPE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_CLAUSE_TYPE
helpviewer_keywords:
- COR_PRF_CLAUSE_TYPE enumeration [.NET Framework profiling]
ms.assetid: f64c325a-ed3a-4aaf-b847-a88edbc4fefc
topic_type:
- apiref
ms.openlocfilehash: 413dbc0ad94e4ab670cd7cd9537bbd1735ffd7cf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649255"
---
# <a name="cor_prf_clause_type-enumeration"></a><span data-ttu-id="6cece-103">COR_PRF_CLAUSE_TYPE 枚举</span><span class="sxs-lookup"><span data-stu-id="6cece-103">COR_PRF_CLAUSE_TYPE Enumeration</span></span>

<span data-ttu-id="6cece-104">指示代码刚进入或离开的异常子句的类型。</span><span class="sxs-lookup"><span data-stu-id="6cece-104">Indicates the type of exception clause that the code has just entered or left.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6cece-105">语法</span><span class="sxs-lookup"><span data-stu-id="6cece-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_CLAUSE_NONE = 0,  
    COR_PRF_CLAUSE_FILTER = 1,  
    COR_PRF_CLAUSE_CATCH = 2,  
    COR_PRF_CLAUSE_FINALLY = 3,  
} COR_PRF_CLAUSE_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="6cece-106">成员</span><span class="sxs-lookup"><span data-stu-id="6cece-106">Members</span></span>  
  
|<span data-ttu-id="6cece-107">成员</span><span class="sxs-lookup"><span data-stu-id="6cece-107">Member</span></span>|<span data-ttu-id="6cece-108">说明</span><span class="sxs-lookup"><span data-stu-id="6cece-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_CLAUSE_NONE`|<span data-ttu-id="6cece-109">异常子句无效。</span><span class="sxs-lookup"><span data-stu-id="6cece-109">The exception clause is not valid.</span></span>|  
|`COR_PRF_CLAUSE_FILTER`|<span data-ttu-id="6cece-110">Exception 子句是一个筛选器表达式。</span><span class="sxs-lookup"><span data-stu-id="6cece-110">The exception clause is a filter expression.</span></span>|  
|`COR_PRF_CLAUSE_CATCH`|<span data-ttu-id="6cece-111">Exception 子句为 `catch` 语句。</span><span class="sxs-lookup"><span data-stu-id="6cece-111">The exception clause is a `catch` statement.</span></span>|  
|`COR_PRF_CLAUSE_FINALLY`|<span data-ttu-id="6cece-112">Exception 子句为 `finally` 语句。</span><span class="sxs-lookup"><span data-stu-id="6cece-112">The exception clause is a `finally` statement.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6cece-113">要求</span><span class="sxs-lookup"><span data-stu-id="6cece-113">Requirements</span></span>  

 <span data-ttu-id="6cece-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6cece-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6cece-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="6cece-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="6cece-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6cece-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6cece-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6cece-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6cece-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="6cece-118">See also</span></span>

- [<span data-ttu-id="6cece-119">分析枚举</span><span class="sxs-lookup"><span data-stu-id="6cece-119">Profiling Enumerations</span></span>](profiling-enumerations.md)
