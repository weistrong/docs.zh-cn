---
description: 了解详细信息： COR_IL_MAP 结构
title: COR_IL_MAP 结构
ms.date: 03/30/2017
api_name:
- COR_IL_MAP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_IL_MAP
helpviewer_keywords:
- COR_IL_MAP structure [.NET Framework debugging]
ms.assetid: 534ebc17-963d-4b26-8375-8cd940281db3
topic_type:
- apiref
ms.openlocfilehash: ff3d636429f51119342baea5d71163eb9d764e03
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712310"
---
# <a name="cor_il_map-structure"></a><span data-ttu-id="e768c-103">COR_IL_MAP 结构</span><span class="sxs-lookup"><span data-stu-id="e768c-103">COR_IL_MAP Structure</span></span>

<span data-ttu-id="e768c-104">指定函数的相对偏移量的更改。</span><span class="sxs-lookup"><span data-stu-id="e768c-104">Specifies changes in the relative offset of a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e768c-105">语法</span><span class="sxs-lookup"><span data-stu-id="e768c-105">Syntax</span></span>  
  
```cpp  
typedef struct _COR_IL_MAP {  
    ULONG32 oldOffset;
    ULONG32 newOffset;
    BOOL    fAccurate;  
} COR_IL_MAP;  
```  
  
## <a name="members"></a><span data-ttu-id="e768c-106">成员</span><span class="sxs-lookup"><span data-stu-id="e768c-106">Members</span></span>  
  
|<span data-ttu-id="e768c-107">成员</span><span class="sxs-lookup"><span data-stu-id="e768c-107">Member</span></span>|<span data-ttu-id="e768c-108">说明</span><span class="sxs-lookup"><span data-stu-id="e768c-108">Description</span></span>|  
|------------|-----------------|  
|`oldOffset`|<span data-ttu-id="e768c-109">旧的 Microsoft 中间语言 (MSIL) 相对于函数开头的偏移量。</span><span class="sxs-lookup"><span data-stu-id="e768c-109">The old Microsoft intermediate language (MSIL) offset relative to the beginning of the function.</span></span>|  
|`newOffset`|<span data-ttu-id="e768c-110">相对于函数开头的新 MSIL 偏移量。</span><span class="sxs-lookup"><span data-stu-id="e768c-110">The new MSIL offset relative to the beginning of the function.</span></span>|  
|`fAccurate`|<span data-ttu-id="e768c-111">`true` 如果已知正确的映射，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="e768c-111">`true` if the mapping is known to be accurate; otherwise, `false`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e768c-112">备注</span><span class="sxs-lookup"><span data-stu-id="e768c-112">Remarks</span></span>  

 <span data-ttu-id="e768c-113">映射的格式如下所示：调试器将假设，这 `oldOffset` 是在原始的未修改的 msil 代码内引用 msil 偏移量。</span><span class="sxs-lookup"><span data-stu-id="e768c-113">The format of the map is as follows: The debugger will assume that `oldOffset` refers to an MSIL offset within the original, unmodified MSIL code.</span></span> <span data-ttu-id="e768c-114">`newOffset`参数引用新的、经过检测的代码中的相应 MSIL 偏移量。</span><span class="sxs-lookup"><span data-stu-id="e768c-114">The `newOffset` parameter refers to the corresponding MSIL offset within the new, instrumented code.</span></span>  
  
 <span data-ttu-id="e768c-115">若要单步执行，应满足以下要求：</span><span class="sxs-lookup"><span data-stu-id="e768c-115">For stepping to work properly, the following requirements should be met:</span></span>  
  
- <span data-ttu-id="e768c-116">地图应按升序排序。</span><span class="sxs-lookup"><span data-stu-id="e768c-116">The map should be sorted in ascending order.</span></span>  
  
- <span data-ttu-id="e768c-117">不应对已检测的 MSIL 代码进行重新排序。</span><span class="sxs-lookup"><span data-stu-id="e768c-117">Instrumented MSIL code should not be reordered.</span></span>  
  
- <span data-ttu-id="e768c-118">不应删除原始的 MSIL 代码。</span><span class="sxs-lookup"><span data-stu-id="e768c-118">Original MSIL code should not be removed.</span></span>  
  
- <span data-ttu-id="e768c-119">映射应包括用于将程序数据库中的所有序列点映射到 (PDB) 文件的项。</span><span class="sxs-lookup"><span data-stu-id="e768c-119">The map should include entries to map all the sequence points from the program database (PDB) file.</span></span>  
  
 <span data-ttu-id="e768c-120">地图未插入缺失的条目。</span><span class="sxs-lookup"><span data-stu-id="e768c-120">The map does not interpolate missing entries.</span></span> <span data-ttu-id="e768c-121">下面的示例演示了一个映射及其结果。</span><span class="sxs-lookup"><span data-stu-id="e768c-121">The following example shows a map and its results.</span></span>  
  
 <span data-ttu-id="e768c-122">Map:</span><span class="sxs-lookup"><span data-stu-id="e768c-122">Map:</span></span>  
  
- <span data-ttu-id="e768c-123">0个旧偏移，0个新偏移</span><span class="sxs-lookup"><span data-stu-id="e768c-123">0 old offset, 0 new offset</span></span>  
  
- <span data-ttu-id="e768c-124">5旧偏移量，10个新偏移</span><span class="sxs-lookup"><span data-stu-id="e768c-124">5 old offset, 10 new offset</span></span>  
  
- <span data-ttu-id="e768c-125">9旧偏移，20个新偏移</span><span class="sxs-lookup"><span data-stu-id="e768c-125">9 old offset, 20 new offset</span></span>  
  
 <span data-ttu-id="e768c-126">结果：</span><span class="sxs-lookup"><span data-stu-id="e768c-126">Results:</span></span>  
  
- <span data-ttu-id="e768c-127">早于0、1、2、3或4的偏移将映射到新的偏移量0。</span><span class="sxs-lookup"><span data-stu-id="e768c-127">An old offset of 0, 1, 2, 3, or 4 will be mapped to a new offset of 0.</span></span>  
  
- <span data-ttu-id="e768c-128">旧偏移量5、6、7或8将映射到新的偏移量10。</span><span class="sxs-lookup"><span data-stu-id="e768c-128">An old offset of 5, 6, 7, or 8 will be mapped to new offset 10.</span></span>  
  
- <span data-ttu-id="e768c-129">旧偏移量9或更高将映射到新偏移量20。</span><span class="sxs-lookup"><span data-stu-id="e768c-129">An old offset of 9 or higher will be mapped to new offset 20.</span></span>  
  
- <span data-ttu-id="e768c-130">新偏移量为0、1、2、3、4、5、6、7、8或9，将映射到旧偏移量0。</span><span class="sxs-lookup"><span data-stu-id="e768c-130">A new offset of 0, 1, 2, 3, 4, 5, 6, 7, 8, or 9 will be mapped to old offset 0.</span></span>  
  
- <span data-ttu-id="e768c-131">新偏移量为10、11、12、13、14、15、16、17、18或19，将映射到旧偏移量5。</span><span class="sxs-lookup"><span data-stu-id="e768c-131">A new offset of 10, 11, 12, 13, 14, 15, 16, 17, 18, or 19 will be mapped to old offset 5.</span></span>  
  
- <span data-ttu-id="e768c-132">20或更高的新偏移量将映射到旧偏移量9。</span><span class="sxs-lookup"><span data-stu-id="e768c-132">A new offset of 20 or higher will be mapped to old offset 9.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e768c-133">要求</span><span class="sxs-lookup"><span data-stu-id="e768c-133">Requirements</span></span>  

 <span data-ttu-id="e768c-134">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e768c-134">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e768c-135">**标头：** Cordebug.idl、Corprof.idl</span><span class="sxs-lookup"><span data-stu-id="e768c-135">**Header:** CorDebug.idl, CorProf.idl</span></span>  
  
 <span data-ttu-id="e768c-136">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e768c-136">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e768c-137">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e768c-137">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e768c-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="e768c-138">See also</span></span>

- [<span data-ttu-id="e768c-139">调试结构</span><span class="sxs-lookup"><span data-stu-id="e768c-139">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="e768c-140">调试</span><span class="sxs-lookup"><span data-stu-id="e768c-140">Debugging</span></span>](index.md)
