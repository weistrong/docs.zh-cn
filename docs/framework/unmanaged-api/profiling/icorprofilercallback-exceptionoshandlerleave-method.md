---
description: 了解详细信息： ICorProfilerCallback：： ExceptionOSHandlerLeave 方法
title: ICorProfilerCallback::ExceptionOSHandlerLeave 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionOSHandlerLeave
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionOSHandlerLeave
helpviewer_keywords:
- ExceptionOSHandlerLeave method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionOSHandlerLeave method [.NET Framework profiling]
ms.assetid: 4d164676-0ee9-4f67-a8ea-cb474db09053
topic_type:
- apiref
ms.openlocfilehash: 809f9440510bc0b55c9cae9827757eb61e61b257
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657549"
---
# <a name="icorprofilercallbackexceptionoshandlerleave-method"></a><span data-ttu-id="ca7aa-103">ICorProfilerCallback::ExceptionOSHandlerLeave 方法</span><span class="sxs-lookup"><span data-stu-id="ca7aa-103">ICorProfilerCallback::ExceptionOSHandlerLeave Method</span></span>

<span data-ttu-id="ca7aa-104">未实现。</span><span class="sxs-lookup"><span data-stu-id="ca7aa-104">Not implemented.</span></span> <span data-ttu-id="ca7aa-105">需要非托管异常信息的探查器必须通过其他方式获取此信息。</span><span class="sxs-lookup"><span data-stu-id="ca7aa-105">A profiler that needs unmanaged exception information must obtain this information through other means.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca7aa-106">语法</span><span class="sxs-lookup"><span data-stu-id="ca7aa-106">Syntax</span></span>  
  
```cpp  
HRESULT ExceptionOSHandlerLeave(  
    [in] UINT_PTR __unused);  
```  
  
## <a name="requirements"></a><span data-ttu-id="ca7aa-107">要求</span><span class="sxs-lookup"><span data-stu-id="ca7aa-107">Requirements</span></span>  

 <span data-ttu-id="ca7aa-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ca7aa-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca7aa-109">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ca7aa-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ca7aa-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ca7aa-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ca7aa-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca7aa-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca7aa-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="ca7aa-112">See also</span></span>

- [<span data-ttu-id="ca7aa-113">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="ca7aa-113">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
