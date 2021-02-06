---
description: 了解详细信息： ICorProfilerCallback：： ExceptionOSHandlerEnter 方法
title: ICorProfilerCallback::ExceptionOSHandlerEnter 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionOSHandlerEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionOSHandlerEnter
helpviewer_keywords:
- ExceptionOSHandlerEnter method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionOSHandlerEnter method [.NET Framework profiling]
ms.assetid: 09238b9b-9359-4780-89dc-2f5e4f57920e
topic_type:
- apiref
ms.openlocfilehash: 88dfd062451c63265716e7cf4c04292aa15f91ed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657601"
---
# <a name="icorprofilercallbackexceptionoshandlerenter-method"></a><span data-ttu-id="b8980-103">ICorProfilerCallback::ExceptionOSHandlerEnter 方法</span><span class="sxs-lookup"><span data-stu-id="b8980-103">ICorProfilerCallback::ExceptionOSHandlerEnter Method</span></span>

<span data-ttu-id="b8980-104">未实现。</span><span class="sxs-lookup"><span data-stu-id="b8980-104">Not implemented.</span></span> <span data-ttu-id="b8980-105">需要非托管异常信息的探查器必须通过其他方式获取此信息。</span><span class="sxs-lookup"><span data-stu-id="b8980-105">A profiler that needs unmanaged exception information must obtain this information through other means.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8980-106">语法</span><span class="sxs-lookup"><span data-stu-id="b8980-106">Syntax</span></span>  
  
```cpp  
HRESULT ExceptionOSHandlerEnter(  
    [in] UINT_PTR __unused);  
```  
  
## <a name="requirements"></a><span data-ttu-id="b8980-107">要求</span><span class="sxs-lookup"><span data-stu-id="b8980-107">Requirements</span></span>  

 <span data-ttu-id="b8980-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b8980-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b8980-109">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b8980-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b8980-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b8980-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b8980-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b8980-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8980-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="b8980-112">See also</span></span>

- [<span data-ttu-id="b8980-113">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="b8980-113">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
