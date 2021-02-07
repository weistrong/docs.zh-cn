---
description: 了解详细信息： ICorProfilerThreadEnum：： Skip 方法
title: ICorProfilerThreadEnum::Skip 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum.Skip
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum::Skip
helpviewer_keywords:
- Skip method, ICorProfilerThreadEnum interface [.NET Framework profiling]
- ICorProfilerThreadEnum::Skip method [.NET Framework profiling]
ms.assetid: acb8b029-4a96-4ed7-ae3c-310204e5ceea
topic_type:
- apiref
ms.openlocfilehash: 1da191980364868ed4237fccaf7495d5417705cc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736885"
---
# <a name="icorprofilerthreadenumskip-method"></a><span data-ttu-id="08060-103">ICorProfilerThreadEnum::Skip 方法</span><span class="sxs-lookup"><span data-stu-id="08060-103">ICorProfilerThreadEnum::Skip Method</span></span>

<span data-ttu-id="08060-104">从当前位置前移枚举器的光标，以便跳过指定的元素数量。</span><span class="sxs-lookup"><span data-stu-id="08060-104">Advances the enumerator's cursor from its current position to skip the specified number of elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08060-105">语法</span><span class="sxs-lookup"><span data-stu-id="08060-105">Syntax</span></span>  
  
```cpp  
HRESULT Skip (    [in] ULONG celt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="08060-106">参数</span><span class="sxs-lookup"><span data-stu-id="08060-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="08060-107">中要跳过的元素数。</span><span class="sxs-lookup"><span data-stu-id="08060-107">[in] The number of elements to be skipped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="08060-108">返回值</span><span class="sxs-lookup"><span data-stu-id="08060-108">Return Value</span></span>  

 <span data-ttu-id="08060-109">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="08060-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="08060-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="08060-110">HRESULT</span></span>|<span data-ttu-id="08060-111">说明</span><span class="sxs-lookup"><span data-stu-id="08060-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="08060-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="08060-112">S_OK</span></span>|<span data-ttu-id="08060-113">`celt` 元素已被跳过。</span><span class="sxs-lookup"><span data-stu-id="08060-113">`celt` elements were skipped.</span></span>|  
|<span data-ttu-id="08060-114">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="08060-114">S_FALSE</span></span>|<span data-ttu-id="08060-115">`celt`跳过的元素数少于个，这表示没有更多元素。</span><span class="sxs-lookup"><span data-stu-id="08060-115">Fewer than `celt` elements were skipped, which indicates that there are no more elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="08060-116">备注</span><span class="sxs-lookup"><span data-stu-id="08060-116">Remarks</span></span>  

 <span data-ttu-id="08060-117">此枚举器的游标的新位置 (当前位置) + `celt` 。</span><span class="sxs-lookup"><span data-stu-id="08060-117">The new position of this enumerator's cursor is (current position) + `celt`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08060-118">要求</span><span class="sxs-lookup"><span data-stu-id="08060-118">Requirements</span></span>  

 <span data-ttu-id="08060-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="08060-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="08060-120">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="08060-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="08060-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="08060-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="08060-122">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="08060-122">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08060-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="08060-123">See also</span></span>

- [<span data-ttu-id="08060-124">ICorProfilerThreadEnum 接口</span><span class="sxs-lookup"><span data-stu-id="08060-124">ICorProfilerThreadEnum Interface</span></span>](icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="08060-125">分析接口</span><span class="sxs-lookup"><span data-stu-id="08060-125">Profiling Interfaces</span></span>](profiling-interfaces.md)
