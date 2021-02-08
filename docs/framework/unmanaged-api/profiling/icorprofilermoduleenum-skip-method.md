---
description: 了解详细信息： ICorProfilerModuleEnum：： Skip 方法
title: ICorProfilerModuleEnum::Skip 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerModuleEnum.Skip Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerModuleEnum::Skip
helpviewer_keywords:
- Skip method, ICorProfilerModuleEnum interface [.NET Framework profiling]
- ICorProfilerModuleEnum::Skip method [.NET Framework profiling]
ms.assetid: 8dc29c6a-e2ba-41d8-a1e0-0fdd21421e0b
topic_type:
- apiref
ms.openlocfilehash: 4d814e5e9e369fe286b471fadc9675345cfb5b94
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99798961"
---
# <a name="icorprofilermoduleenumskip-method"></a><span data-ttu-id="7c1ac-103">ICorProfilerModuleEnum::Skip 方法</span><span class="sxs-lookup"><span data-stu-id="7c1ac-103">ICorProfilerModuleEnum::Skip Method</span></span>

<span data-ttu-id="7c1ac-104">将枚举器的游标从其当前位置前移，以便跳过指定数量的元素。</span><span class="sxs-lookup"><span data-stu-id="7c1ac-104">Advances the enumerator's cursor from its current position so that the specified number of elements are skipped.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7c1ac-105">语法</span><span class="sxs-lookup"><span data-stu-id="7c1ac-105">Syntax</span></span>  
  
```cpp  
HRESULT Skip([in] ULONG celt);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7c1ac-106">参数</span><span class="sxs-lookup"><span data-stu-id="7c1ac-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="7c1ac-107">中要跳过的元素数。</span><span class="sxs-lookup"><span data-stu-id="7c1ac-107">[in] The number of elements to be skipped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7c1ac-108">返回值</span><span class="sxs-lookup"><span data-stu-id="7c1ac-108">Return Value</span></span>  

 <span data-ttu-id="7c1ac-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="7c1ac-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="7c1ac-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7c1ac-110">HRESULT</span></span>|<span data-ttu-id="7c1ac-111">说明</span><span class="sxs-lookup"><span data-stu-id="7c1ac-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7c1ac-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c1ac-112">S_OK</span></span>|<span data-ttu-id="7c1ac-113">`celt` 元素已被跳过。</span><span class="sxs-lookup"><span data-stu-id="7c1ac-113">`celt` elements were skipped.</span></span>|  
|<span data-ttu-id="7c1ac-114">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="7c1ac-114">S_FALSE</span></span>|<span data-ttu-id="7c1ac-115">`celt`跳过的元素数少于个，这表示没有更多元素。</span><span class="sxs-lookup"><span data-stu-id="7c1ac-115">Fewer than `celt` elements were skipped, which indicates that there are no more elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7c1ac-116">备注</span><span class="sxs-lookup"><span data-stu-id="7c1ac-116">Remarks</span></span>  

 <span data-ttu-id="7c1ac-117">此枚举器的游标的新位置 (当前位置) + `celt` 。</span><span class="sxs-lookup"><span data-stu-id="7c1ac-117">The new position of this enumerator's cursor is (current position) + `celt`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7c1ac-118">要求</span><span class="sxs-lookup"><span data-stu-id="7c1ac-118">Requirements</span></span>  

 <span data-ttu-id="7c1ac-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7c1ac-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7c1ac-120">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7c1ac-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7c1ac-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7c1ac-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7c1ac-122">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7c1ac-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c1ac-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="7c1ac-123">See also</span></span>

- [<span data-ttu-id="7c1ac-124">ICorProfilerModuleEnum 接口</span><span class="sxs-lookup"><span data-stu-id="7c1ac-124">ICorProfilerModuleEnum Interface</span></span>](icorprofilermoduleenum-interface.md)
- [<span data-ttu-id="7c1ac-125">分析接口</span><span class="sxs-lookup"><span data-stu-id="7c1ac-125">Profiling Interfaces</span></span>](profiling-interfaces.md)
