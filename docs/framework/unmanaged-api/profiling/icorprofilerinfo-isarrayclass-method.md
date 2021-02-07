---
description: 了解详细信息： ICorProfilerInfo：： IsArrayClass 方法
title: ICorProfilerInfo::IsArrayClass 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.IsArrayClass
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::IsArrayClass
helpviewer_keywords:
- IsArrayClass method [.NET Framework profiling]
- ICorProfilerInfo::IsArrayClass method [.NET Framework profiling]
ms.assetid: 7f230961-23a6-4d56-ad2d-7a876d65705f
topic_type:
- apiref
ms.openlocfilehash: 1eee0b834c63c3cfe15bd08776214ca8b2ba3f69
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687228"
---
# <a name="icorprofilerinfoisarrayclass-method"></a><span data-ttu-id="fa31d-103">ICorProfilerInfo::IsArrayClass 方法</span><span class="sxs-lookup"><span data-stu-id="fa31d-103">ICorProfilerInfo::IsArrayClass Method</span></span>

<span data-ttu-id="fa31d-104">确定指定的类是否为数组类。</span><span class="sxs-lookup"><span data-stu-id="fa31d-104">Determines whether the specified class is an array class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa31d-105">语法</span><span class="sxs-lookup"><span data-stu-id="fa31d-105">Syntax</span></span>  
  
```cpp  
HRESULT IsArrayClass(  
    [in]  ClassID        classId,  
    [out] CorElementType *pBaseElemType,  
    [out] ClassID        *pBaseClassId,  
    [out] ULONG          *pcRank);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fa31d-106">参数</span><span class="sxs-lookup"><span data-stu-id="fa31d-106">Parameters</span></span>  

 `classId`  
 <span data-ttu-id="fa31d-107">中要检查的类的 ID。</span><span class="sxs-lookup"><span data-stu-id="fa31d-107">[in] The ID of the class to be examined.</span></span>  
  
 `pBaseElemType`  
 <span data-ttu-id="fa31d-108">弄指向 CorElementType 枚举的值的指针，该枚举指示数组元素的类型。</span><span class="sxs-lookup"><span data-stu-id="fa31d-108">[out] A pointer to a value of the CorElementType enumeration that indicates the type of the array elements.</span></span>  
  
 `pBaseClassId`  
 <span data-ttu-id="fa31d-109">弄指向数组元素的类 ID 的指针（如果可用）。</span><span class="sxs-lookup"><span data-stu-id="fa31d-109">[out] A pointer to the class ID of the array elements, when available.</span></span>  
  
 `pcRank`  
 <span data-ttu-id="fa31d-110">弄指向整数的指针，该整数指示 (数组的维数) 的级别。</span><span class="sxs-lookup"><span data-stu-id="fa31d-110">[out] A pointer to an integer that indicates the rank (that is, number of dimensions) of the array.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fa31d-111">备注</span><span class="sxs-lookup"><span data-stu-id="fa31d-111">Remarks</span></span>  

 <span data-ttu-id="fa31d-112">如果指定的类是一个数组类，则该 `IsArrayClass` 方法将返回 S_OK HRESULT 和任何非 null 输出参数的值。</span><span class="sxs-lookup"><span data-stu-id="fa31d-112">If the specified class is an array class, the `IsArrayClass` method returns an S_OK HRESULT and values for any non-null output parameters.</span></span> <span data-ttu-id="fa31d-113">否则，它将返回 S_FALSE。</span><span class="sxs-lookup"><span data-stu-id="fa31d-113">Otherwise, it returns S_FALSE.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fa31d-114">要求</span><span class="sxs-lookup"><span data-stu-id="fa31d-114">Requirements</span></span>  

 <span data-ttu-id="fa31d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fa31d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fa31d-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fa31d-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fa31d-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fa31d-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fa31d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa31d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa31d-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="fa31d-119">See also</span></span>

- [<span data-ttu-id="fa31d-120">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="fa31d-120">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
