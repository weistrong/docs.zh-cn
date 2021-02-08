---
description: 了解详细信息： ICorProfilerCallback：： RemotingServerInvocationStarted 方法
title: ICorProfilerCallback::RemotingServerInvocationStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingServerInvocationStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingServerInvocationStarted
helpviewer_keywords:
- RemotingServerInvocationStarted method [.NET Framework profiling]
- ICorProfilerCallback::RemotingServerInvocationStarted method [.NET Framework profiling]
ms.assetid: 86051a11-ad8e-4ace-9a11-ff0f982a5e11
topic_type:
- apiref
ms.openlocfilehash: 8a27e3e545b9ff2812561f5faa7ebfe70d41f015
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788899"
---
# <a name="icorprofilercallbackremotingserverinvocationstarted-method"></a><span data-ttu-id="5fd58-103">ICorProfilerCallback::RemotingServerInvocationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="5fd58-103">ICorProfilerCallback::RemotingServerInvocationStarted Method</span></span>

<span data-ttu-id="5fd58-104">通知探查器进程正在调用方法以响应远程方法调用请求。</span><span class="sxs-lookup"><span data-stu-id="5fd58-104">Notifies the profiler that the process is invoking a method in response to a remote method invocation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5fd58-105">语法</span><span class="sxs-lookup"><span data-stu-id="5fd58-105">Syntax</span></span>  
  
```cpp  
HRESULT RemotingServerInvocationStarted();  
```  
  
## <a name="requirements"></a><span data-ttu-id="5fd58-106">要求</span><span class="sxs-lookup"><span data-stu-id="5fd58-106">Requirements</span></span>  

 <span data-ttu-id="5fd58-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5fd58-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5fd58-108">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5fd58-108">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5fd58-109">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5fd58-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5fd58-110">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5fd58-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5fd58-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="5fd58-111">See also</span></span>

- [<span data-ttu-id="5fd58-112">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="5fd58-112">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
