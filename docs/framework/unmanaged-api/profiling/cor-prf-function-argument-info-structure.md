---
description: 了解详细信息： COR_PRF_FUNCTION_ARGUMENT_INFO 结构
title: COR_PRF_FUNCTION_ARGUMENT_INFO 结构
ms.date: 03/30/2017
api_name:
- COR_PRF_FUNCTION_ARGUMENT_INFO
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_FUNCTION_ARGUMENT_INFO
helpviewer_keywords:
- COR_PRF_FUNCTION_ARGUMENT_INFO structure [.NET Framework profiling]
ms.assetid: 07cf3bab-e193-4991-8205-3f41cf2d67b3
topic_type:
- apiref
ms.openlocfilehash: c40c9b20dad79fa36a1ed4471106a54f2c55b422
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649060"
---
# <a name="cor_prf_function_argument_info-structure"></a><span data-ttu-id="8a2cb-103">COR_PRF_FUNCTION_ARGUMENT_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="8a2cb-103">COR_PRF_FUNCTION_ARGUMENT_INFO Structure</span></span>

<span data-ttu-id="8a2cb-104">按从左向右的顺序表示函数的参数。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-104">Represents a function's arguments, in left-to-right order.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a2cb-105">语法</span><span class="sxs-lookup"><span data-stu-id="8a2cb-105">Syntax</span></span>  
  
```cpp  
typedef struct _COR_PRF_FUNCTION_ARGUMENT_INFO {  
    ULONG numRanges;  
    ULONG totalArgumentSize;  
    COR_PRF_FUNCTION_ARGUMENT_RANGE ranges[1];  
} COR_PRF_FUNCTION_ARGUMENT_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="8a2cb-106">成员</span><span class="sxs-lookup"><span data-stu-id="8a2cb-106">Members</span></span>  
  
|<span data-ttu-id="8a2cb-107">成员</span><span class="sxs-lookup"><span data-stu-id="8a2cb-107">Member</span></span>|<span data-ttu-id="8a2cb-108">说明</span><span class="sxs-lookup"><span data-stu-id="8a2cb-108">Description</span></span>|  
|------------|-----------------|  
|`numRanges`|<span data-ttu-id="8a2cb-109">参数块的数目。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-109">The number of blocks of arguments.</span></span> <span data-ttu-id="8a2cb-110">也就是说，此值是数组中 [COR_PRF_FUNCTION_ARGUMENT_RANGE](cor-prf-function-argument-range-structure.md) 的结构数 `ranges` 。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-110">That is, this value is the number of [COR_PRF_FUNCTION_ARGUMENT_RANGE](cor-prf-function-argument-range-structure.md) structures in the `ranges` array.</span></span>|  
|`totalArgumentSize`|<span data-ttu-id="8a2cb-111">所有参数的总大小。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-111">The total size of all arguments.</span></span> <span data-ttu-id="8a2cb-112">换言之，此值是自变量长度之和。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-112">In other words, this value is the sum of the argument lengths.</span></span>|  
|`ranges`|<span data-ttu-id="8a2cb-113">结构的数组 `COR_PRF_FUNCTION_ARGUMENT_RANGE` ，其中每个结构都表示一个函数参数块。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-113">An array of `COR_PRF_FUNCTION_ARGUMENT_RANGE` structures, each of which represents one block of function arguments.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8a2cb-114">备注</span><span class="sxs-lookup"><span data-stu-id="8a2cb-114">Remarks</span></span>  

 <span data-ttu-id="8a2cb-115">函数可以包含多个参数。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-115">A function may have many arguments.</span></span> <span data-ttu-id="8a2cb-116">这些参数可能不会连续存储在内存中。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-116">Those arguments might not be stored contiguously in memory.</span></span> <span data-ttu-id="8a2cb-117">在一个位置，您可能有一个包含三个自变量的块、另一个位置中的两个参数块，以及在不同位置中的一个自变量的最后一个块。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-117">You might have a block of three arguments in one place, a block of two arguments in another place, and a final block of one argument in a different place.</span></span> <span data-ttu-id="8a2cb-118">这些参数全部用于相同的函数;它们只是存储在不同的位置。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-118">These arguments are all for the same function; they're just stored in different places.</span></span>  
  
 <span data-ttu-id="8a2cb-119">`COR_PRF_FUNCTION_ARGUMENT_INFO`结构表示一个函数的所有自变量。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-119">The `COR_PRF_FUNCTION_ARGUMENT_INFO` structure represents all the arguments of a single function.</span></span> <span data-ttu-id="8a2cb-120">它使用数组引用函数参数的所有块。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-120">It uses an array to reference all the blocks of function arguments.</span></span> <span data-ttu-id="8a2cb-121">因此，对于单个函数，你有一个 `COR_PRF_FUNCTION_ARGUMENT_INFO` 结构，它引用多个 `COR_PRF_FUNCTION_ARGUMENT_RANGE` 结构，其中每个结构都指向一个或多个函数自变量。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-121">So, for a single function, you have a single `COR_PRF_FUNCTION_ARGUMENT_INFO` structure, which references multiple `COR_PRF_FUNCTION_ARGUMENT_RANGE` structures, each of which points to one or more function arguments.</span></span>  
  
 <span data-ttu-id="8a2cb-122">存储在寄存器中的参数会溢出到内存中以生成结构。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-122">Arguments that are stored in registers are spilled into memory to build the structures.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a2cb-123">要求</span><span class="sxs-lookup"><span data-stu-id="8a2cb-123">Requirements</span></span>  

 <span data-ttu-id="8a2cb-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8a2cb-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a2cb-125">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="8a2cb-125">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="8a2cb-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8a2cb-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8a2cb-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a2cb-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a2cb-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="8a2cb-128">See also</span></span>

- [<span data-ttu-id="8a2cb-129">分析结构</span><span class="sxs-lookup"><span data-stu-id="8a2cb-129">Profiling Structures</span></span>](profiling-structures.md)
