---
description: 了解详细信息： ICorProfilerInfo：： GetInprocInspectionIThisThread 方法
title: ICorProfilerInfo::GetInprocInspectionIThisThread 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetInprocInspectionIThisThread
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetInprocInspectionIThisThread
helpviewer_keywords:
- ICorProfilerInfo::GetInprocInspectionIThisThread method [.NET Framework profiling]
- GetInprocInspectionIThisThread method [.NET Framework profiling]
ms.assetid: badddccd-f85c-416e-9f0f-419eab2c9d42
topic_type:
- apiref
ms.openlocfilehash: 07ff904170750976e54e623101a2552db0c7f290
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647240"
---
# <a name="icorprofilerinfogetinprocinspectionithisthread-method"></a><span data-ttu-id="4a260-103">ICorProfilerInfo::GetInprocInspectionIThisThread 方法</span><span class="sxs-lookup"><span data-stu-id="4a260-103">ICorProfilerInfo::GetInprocInspectionIThisThread Method</span></span>

<span data-ttu-id="4a260-104">获取一个对象，该对象可查询 ICorDebugThread 接口。</span><span class="sxs-lookup"><span data-stu-id="4a260-104">Gets an object that can be queried for the ICorDebugThread interface.</span></span> <span data-ttu-id="4a260-105">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="4a260-105">This method is obsolete in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a260-106">语法</span><span class="sxs-lookup"><span data-stu-id="4a260-106">Syntax</span></span>  
  
```cpp  
HRESULT GetInprocInspectionIThisThread(  
    [out] IUnknown **ppicd);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4a260-107">参数</span><span class="sxs-lookup"><span data-stu-id="4a260-107">Parameters</span></span>  

 `ppicd`  
 <span data-ttu-id="4a260-108">可在接口上查询的[输出](/cpp/atl/iunknown)对象 `ICorDebugThread` 。</span><span class="sxs-lookup"><span data-stu-id="4a260-108">[out](/cpp/atl/iunknown) object that can be queried for the `ICorDebugThread` interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4a260-109">备注</span><span class="sxs-lookup"><span data-stu-id="4a260-109">Remarks</span></span>  

 <span data-ttu-id="4a260-110">公共语言运行时 (CLR) 调试服务在 .NET Framework 版本1.0 中支持有限的进程内调试。</span><span class="sxs-lookup"><span data-stu-id="4a260-110">The common language runtime (CLR) debugging services supported limited in-process debugging in the .NET Framework version 1.0.</span></span> <span data-ttu-id="4a260-111">进程内调试使探查器能够使用调试 API 的检查部分。</span><span class="sxs-lookup"><span data-stu-id="4a260-111">In-process debugging enabled a profiler to use the inspection portions of the debugging API.</span></span> <span data-ttu-id="4a260-112">由于客户反馈，已从版本2.0 中的 .NET Framework 中删除进程内调试，并将其替换为一组功能，这些功能与分析 API 是一种更多的功能。</span><span class="sxs-lookup"><span data-stu-id="4a260-112">As a result of customer feedback, in-process debugging has been removed from the .NET Framework in version 2.0, and replaced with a set of functionality that is more in line with the profiling API.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a260-113">要求</span><span class="sxs-lookup"><span data-stu-id="4a260-113">Requirements</span></span>  

 <span data-ttu-id="4a260-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4a260-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a260-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="4a260-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="4a260-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4a260-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4a260-117">**.NET Framework 版本：** 1。0</span><span class="sxs-lookup"><span data-stu-id="4a260-117">**.NET Framework Version:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a260-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="4a260-118">See also</span></span>

- [<span data-ttu-id="4a260-119">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="4a260-119">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
