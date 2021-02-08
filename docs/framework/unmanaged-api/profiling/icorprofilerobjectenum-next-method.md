---
description: 了解详细信息： ICorProfilerObjectEnum：： Next 方法
title: ICorProfilerObjectEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.Next
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::Next
helpviewer_keywords:
- Next method, ICorProfilerObjectEnum interface [.NET Framework profiling]
- ICorProfilerObjectEnum::Next method [.NET Framework profiling]
ms.assetid: b420433c-5ebe-4986-bba1-97902e6db819
topic_type:
- apiref
ms.openlocfilehash: 7f61fa1d4e28043bf5eda95f67dde0d8e87d8c0d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781401"
---
# <a name="icorprofilerobjectenumnext-method"></a><span data-ttu-id="7a4c5-103">ICorProfilerObjectEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="7a4c5-103">ICorProfilerObjectEnum::Next Method</span></span>

<span data-ttu-id="7a4c5-104">从对象的顺序集合中获取指定数目的连续对象，从该序列中的枚举器的当前位置开始。</span><span class="sxs-lookup"><span data-stu-id="7a4c5-104">Gets the specified number of contiguous objects from a sequential collection of objects, starting at the enumerator's current position in the sequence.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a4c5-105">语法</span><span class="sxs-lookup"><span data-stu-id="7a4c5-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG                    celt,  
    [out, size_is(celt), length_is(*pceltFetched)]
        ObjectID                  objects[],  
    [out] ULONG                   *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7a4c5-106">参数</span><span class="sxs-lookup"><span data-stu-id="7a4c5-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="7a4c5-107">[in] 要检索的对象数。</span><span class="sxs-lookup"><span data-stu-id="7a4c5-107">[in] The number of objects to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="7a4c5-108">弄值的数组 `ObjectID` ，其中每个值都表示检索到的对象。</span><span class="sxs-lookup"><span data-stu-id="7a4c5-108">[out] An array of `ObjectID` values, each of which represents a retrieved object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="7a4c5-109">[out] 指向 `objects` 数组中实际返回的元素数目的指针。</span><span class="sxs-lookup"><span data-stu-id="7a4c5-109">[out] A pointer to the number of elements actually returned in the `objects` array.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a4c5-110">要求</span><span class="sxs-lookup"><span data-stu-id="7a4c5-110">Requirements</span></span>  

 <span data-ttu-id="7a4c5-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7a4c5-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a4c5-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7a4c5-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7a4c5-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7a4c5-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7a4c5-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7a4c5-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a4c5-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="7a4c5-115">See also</span></span>

- [<span data-ttu-id="7a4c5-116">ICorProfilerObjectEnum 接口</span><span class="sxs-lookup"><span data-stu-id="7a4c5-116">ICorProfilerObjectEnum Interface</span></span>](icorprofilerobjectenum-interface.md)
