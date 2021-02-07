---
description: 了解详细信息： ICorDebugArrayValue 接口
title: ICorDebugArrayValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue interface
helpviewer_keywords:
- ICorDebugArrayValue interface [.NET Framework debugging]
ms.assetid: dc437751-7093-44e2-bfdc-191d9ce3c192
topic_type:
- apiref
ms.openlocfilehash: 2b91c910b9444b061b4a6bea715667bca6a4629c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722888"
---
# <a name="icordebugarrayvalue-interface"></a><span data-ttu-id="a9869-103">ICorDebugArrayValue 接口</span><span class="sxs-lookup"><span data-stu-id="a9869-103">ICorDebugArrayValue Interface</span></span>

<span data-ttu-id="a9869-104">表示一维或多维数组的 ICorDebugHeapValue 的子类。</span><span class="sxs-lookup"><span data-stu-id="a9869-104">A subclass of ICorDebugHeapValue that represents a single-dimensional or multi-dimensional array.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a9869-105">方法</span><span class="sxs-lookup"><span data-stu-id="a9869-105">Methods</span></span>  
  
|<span data-ttu-id="a9869-106">方法</span><span class="sxs-lookup"><span data-stu-id="a9869-106">Method</span></span>|<span data-ttu-id="a9869-107">说明</span><span class="sxs-lookup"><span data-stu-id="a9869-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a9869-108">GetBaseIndicies 方法</span><span class="sxs-lookup"><span data-stu-id="a9869-108">GetBaseIndicies Method</span></span>](icordebugarrayvalue-getbaseindicies-method.md)|<span data-ttu-id="a9869-109">获取数组中每个维的基索引。</span><span class="sxs-lookup"><span data-stu-id="a9869-109">Gets the base index of each dimension in the array.</span></span>|  
|[<span data-ttu-id="a9869-110">GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="a9869-110">GetCount Method</span></span>](icordebugarrayvalue-getcount-method.md)|<span data-ttu-id="a9869-111">获取数组中的元素总数。</span><span class="sxs-lookup"><span data-stu-id="a9869-111">Gets the total number of elements in the array.</span></span>|  
|[<span data-ttu-id="a9869-112">GetDimensions 方法</span><span class="sxs-lookup"><span data-stu-id="a9869-112">GetDimensions Method</span></span>](icordebugarrayvalue-getdimensions-method.md)|<span data-ttu-id="a9869-113">获取数组的尺寸。</span><span class="sxs-lookup"><span data-stu-id="a9869-113">Gets the dimensions of the array.</span></span>|  
|[<span data-ttu-id="a9869-114">GetElement 方法</span><span class="sxs-lookup"><span data-stu-id="a9869-114">GetElement Method</span></span>](icordebugarrayvalue-getelement-method.md)|<span data-ttu-id="a9869-115">获取一个值，该值表示数组中的给定元素。</span><span class="sxs-lookup"><span data-stu-id="a9869-115">Gets a value representing the given element in the array.</span></span>|  
|[<span data-ttu-id="a9869-116">GetElementAtPosition 方法</span><span class="sxs-lookup"><span data-stu-id="a9869-116">GetElementAtPosition Method</span></span>](icordebugarrayvalue-getelementatposition-method.md)|<span data-ttu-id="a9869-117">获取位于给定位置的元素，并将该数组视为从零开始的一维数组。</span><span class="sxs-lookup"><span data-stu-id="a9869-117">Gets the element at the given position, treating the array as a zero-based, single-dimensional array.</span></span>|  
|[<span data-ttu-id="a9869-118">GetElementType 方法</span><span class="sxs-lookup"><span data-stu-id="a9869-118">GetElementType Method</span></span>](icordebugarrayvalue-getelementtype-method.md)|<span data-ttu-id="a9869-119">获取数组中元素的简单类型。</span><span class="sxs-lookup"><span data-stu-id="a9869-119">Gets the simple type of the elements in the array.</span></span>|  
|[<span data-ttu-id="a9869-120">GetRank 方法</span><span class="sxs-lookup"><span data-stu-id="a9869-120">GetRank Method</span></span>](icordebugarrayvalue-getrank-method.md)|<span data-ttu-id="a9869-121">获取数组中的维度数。</span><span class="sxs-lookup"><span data-stu-id="a9869-121">Gets the number of dimensions in the array.</span></span>|  
|[<span data-ttu-id="a9869-122">HasBaseIndicies 方法</span><span class="sxs-lookup"><span data-stu-id="a9869-122">HasBaseIndicies Method</span></span>](icordebugarrayvalue-hasbaseindicies-method.md)|<span data-ttu-id="a9869-123">确定数组是否具有基索引。</span><span class="sxs-lookup"><span data-stu-id="a9869-123">Determines whether the array has base indexes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a9869-124">备注</span><span class="sxs-lookup"><span data-stu-id="a9869-124">Remarks</span></span>  

 <span data-ttu-id="a9869-125">`ICorDebugArrayValue` 支持一维数组和多维数组。</span><span class="sxs-lookup"><span data-stu-id="a9869-125">`ICorDebugArrayValue` supports both single-dimensional and multi-dimensional arrays.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="a9869-126">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="a9869-126">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9869-127">要求</span><span class="sxs-lookup"><span data-stu-id="a9869-127">Requirements</span></span>  

 <span data-ttu-id="a9869-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a9869-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9869-129">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a9869-129">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a9869-130">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a9869-130">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a9869-131">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9869-131">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9869-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="a9869-132">See also</span></span>

- [<span data-ttu-id="a9869-133">调试接口</span><span class="sxs-lookup"><span data-stu-id="a9869-133">Debugging Interfaces</span></span>](debugging-interfaces.md)
