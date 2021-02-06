---
description: 了解详细信息： ICorProfilerFunctionEnum：： Skip 方法
title: ICorProfilerFunctionEnum::Skip 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionEnum.Skip Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionEnum::Skip
helpviewer_keywords:
- Skip method, ICorProfilerFunctionEnum interface [.NET Framework profiling]
- ICorProfilerFunctionEnum::Skip method [.NET Framework profiling]
ms.assetid: 051465b9-e479-494a-804b-c880323b4cbe
topic_type:
- apiref
ms.openlocfilehash: 6d176c51788135952127008f2f43545ead1e2369
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657055"
---
# <a name="icorprofilerfunctionenumskip-method"></a><span data-ttu-id="ee094-103">ICorProfilerFunctionEnum::Skip 方法</span><span class="sxs-lookup"><span data-stu-id="ee094-103">ICorProfilerFunctionEnum::Skip Method</span></span>

<span data-ttu-id="ee094-104">将枚举器的游标从其当前位置前移，以便跳过指定数量的元素。</span><span class="sxs-lookup"><span data-stu-id="ee094-104">Advances the enumerator's cursor from its current position so that the specified number of elements are skipped.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ee094-105">语法</span><span class="sxs-lookup"><span data-stu-id="ee094-105">Syntax</span></span>  
  
```cpp  
HRESULT Skip([in] ULONG celt);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ee094-106">参数</span><span class="sxs-lookup"><span data-stu-id="ee094-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="ee094-107">中要跳过的元素数。</span><span class="sxs-lookup"><span data-stu-id="ee094-107">[in] The number of elements to be skipped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ee094-108">返回值</span><span class="sxs-lookup"><span data-stu-id="ee094-108">Return Value</span></span>  

 <span data-ttu-id="ee094-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="ee094-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="ee094-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ee094-110">HRESULT</span></span>|<span data-ttu-id="ee094-111">说明</span><span class="sxs-lookup"><span data-stu-id="ee094-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ee094-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee094-112">S_OK</span></span>|<span data-ttu-id="ee094-113">`celt` 元素已被跳过。</span><span class="sxs-lookup"><span data-stu-id="ee094-113">`celt` elements were skipped.</span></span>|  
|<span data-ttu-id="ee094-114">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ee094-114">S_FALSE</span></span>|<span data-ttu-id="ee094-115">`celt`跳过的元素数少于个，这表示没有更多元素。</span><span class="sxs-lookup"><span data-stu-id="ee094-115">Fewer than `celt` elements were skipped, which indicates that there are no more elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ee094-116">备注</span><span class="sxs-lookup"><span data-stu-id="ee094-116">Remarks</span></span>  

 <span data-ttu-id="ee094-117">此枚举器的游标的新位置 (当前位置) + `celt` 。</span><span class="sxs-lookup"><span data-stu-id="ee094-117">The new position of this enumerator's cursor is (current position) + `celt`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ee094-118">要求</span><span class="sxs-lookup"><span data-stu-id="ee094-118">Requirements</span></span>  

 <span data-ttu-id="ee094-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ee094-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ee094-120">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ee094-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ee094-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ee094-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ee094-122">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ee094-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee094-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="ee094-123">See also</span></span>

- [<span data-ttu-id="ee094-124">ICorProfilerFunctionEnum 接口</span><span class="sxs-lookup"><span data-stu-id="ee094-124">ICorProfilerFunctionEnum Interface</span></span>](icorprofilerfunctionenum-interface.md)
- [<span data-ttu-id="ee094-125">分析接口</span><span class="sxs-lookup"><span data-stu-id="ee094-125">Profiling Interfaces</span></span>](profiling-interfaces.md)
