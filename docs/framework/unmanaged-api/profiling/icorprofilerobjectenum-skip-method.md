---
description: 了解详细信息： ICorProfilerObjectEnum：： Skip 方法
title: ICorProfilerObjectEnum::Skip 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.Skip
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::Skip
helpviewer_keywords:
- ICorProfilerObjectEnum::Skip method [.NET Framework profiling]
- Skip method, ICorProfilerObjectEnum interface [.NET Framework profiling]
ms.assetid: f8e498f8-f93a-4b82-bd22-55bdbf5e8d45
topic_type:
- apiref
ms.openlocfilehash: 8a2aa5dd2b905931b97fafa4db6709aab16aacc4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781254"
---
# <a name="icorprofilerobjectenumskip-method"></a><span data-ttu-id="780bd-103">ICorProfilerObjectEnum::Skip 方法</span><span class="sxs-lookup"><span data-stu-id="780bd-103">ICorProfilerObjectEnum::Skip Method</span></span>

<span data-ttu-id="780bd-104">将此枚举器的光标从其当前位置前移，以便跳过指定数目的元素。</span><span class="sxs-lookup"><span data-stu-id="780bd-104">Advances the cursor of this enumerator from its current position so that the specified number of elements are skipped.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="780bd-105">语法</span><span class="sxs-lookup"><span data-stu-id="780bd-105">Syntax</span></span>  
  
```cpp  
HRESULT Skip (  
    [in] ULONG   celt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="780bd-106">参数</span><span class="sxs-lookup"><span data-stu-id="780bd-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="780bd-107">中要跳过的元素数。</span><span class="sxs-lookup"><span data-stu-id="780bd-107">[in] The number of elements to be skipped.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="780bd-108">备注</span><span class="sxs-lookup"><span data-stu-id="780bd-108">Remarks</span></span>  

 <span data-ttu-id="780bd-109">此枚举器的游标的新位置为： (当前位置) + `celt` 。</span><span class="sxs-lookup"><span data-stu-id="780bd-109">The new position of this enumerator's cursor is: (current position) + `celt` .</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="780bd-110">要求</span><span class="sxs-lookup"><span data-stu-id="780bd-110">Requirements</span></span>  

 <span data-ttu-id="780bd-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="780bd-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="780bd-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="780bd-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="780bd-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="780bd-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="780bd-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="780bd-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="780bd-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="780bd-115">See also</span></span>

- [<span data-ttu-id="780bd-116">ICorProfilerObjectEnum 接口</span><span class="sxs-lookup"><span data-stu-id="780bd-116">ICorProfilerObjectEnum Interface</span></span>](icorprofilerobjectenum-interface.md)
