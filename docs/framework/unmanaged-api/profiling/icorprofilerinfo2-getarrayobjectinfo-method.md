---
description: 了解详细信息： ICorProfilerInfo2：： GetArrayObjectInfo 方法
title: ICorProfilerInfo2::GetArrayObjectInfo 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetArrayObjectInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetArrayObjectInfo
helpviewer_keywords:
- ICorProfilerInfo2::GetArrayObjectInfo method [.NET Framework profiling]
- GetArrayObjectInfo method [.NET Framework profiling]
ms.assetid: bda75017-739f-4ce5-9000-f3b526e8473c
topic_type:
- apiref
ms.openlocfilehash: 1427ad696f73d90a2a07698c71456571fb14ee70
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760532"
---
# <a name="icorprofilerinfo2getarrayobjectinfo-method"></a><span data-ttu-id="e784a-103">ICorProfilerInfo2::GetArrayObjectInfo 方法</span><span class="sxs-lookup"><span data-stu-id="e784a-103">ICorProfilerInfo2::GetArrayObjectInfo Method</span></span>

<span data-ttu-id="e784a-104">获取有关数组对象的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e784a-104">Gets detailed information about an array object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e784a-105">语法</span><span class="sxs-lookup"><span data-stu-id="e784a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetArrayObjectInfo(  
    [in] ObjectID objectId,  
    [in] ULONG32 cDimensions,  
    [out, size_is(cDimensions), length_is(cDimensions)] ULONG32 pDimensionSizes[],  
    [out, size_is(cDimensions), length_is(cDimensions)] int pDimensionLowerBounds[],  
    [out] BYTE **ppData);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e784a-106">参数</span><span class="sxs-lookup"><span data-stu-id="e784a-106">Parameters</span></span>  

 `objectId`  
 <span data-ttu-id="e784a-107">中有效数组对象的 ID。</span><span class="sxs-lookup"><span data-stu-id="e784a-107">[in] The ID of a valid array object.</span></span>  
  
 `cDimensions`  
 <span data-ttu-id="e784a-108">中数组) 维度的排名 (。</span><span class="sxs-lookup"><span data-stu-id="e784a-108">[in] The rank (number of dimensions) of the array.</span></span>  
  
 `pDimensionSizes`  
 <span data-ttu-id="e784a-109">弄一个包含整数的数组，每个整数表示数组维度的大小。</span><span class="sxs-lookup"><span data-stu-id="e784a-109">[out] An array that contains integers, each representing the size of a dimension of the array.</span></span>  
  
 `pDimensionLowerBounds`  
 <span data-ttu-id="e784a-110">弄一个包含整数的数组，其中每个整数表示数组维度的下限。</span><span class="sxs-lookup"><span data-stu-id="e784a-110">[out] An array that contains integers, each representing the lower bound of a dimension of the array.</span></span>  
  
 `ppData`  
 <span data-ttu-id="e784a-111">弄指向数组的原始缓冲区的地址的指针，该缓冲区根据 c + + 约定进行布局。</span><span class="sxs-lookup"><span data-stu-id="e784a-111">[out] A pointer to the address of the raw buffer for the array, which is laid out according to the C++ convention.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e784a-112">备注</span><span class="sxs-lookup"><span data-stu-id="e784a-112">Remarks</span></span>  

 <span data-ttu-id="e784a-113">`pDimensionSizes`和 `pDimensionLowerBounds` 是并行数组，因此位于每个数组中同一索引处的元素是同一实体的特征。</span><span class="sxs-lookup"><span data-stu-id="e784a-113">The `pDimensionSizes` and `pDimensionLowerBounds` are parallel arrays, so the elements located at the same index in each array are characteristics of the same entity.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e784a-114">要求</span><span class="sxs-lookup"><span data-stu-id="e784a-114">Requirements</span></span>  

 <span data-ttu-id="e784a-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e784a-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e784a-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e784a-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e784a-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e784a-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e784a-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e784a-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e784a-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="e784a-119">See also</span></span>

- [<span data-ttu-id="e784a-120">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="e784a-120">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="e784a-121">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="e784a-121">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
