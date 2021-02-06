---
description: 了解详细信息： ICorProfilerThreadEnum：： GetCount 方法
title: ICorProfilerThreadEnum::GetCount 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum.GetCount
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum::GetCount
helpviewer_keywords:
- ICorProfilerThreadEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerThreadEnum interface [.NET Framework profiling]
ms.assetid: d6dbdc4a-6115-455d-a3f3-704a81d3646b
topic_type:
- apiref
ms.openlocfilehash: 5219dfc71b79be82f769ac7c8230beaf62c6f33e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646421"
---
# <a name="icorprofilerthreadenumgetcount-method"></a><span data-ttu-id="fcc71-103">ICorProfilerThreadEnum::GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="fcc71-103">ICorProfilerThreadEnum::GetCount Method</span></span>

<span data-ttu-id="fcc71-104">获取应用程序使用的线程数。</span><span class="sxs-lookup"><span data-stu-id="fcc71-104">Gets the number of threads that are used by the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fcc71-105">语法</span><span class="sxs-lookup"><span data-stu-id="fcc71-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCount (    [out] ULONG * pcelt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fcc71-106">参数</span><span class="sxs-lookup"><span data-stu-id="fcc71-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="fcc71-107">弄应用程序使用的线程数。</span><span class="sxs-lookup"><span data-stu-id="fcc71-107">[out] The number of threads used by the application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fcc71-108">要求</span><span class="sxs-lookup"><span data-stu-id="fcc71-108">Requirements</span></span>  

 <span data-ttu-id="fcc71-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fcc71-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fcc71-110">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fcc71-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fcc71-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fcc71-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fcc71-112">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fcc71-112">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fcc71-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="fcc71-113">See also</span></span>

- [<span data-ttu-id="fcc71-114">ICorProfilerThreadEnum 接口</span><span class="sxs-lookup"><span data-stu-id="fcc71-114">ICorProfilerThreadEnum Interface</span></span>](icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="fcc71-115">分析接口</span><span class="sxs-lookup"><span data-stu-id="fcc71-115">Profiling Interfaces</span></span>](profiling-interfaces.md)
