---
description: 了解详细信息： COR_PRF_FUNCTION_ARGUMENT_RANGE 结构
title: COR_PRF_FUNCTION_ARGUMENT_RANGE 结构
ms.date: 03/30/2017
api_name:
- COR_PRF_FUNCTION_ARGUMENT_RANGE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_FUNCTION_ARGUMENT_RANGE
helpviewer_keywords:
- COR_PRF_FUNCTION_ARGUMENT_RANGE structure [.NET Framework profiling'
ms.assetid: 9f469eac-ac66-419b-8668-fe705bc1a51f
topic_type:
- apiref
ms.openlocfilehash: 65d762ba4513341b20426ea56d423a2066f6e714
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649008"
---
# <a name="cor_prf_function_argument_range-structure"></a><span data-ttu-id="c31bf-103">COR_PRF_FUNCTION_ARGUMENT_RANGE 结构</span><span class="sxs-lookup"><span data-stu-id="c31bf-103">COR_PRF_FUNCTION_ARGUMENT_RANGE Structure</span></span>

<span data-ttu-id="c31bf-104">表示内存中按从左向右的顺序连续存储的函数自变量块。</span><span class="sxs-lookup"><span data-stu-id="c31bf-104">Represents a block of function arguments stored contiguously in left-to-right order in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c31bf-105">语法</span><span class="sxs-lookup"><span data-stu-id="c31bf-105">Syntax</span></span>  
  
```cpp  
typedef struct _COR_PRF_FUNCTION_ARGUMENT_RANGE {  
    UINT_PTR startAddress;  
    ULONG length;  
} COR_PRF_FUNCTION_ARGUMENT_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="c31bf-106">成员</span><span class="sxs-lookup"><span data-stu-id="c31bf-106">Members</span></span>  
  
|<span data-ttu-id="c31bf-107">成员</span><span class="sxs-lookup"><span data-stu-id="c31bf-107">Members</span></span>|<span data-ttu-id="c31bf-108">说明</span><span class="sxs-lookup"><span data-stu-id="c31bf-108">Description</span></span>|  
|-------------|-----------------|  
|`startAddress`|<span data-ttu-id="c31bf-109">块的起始地址。</span><span class="sxs-lookup"><span data-stu-id="c31bf-109">The starting address of the block.</span></span>|  
|`length`|<span data-ttu-id="c31bf-110">连续块的长度。</span><span class="sxs-lookup"><span data-stu-id="c31bf-110">The length of the contiguous block.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c31bf-111">要求</span><span class="sxs-lookup"><span data-stu-id="c31bf-111">Requirements</span></span>  

 <span data-ttu-id="c31bf-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c31bf-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c31bf-113">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="c31bf-113">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="c31bf-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c31bf-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c31bf-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c31bf-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c31bf-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="c31bf-116">See also</span></span>

- [<span data-ttu-id="c31bf-117">分析结构</span><span class="sxs-lookup"><span data-stu-id="c31bf-117">Profiling Structures</span></span>](profiling-structures.md)
