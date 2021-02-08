---
description: 了解详细信息： ICorProfilerCallback：： RemotingServerInvocationReturned 方法
title: ICorProfilerCallback::RemotingServerInvocationReturned 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingServerInvocationReturned
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingServerInvocationReturned
helpviewer_keywords:
- ICorProfilerCallback::RemotingServerInvocationReturned method [.NET Framework profiling]
- RemotingServerInvocationReturned method [.NET Framework profiling]
ms.assetid: a4de6805-e159-4280-99e5-3390c86166d0
topic_type:
- apiref
ms.openlocfilehash: 97f9fda42059ac66fc3a29689adc252556798e4b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788912"
---
# <a name="icorprofilercallbackremotingserverinvocationreturned-method"></a><span data-ttu-id="cbb6d-103">ICorProfilerCallback::RemotingServerInvocationReturned 方法</span><span class="sxs-lookup"><span data-stu-id="cbb6d-103">ICorProfilerCallback::RemotingServerInvocationReturned Method</span></span>

<span data-ttu-id="cbb6d-104">通知探查器进程已完成调用方法以响应远程方法调用请求。</span><span class="sxs-lookup"><span data-stu-id="cbb6d-104">Notifies the profiler that the process has finished invoking a method in response to a remote method invocation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cbb6d-105">语法</span><span class="sxs-lookup"><span data-stu-id="cbb6d-105">Syntax</span></span>  
  
```cpp  
HRESULT RemotingServerInvocationReturned();  
```  
  
## <a name="requirements"></a><span data-ttu-id="cbb6d-106">要求</span><span class="sxs-lookup"><span data-stu-id="cbb6d-106">Requirements</span></span>  

 <span data-ttu-id="cbb6d-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cbb6d-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cbb6d-108">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="cbb6d-108">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="cbb6d-109">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cbb6d-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cbb6d-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cbb6d-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cbb6d-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="cbb6d-111">See also</span></span>

- [<span data-ttu-id="cbb6d-112">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="cbb6d-112">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
