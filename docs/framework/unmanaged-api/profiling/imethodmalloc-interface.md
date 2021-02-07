---
description: 了解详细信息： IMethodMalloc 接口
title: IMethodMalloc 接口
ms.date: 03/30/2017
api_name:
- IMethodMalloc
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- IMethodMalloc
helpviewer_keywords:
- IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8c8ab5dc-557c-473a-82f2-6e403eca7dac
topic_type:
- apiref
ms.openlocfilehash: 6b84ac0ddb49718d24b2cad174613bc311dc509b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736947"
---
# <a name="imethodmalloc-interface"></a><span data-ttu-id="672a5-103">IMethodMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="672a5-103">IMethodMalloc Interface</span></span>

<span data-ttu-id="672a5-104">提供一个方法，用于为新的 Microsoft 中间语言 (MSIL) 函数体分配内存。</span><span class="sxs-lookup"><span data-stu-id="672a5-104">Provides a method to allocate memory for a new Microsoft intermediate language (MSIL) function body.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="672a5-105">`IMethodMalloc`接口是一个简单的内存分配器。</span><span class="sxs-lookup"><span data-stu-id="672a5-105">The `IMethodMalloc` interface is a simple memory allocator.</span></span> <span data-ttu-id="672a5-106">它允许您分配内存，但不能释放内存。</span><span class="sxs-lookup"><span data-stu-id="672a5-106">It allows you to allocate memory, but not to free it.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="672a5-107">方法</span><span class="sxs-lookup"><span data-stu-id="672a5-107">Methods</span></span>  
  
|<span data-ttu-id="672a5-108">方法</span><span class="sxs-lookup"><span data-stu-id="672a5-108">Method</span></span>|<span data-ttu-id="672a5-109">说明</span><span class="sxs-lookup"><span data-stu-id="672a5-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="672a5-110">Alloc 方法</span><span class="sxs-lookup"><span data-stu-id="672a5-110">Alloc Method</span></span>](imethodmalloc-alloc-method.md)|<span data-ttu-id="672a5-111">尝试为新的 MSIL 函数体分配指定的内存量。</span><span class="sxs-lookup"><span data-stu-id="672a5-111">Attempts to allocate a specified amount of memory for a new MSIL function body.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="672a5-112">备注</span><span class="sxs-lookup"><span data-stu-id="672a5-112">Remarks</span></span>  

 <span data-ttu-id="672a5-113">每个分配器都是特定于模块的，并确保函数体与模块的基偏移为正偏移量。</span><span class="sxs-lookup"><span data-stu-id="672a5-113">Each allocator is module-specific and ensures that the function body will be at a positive offset from the base of the module.</span></span> <span data-ttu-id="672a5-114">超出模块基的内存可能非常宝贵，因此应使用分配器仅为函数体分配内存。</span><span class="sxs-lookup"><span data-stu-id="672a5-114">Memory above the base of a module can be precious, so the allocator should be used to allocate memory only for a function body.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="672a5-115">要求</span><span class="sxs-lookup"><span data-stu-id="672a5-115">Requirements</span></span>  

 <span data-ttu-id="672a5-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="672a5-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="672a5-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="672a5-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="672a5-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="672a5-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="672a5-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="672a5-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="672a5-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="672a5-120">See also</span></span>

- [<span data-ttu-id="672a5-121">分析接口</span><span class="sxs-lookup"><span data-stu-id="672a5-121">Profiling Interfaces</span></span>](profiling-interfaces.md)
