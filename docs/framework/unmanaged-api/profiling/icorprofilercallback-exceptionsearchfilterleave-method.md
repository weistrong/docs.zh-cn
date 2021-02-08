---
description: 了解详细信息： ICorProfilerCallback：： ExceptionSearchFilterLeave 方法
title: ICorProfilerCallback::ExceptionSearchFilterLeave 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionSearchFilterLeave
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionSearchFilterLeave
helpviewer_keywords:
- ICorProfilerCallback::ExceptionSearchFilterLeave method [.NET Framework profiling]
- ExceptionSearchFilterLeave method [.NET Framework profiling]
ms.assetid: c28a2a82-dd11-4385-843f-b509fb61753b
topic_type:
- apiref
ms.openlocfilehash: d2195e8e055b25f71efbfbcc71e933daa07a4e3e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799117"
---
# <a name="icorprofilercallbackexceptionsearchfilterleave-method"></a><span data-ttu-id="b3f9a-103">ICorProfilerCallback::ExceptionSearchFilterLeave 方法</span><span class="sxs-lookup"><span data-stu-id="b3f9a-103">ICorProfilerCallback::ExceptionSearchFilterLeave Method</span></span>

<span data-ttu-id="b3f9a-104">通知探查器用户筛选器刚刚执行完毕。</span><span class="sxs-lookup"><span data-stu-id="b3f9a-104">Notifies the profiler that a user filter has just finished executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b3f9a-105">语法</span><span class="sxs-lookup"><span data-stu-id="b3f9a-105">Syntax</span></span>  
  
```cpp  
HRESULT ExceptionSearchFilterLeave();  
```  
  
## <a name="requirements"></a><span data-ttu-id="b3f9a-106">要求</span><span class="sxs-lookup"><span data-stu-id="b3f9a-106">Requirements</span></span>  

 <span data-ttu-id="b3f9a-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b3f9a-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b3f9a-108">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b3f9a-108">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b3f9a-109">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b3f9a-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b3f9a-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b3f9a-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3f9a-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="b3f9a-111">See also</span></span>

- [<span data-ttu-id="b3f9a-112">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="b3f9a-112">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="b3f9a-113">ExceptionSearchFilterEnter 方法</span><span class="sxs-lookup"><span data-stu-id="b3f9a-113">ExceptionSearchFilterEnter Method</span></span>](icorprofilercallback-exceptionsearchfilterenter-method.md)
