---
description: 了解详细信息： ICorProfilerInfo：： GetInprocInspectionInterface 方法
title: ICorProfilerInfo::GetInprocInspectionInterface 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetInprocInspectionInterface
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetInprocInspectionInterface
helpviewer_keywords:
- GetInprocInspectionInterface method [.NET Framework profiling]
- ICorProfilerInfo::GetInprocInspectionInterface method [.NET Framework profiling]
ms.assetid: 22a92d1d-8849-4af6-8304-ecc53dd1d289
topic_type:
- apiref
ms.openlocfilehash: 5b7ce053f0a64afd5d702a4eb59c1712f4b26e9e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781462"
---
# <a name="icorprofilerinfogetinprocinspectioninterface-method"></a><span data-ttu-id="713aa-103">ICorProfilerInfo::GetInprocInspectionInterface 方法</span><span class="sxs-lookup"><span data-stu-id="713aa-103">ICorProfilerInfo::GetInprocInspectionInterface Method</span></span>

<span data-ttu-id="713aa-104">获取一个对象，该对象可查询 "ICorDebugProcess" 接口。</span><span class="sxs-lookup"><span data-stu-id="713aa-104">Gets an object that can be queried for an "ICorDebugProcess" interface.</span></span> <span data-ttu-id="713aa-105">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="713aa-105">This method is obsolete in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="713aa-106">语法</span><span class="sxs-lookup"><span data-stu-id="713aa-106">Syntax</span></span>  
  
```cpp  
HRESULT GetInprocInspectionInterface(  
    [out] IUnknown **ppicd);  
```  
  
## <a name="parameters"></a><span data-ttu-id="713aa-107">参数</span><span class="sxs-lookup"><span data-stu-id="713aa-107">Parameters</span></span>  

 `ppicd`  
 <span data-ttu-id="713aa-108">可在接口上查询的[out](/cpp/atl/iunknown)对象 `ICorDebugProcess` 。</span><span class="sxs-lookup"><span data-stu-id="713aa-108">[out](/cpp/atl/iunknown) object that can be queried for an `ICorDebugProcess` interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="713aa-109">备注</span><span class="sxs-lookup"><span data-stu-id="713aa-109">Remarks</span></span>  

 <span data-ttu-id="713aa-110">公共语言运行时 (CLR) 调试 API 在 .NET Framework 版本1.0 中支持有限的进程内调试。</span><span class="sxs-lookup"><span data-stu-id="713aa-110">The common language runtime (CLR) debugging API supported limited in-process debugging in the .NET Framework version 1.0.</span></span> <span data-ttu-id="713aa-111">进程内调试使探查器能够使用调试 API 的检查部分。</span><span class="sxs-lookup"><span data-stu-id="713aa-111">In-process debugging enabled a profiler to use the inspection portions of the debugging API.</span></span> <span data-ttu-id="713aa-112">由于客户反馈，已从版本2.0 中的 .NET Framework 中删除进程内调试，并将其替换为一组功能，这些功能与分析 API 是一种更多的功能。</span><span class="sxs-lookup"><span data-stu-id="713aa-112">As a result of customer feedback, in-process debugging has been removed from the .NET Framework in version 2.0, and replaced with a set of functionality that is more in line with the profiling API.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="713aa-113">要求</span><span class="sxs-lookup"><span data-stu-id="713aa-113">Requirements</span></span>  

 <span data-ttu-id="713aa-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="713aa-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="713aa-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="713aa-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="713aa-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="713aa-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="713aa-117">**.NET Framework 版本：** 1。0</span><span class="sxs-lookup"><span data-stu-id="713aa-117">**.NET Framework Version:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="713aa-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="713aa-118">See also</span></span>

- [<span data-ttu-id="713aa-119">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="713aa-119">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
