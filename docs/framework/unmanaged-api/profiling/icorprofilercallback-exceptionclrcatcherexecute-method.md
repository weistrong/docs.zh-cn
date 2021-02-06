---
description: 了解详细信息： ICorProfilerCallback：： ExceptionCLRCatcherExecute 方法
title: ICorProfilerCallback::ExceptionCLRCatcherExecute 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionCLRCatcherExecute
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionCLRCatcherExecute
helpviewer_keywords:
- ExceptionCLRCatcherExecute method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionCLRCatcherExecute method [.NET Framework profiling]
ms.assetid: aaac8f98-5cf4-42c7-b04b-556cce367e36
topic_type:
- apiref
ms.openlocfilehash: cb6926fdfcc9b5ffef20cc69c71a3bafefd9f6ff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657497"
---
# <a name="icorprofilercallbackexceptionclrcatcherexecute-method"></a><span data-ttu-id="aba81-103">ICorProfilerCallback::ExceptionCLRCatcherExecute 方法</span><span class="sxs-lookup"><span data-stu-id="aba81-103">ICorProfilerCallback::ExceptionCLRCatcherExecute Method</span></span>

<span data-ttu-id="aba81-104">在 `catch` 公共语言运行时中执行异常时调用 (CLR) 自身。</span><span class="sxs-lookup"><span data-stu-id="aba81-104">Called when a `catch` block for an exception is executed inside the common language runtime (CLR) itself.</span></span> <span data-ttu-id="aba81-105">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="aba81-105">This method is obsolete in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aba81-106">语法</span><span class="sxs-lookup"><span data-stu-id="aba81-106">Syntax</span></span>  
  
```cpp  
HRESULT ExceptionCLRCatcherExecute();  
```  
  
## <a name="requirements"></a><span data-ttu-id="aba81-107">要求</span><span class="sxs-lookup"><span data-stu-id="aba81-107">Requirements</span></span>  

 <span data-ttu-id="aba81-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="aba81-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aba81-109">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="aba81-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="aba81-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aba81-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aba81-111">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="aba81-111">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aba81-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="aba81-112">See also</span></span>

- [<span data-ttu-id="aba81-113">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="aba81-113">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="aba81-114">ExceptionCLRCatcherFound 方法</span><span class="sxs-lookup"><span data-stu-id="aba81-114">ExceptionCLRCatcherFound Method</span></span>](icorprofilercallback-exceptionclrcatcherfound-method.md)
