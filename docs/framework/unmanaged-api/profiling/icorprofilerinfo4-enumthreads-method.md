---
description: 了解详细信息： ICorProfilerInfo4：： EnumThreads 方法
title: ICorProfilerInfo4::EnumThreads 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.EnumThreads
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::EnumThreads
helpviewer_keywords:
- ICorProfilerInfo4::EnumThreads method [.NET Framework profiling]
- EnumThreads method, ICorProfilerInfo4 interface [.NET Framework profiling]
ms.assetid: bca7a5b4-c207-4894-918c-0733926296dd
topic_type:
- apiref
ms.openlocfilehash: d597e68b8765e135d5bdb403dbdb161b7acbaa9b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99686929"
---
# <a name="icorprofilerinfo4enumthreads-method"></a><span data-ttu-id="670f3-103">ICorProfilerInfo4::EnumThreads 方法</span><span class="sxs-lookup"><span data-stu-id="670f3-103">ICorProfilerInfo4::EnumThreads Method</span></span>

<span data-ttu-id="670f3-104">返回一个枚举器，该枚举器提供按顺序循环访问所分析进程中所有托管线程的集合的方法。</span><span class="sxs-lookup"><span data-stu-id="670f3-104">Returns an enumerator that provides methods to sequentially iterate through the collection of all managed threads in the profiled process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="670f3-105">语法</span><span class="sxs-lookup"><span data-stu-id="670f3-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumThreads([out]  
            ICorProfilerThreadEnum** ppEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="670f3-106">参数</span><span class="sxs-lookup"><span data-stu-id="670f3-106">Parameters</span></span>  

 `ppEnum`  
 <span data-ttu-id="670f3-107">弄指向 [ICorProfilerThreadEnum](icorprofilerthreadenum-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="670f3-107">[out] A pointer to an [ICorProfilerThreadEnum](icorprofilerthreadenum-interface.md) interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="670f3-108">备注</span><span class="sxs-lookup"><span data-stu-id="670f3-108">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="670f3-109">要求</span><span class="sxs-lookup"><span data-stu-id="670f3-109">Requirements</span></span>  

 <span data-ttu-id="670f3-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="670f3-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="670f3-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="670f3-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="670f3-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="670f3-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="670f3-113">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="670f3-113">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="670f3-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="670f3-114">See also</span></span>

- [<span data-ttu-id="670f3-115">ICorProfilerThreadEnum 接口</span><span class="sxs-lookup"><span data-stu-id="670f3-115">ICorProfilerThreadEnum Interface</span></span>](icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="670f3-116">ICorProfilerInfo4 接口</span><span class="sxs-lookup"><span data-stu-id="670f3-116">ICorProfilerInfo4 Interface</span></span>](icorprofilerinfo4-interface.md)
- [<span data-ttu-id="670f3-117">分析接口</span><span class="sxs-lookup"><span data-stu-id="670f3-117">Profiling Interfaces</span></span>](profiling-interfaces.md)
- [<span data-ttu-id="670f3-118">分析</span><span class="sxs-lookup"><span data-stu-id="670f3-118">Profiling</span></span>](index.md)
