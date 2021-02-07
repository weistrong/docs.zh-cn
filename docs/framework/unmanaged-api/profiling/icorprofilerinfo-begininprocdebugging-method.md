---
description: 了解详细信息： ICorProfilerInfo：： BeginInprocDebugging 方法
title: ICorProfilerInfo::BeginInprocDebugging 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.BeginInprocDebugging
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::BeginInprocDebugging
helpviewer_keywords:
- BeginInprocDebugging method [.NET Framework profiling]
- ICorProfilerInfo::BeginInprocDebugging method [.NET Framework profiling]
ms.assetid: c5c82c69-99f8-4447-aee0-42cca0a5eb5c
topic_type:
- apiref
ms.openlocfilehash: 151aa3604d61e4c5d9e7e24fe9f17bf754d72233
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737397"
---
# <a name="icorprofilerinfobegininprocdebugging-method"></a><span data-ttu-id="26e38-103">ICorProfilerInfo::BeginInprocDebugging 方法</span><span class="sxs-lookup"><span data-stu-id="26e38-103">ICorProfilerInfo::BeginInprocDebugging Method</span></span>

<span data-ttu-id="26e38-104">初始化进程内调试支持。</span><span class="sxs-lookup"><span data-stu-id="26e38-104">Initializes in-process debugging support.</span></span> <span data-ttu-id="26e38-105">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="26e38-105">This method is obsolete in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26e38-106">语法</span><span class="sxs-lookup"><span data-stu-id="26e38-106">Syntax</span></span>  
  
```cpp  
HRESULT BeginInprocDebugging(  
    [in]  BOOL   fThisThreadOnly,  
    [out] DWORD *pdwProfilerContext);  
```  
  
## <a name="parameters"></a><span data-ttu-id="26e38-107">参数</span><span class="sxs-lookup"><span data-stu-id="26e38-107">Parameters</span></span>  

 `fThisThreadOnly`  
 <span data-ttu-id="26e38-108">中将此值设置为 `true` 以仅初始化当前线程的调试支持; 将其设置为 `false` 以初始化对所有线程的调试支持。</span><span class="sxs-lookup"><span data-stu-id="26e38-108">[in] Set this value to `true` to initialize debugging support for only the current thread; set it to `false` to initialize debugging support for all threads.</span></span>  
  
 `pdwProfilerContext`  
 <span data-ttu-id="26e38-109">弄指向用于标识调试会话的返回值的指针。</span><span class="sxs-lookup"><span data-stu-id="26e38-109">[out] The pointer to a returned value that identifies the debugging session.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="26e38-110">备注</span><span class="sxs-lookup"><span data-stu-id="26e38-110">Remarks</span></span>  

 <span data-ttu-id="26e38-111">CLR 调试服务支持 .NET Framework 版本1.0 和1.1 中的有限进程内调试。</span><span class="sxs-lookup"><span data-stu-id="26e38-111">The CLR debugging services supported limited in-process debugging in the .NET Framework versions 1.0 and 1.1.</span></span> <span data-ttu-id="26e38-112">进程内调试使探查器能够使用调试 API 的检查部分。</span><span class="sxs-lookup"><span data-stu-id="26e38-112">In-process debugging enabled a profiler to use the inspection portions of the debugging API.</span></span> <span data-ttu-id="26e38-113">不过，由于客户反馈，已从版本2.0 中的 .NET Framework 中删除进程内调试，并将其替换为一组功能，这些功能与分析 API 行更详细。</span><span class="sxs-lookup"><span data-stu-id="26e38-113">However, due to customer feedback, in-process debugging has been removed from the .NET Framework in version 2.0, and replaced with a set of functionality that is more in line with the profiling API.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26e38-114">要求</span><span class="sxs-lookup"><span data-stu-id="26e38-114">Requirements</span></span>  

 <span data-ttu-id="26e38-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="26e38-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="26e38-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="26e38-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="26e38-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="26e38-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="26e38-118">**.NET Framework 版本：** 1。0</span><span class="sxs-lookup"><span data-stu-id="26e38-118">**.NET Framework Version:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26e38-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="26e38-119">See also</span></span>

- [<span data-ttu-id="26e38-120">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="26e38-120">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
