---
description: 了解详细信息： ICorProfilerThreadEnum：： Next 方法
title: ICorProfilerThreadEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum.Next
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum::Next
helpviewer_keywords:
- ICorProfilerThreadEnum::Next method [.NET Framework profiling]
- Next method, ICorProfilerThreadEnum interface [.NET Framework profiling]
ms.assetid: f3535279-3c63-41a2-ab0e-a129dc5a01e8
topic_type:
- apiref
ms.openlocfilehash: 74567624cbe5042b8ab63a28e7fb07e9f708a959
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636325"
---
# <a name="icorprofilerthreadenumnext-method"></a><span data-ttu-id="07872-103">ICorProfilerThreadEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="07872-103">ICorProfilerThreadEnum::Next Method</span></span>

<span data-ttu-id="07872-104">从线程的序列集合获取指定的连续线程数，从序列中枚举器的当前位置开始。</span><span class="sxs-lookup"><span data-stu-id="07872-104">Gets the specified number of contiguous threads from a sequential collection of threads, starting at the enumerator's current position in the sequence.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07872-105">语法</span><span class="sxs-lookup"><span data-stu-id="07872-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (    [in]  ULONG      celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
                    ThreadID ids[],  
    [out] ULONG *   pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="07872-106">参数</span><span class="sxs-lookup"><span data-stu-id="07872-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="07872-107">[in] 要检索的线程数。</span><span class="sxs-lookup"><span data-stu-id="07872-107">[in] The number of threads to retrieve.</span></span>  
  
 `ids`  
 <span data-ttu-id="07872-108">[out] `ThreadID` 值的数组，其中每个值表示检索的线程。</span><span class="sxs-lookup"><span data-stu-id="07872-108">[out] An array of `ThreadID` values, each of which represents a retrieved thread.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="07872-109">[out] 指向 `ids` 数组中实际返回的线程数的指针。</span><span class="sxs-lookup"><span data-stu-id="07872-109">[out] A pointer to the number of threads actually returned in the `ids` array.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="07872-110">返回值</span><span class="sxs-lookup"><span data-stu-id="07872-110">Return Value</span></span>  

 <span data-ttu-id="07872-111">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="07872-111">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="07872-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="07872-112">HRESULT</span></span>|<span data-ttu-id="07872-113">说明</span><span class="sxs-lookup"><span data-stu-id="07872-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="07872-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="07872-114">S_OK</span></span>|<span data-ttu-id="07872-115">已返回 `celt` 元素。</span><span class="sxs-lookup"><span data-stu-id="07872-115">`celt` elements were returned.</span></span>|  
|<span data-ttu-id="07872-116">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="07872-116">S_FALSE</span></span>|<span data-ttu-id="07872-117">返回的元素少于 `celt` 个，表示枚举已完成。</span><span class="sxs-lookup"><span data-stu-id="07872-117">Fewer than `celt` elements were returned, which indicates that the enumeration is complete.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="07872-118">要求</span><span class="sxs-lookup"><span data-stu-id="07872-118">Requirements</span></span>  

 <span data-ttu-id="07872-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="07872-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="07872-120">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="07872-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="07872-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="07872-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="07872-122">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="07872-122">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07872-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="07872-123">See also</span></span>

- [<span data-ttu-id="07872-124">ICorProfilerThreadEnum 接口</span><span class="sxs-lookup"><span data-stu-id="07872-124">ICorProfilerThreadEnum Interface</span></span>](icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="07872-125">分析接口</span><span class="sxs-lookup"><span data-stu-id="07872-125">Profiling Interfaces</span></span>](profiling-interfaces.md)
