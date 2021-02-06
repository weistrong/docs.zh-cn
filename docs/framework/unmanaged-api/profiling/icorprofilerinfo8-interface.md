---
description: 了解详细信息： ICorProfilerInfo8 接口
title: ICorProfilerInfo8 接口
ms.date: 08/06/2019
author: davmason
ms.author: davmason
ms.openlocfilehash: 4538c9d314283c67ab0bfe6af3f3768062cffda4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646538"
---
# <a name="icorprofilerinfo8-interface"></a><span data-ttu-id="7bfa8-103">ICorProfilerInfo8 接口</span><span class="sxs-lookup"><span data-stu-id="7bfa8-103">ICorProfilerInfo8 Interface</span></span>

<span data-ttu-id="7bfa8-104">[ICorProfilerInfo7](icorprofilerinfo7-interface.md)的子类，提供查询有关动态方法的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="7bfa8-104">A subclass of [ICorProfilerInfo7](icorprofilerinfo7-interface.md) that provides methods to query information about dynamic methods.</span></span>

## <a name="methods"></a><span data-ttu-id="7bfa8-105">方法</span><span class="sxs-lookup"><span data-stu-id="7bfa8-105">Methods</span></span>  

| <span data-ttu-id="7bfa8-106">方法</span><span class="sxs-lookup"><span data-stu-id="7bfa8-106">Method</span></span>|<span data-ttu-id="7bfa8-107">说明</span><span class="sxs-lookup"><span data-stu-id="7bfa8-107">Description</span></span>|  
| ------------|-----------------|  
|[<span data-ttu-id="7bfa8-108">IsFunctionDynamic 方法</span><span class="sxs-lookup"><span data-stu-id="7bfa8-108">IsFunctionDynamic Method</span></span>](icorprofilerinfo8-isfunctiondynamic-method.md)| <span data-ttu-id="7bfa8-109">确定函数是否没有关联的元数据。</span><span class="sxs-lookup"><span data-stu-id="7bfa8-109">Determines if a function does not have associated metadata.</span></span>|
|[<span data-ttu-id="7bfa8-110">GetFunctionFromIP3 方法</span><span class="sxs-lookup"><span data-stu-id="7bfa8-110">GetFunctionFromIP3 Method</span></span>](icorprofilerinfo8-getfunctionfromip3-method.md)| <span data-ttu-id="7bfa8-111">将托管代码指令指针映射到 FunctionID。</span><span class="sxs-lookup"><span data-stu-id="7bfa8-111">Maps a managed code instruction pointer to a FunctionID.</span></span> <span data-ttu-id="7bfa8-112">此方法适用于动态和非动态方法。</span><span class="sxs-lookup"><span data-stu-id="7bfa8-112">This method works for both dynamic and non-dynamic methods.</span></span> |
|[<span data-ttu-id="7bfa8-113">GetDynamicFunctionInfo 方法</span><span class="sxs-lookup"><span data-stu-id="7bfa8-113">GetDynamicFunctionInfo Method</span></span>](icorprofilerinfo8-getdynamicfunctioninfo-method.md)| <span data-ttu-id="7bfa8-114">检索有关动态方法的信息。</span><span class="sxs-lookup"><span data-stu-id="7bfa8-114">Retrieves information about dynamic methods.</span></span> |

## <a name="requirements"></a><span data-ttu-id="7bfa8-115">要求</span><span class="sxs-lookup"><span data-stu-id="7bfa8-115">Requirements</span></span>  

<span data-ttu-id="7bfa8-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7bfa8-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="7bfa8-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7bfa8-117">**Header:** CorProf.idl, CorProf.h</span></span>  
<span data-ttu-id="7bfa8-118">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7bfa8-118">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="7bfa8-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="7bfa8-119">See also</span></span>

- [<span data-ttu-id="7bfa8-120">分析接口</span><span class="sxs-lookup"><span data-stu-id="7bfa8-120">Profiling Interfaces</span></span>](profiling-interfaces.md)
