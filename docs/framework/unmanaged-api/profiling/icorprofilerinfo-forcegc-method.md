---
description: 了解详细信息： ICorProfilerInfo：： ForceGC 方法
title: ICorProfilerInfo::ForceGC 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.ForceGC
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::ForceGC
helpviewer_keywords:
- ICorProfilerInfo::ForceGC method [.NET Framework profiling]
- ForceGC method [.NET Framework profiling]
ms.assetid: 0da1ef80-d242-4636-87d0-43e0470b342a
topic_type:
- apiref
ms.openlocfilehash: 1abed09450b72730a11a168223b6da05e9baf9be
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737527"
---
# <a name="icorprofilerinfoforcegc-method"></a><span data-ttu-id="523ed-103">ICorProfilerInfo::ForceGC 方法</span><span class="sxs-lookup"><span data-stu-id="523ed-103">ICorProfilerInfo::ForceGC Method</span></span>

<span data-ttu-id="523ed-104">强制在公共语言运行时 (CLR) 中发生垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="523ed-104">Forces garbage collection to occur within the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="523ed-105">语法</span><span class="sxs-lookup"><span data-stu-id="523ed-105">Syntax</span></span>  
  
```cpp  
HRESULT ForceGC();  
```  
  
## <a name="remarks"></a><span data-ttu-id="523ed-106">备注</span><span class="sxs-lookup"><span data-stu-id="523ed-106">Remarks</span></span>  

 <span data-ttu-id="523ed-107">`ForceGC`只能从从未运行托管代码并且在其堆栈上没有任何探查器回调的线程调用方法。</span><span class="sxs-lookup"><span data-stu-id="523ed-107">The `ForceGC` method must be called only from a thread that has never run managed code and does not have any profiler callbacks on its stack.</span></span> <span data-ttu-id="523ed-108">最方便的实现是在探查器中创建一个单独的线程，该线程在 `ForceGC` 收到信号时调用。</span><span class="sxs-lookup"><span data-stu-id="523ed-108">The most convenient implementation is to create a separate thread within the profiler that calls `ForceGC` when signaled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="523ed-109">要求</span><span class="sxs-lookup"><span data-stu-id="523ed-109">Requirements</span></span>  

 <span data-ttu-id="523ed-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="523ed-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="523ed-111">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="523ed-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="523ed-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="523ed-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="523ed-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="523ed-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="523ed-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="523ed-114">See also</span></span>

- [<span data-ttu-id="523ed-115">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="523ed-115">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
