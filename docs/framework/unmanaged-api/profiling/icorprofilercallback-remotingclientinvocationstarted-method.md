---
description: 了解详细信息： ICorProfilerCallback：： RemotingClientInvocationStarted 方法
title: ICorProfilerCallback::RemotingClientInvocationStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingClientInvocationStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingClientInvocationStarted
helpviewer_keywords:
- RemotingClientInvocationStarted method [.NET Framework profiling]
- ICorProfilerCallback::RemotingClientInvocationStarted method [.NET Framework profiling]
ms.assetid: 796b63f3-c809-47f1-89cc-b23ad8eb5e79
topic_type:
- apiref
ms.openlocfilehash: 3727383c3a23fa9e4327970e84c6ebde4ab14db0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788964"
---
# <a name="icorprofilercallbackremotingclientinvocationstarted-method"></a><span data-ttu-id="6c28c-103">ICorProfilerCallback::RemotingClientInvocationStarted 方法</span><span class="sxs-lookup"><span data-stu-id="6c28c-103">ICorProfilerCallback::RemotingClientInvocationStarted Method</span></span>

<span data-ttu-id="6c28c-104">通知探查器已开始远程调用。</span><span class="sxs-lookup"><span data-stu-id="6c28c-104">Notifies the profiler that a remoting call has started.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c28c-105">语法</span><span class="sxs-lookup"><span data-stu-id="6c28c-105">Syntax</span></span>  
  
```cpp  
HRESULT RemotingClientInvocationStarted();  
```  
  
## <a name="remarks"></a><span data-ttu-id="6c28c-106">备注</span><span class="sxs-lookup"><span data-stu-id="6c28c-106">Remarks</span></span>  

 <span data-ttu-id="6c28c-107">此事件对于同步和异步调用是相同的。</span><span class="sxs-lookup"><span data-stu-id="6c28c-107">This event is the same for synchronous and asynchronous calls.</span></span>  
  
 <span data-ttu-id="6c28c-108">以下每对回调都将在同一线程上进行：</span><span class="sxs-lookup"><span data-stu-id="6c28c-108">Each of the following pairs of callbacks will occur on the same thread:</span></span>  
  
- <span data-ttu-id="6c28c-109">`RemotingClientInvocationStarted` 和 [ICorProfilerCallback：： RemotingClientSendingMessage](icorprofilercallback-remotingclientsendingmessage-method.md)</span><span class="sxs-lookup"><span data-stu-id="6c28c-109">`RemotingClientInvocationStarted` and [ICorProfilerCallback::RemotingClientSendingMessage](icorprofilercallback-remotingclientsendingmessage-method.md)</span></span>  
  
- <span data-ttu-id="6c28c-110">[ICorProfilerCallback：： RemotingClientReceivingReply](icorprofilercallback-remotingclientreceivingreply-method.md) 和 [ICorProfilerCallback：： RemotingClientInvocationFinished](icorprofilercallback-remotingclientinvocationfinished-method.md)</span><span class="sxs-lookup"><span data-stu-id="6c28c-110">[ICorProfilerCallback::RemotingClientReceivingReply](icorprofilercallback-remotingclientreceivingreply-method.md) and [ICorProfilerCallback::RemotingClientInvocationFinished](icorprofilercallback-remotingclientinvocationfinished-method.md)</span></span>  
  
- <span data-ttu-id="6c28c-111">[ICorProfilerCallback：： RemotingServerInvocationReturned](icorprofilercallback-remotingserverinvocationreturned-method.md) 和 [ICorProfilerCallback：： RemotingServerSendingReply](icorprofilercallback-remotingserversendingreply-method.md)</span><span class="sxs-lookup"><span data-stu-id="6c28c-111">[ICorProfilerCallback::RemotingServerInvocationReturned](icorprofilercallback-remotingserverinvocationreturned-method.md) and [ICorProfilerCallback::RemotingServerSendingReply](icorprofilercallback-remotingserversendingreply-method.md)</span></span>  
  
 <span data-ttu-id="6c28c-112">应注意远程处理回调的以下问题：</span><span class="sxs-lookup"><span data-stu-id="6c28c-112">You should be aware of the following issues with the remoting callbacks:</span></span>  
  
- <span data-ttu-id="6c28c-113">远程处理函数的执行不会由探查器 API 反射，因此无法正确地接收从客户端调用并在服务器上执行的函数的通知。</span><span class="sxs-lookup"><span data-stu-id="6c28c-113">Execution of a remoting function is not reflected by the profiler API, so notifications for functions that are called from the client and executed on the server are not properly received.</span></span> <span data-ttu-id="6c28c-114">实际调用是通过代理对象进行的;对于探查器，似乎某些函数是 JIT 编译的，但从未使用过。</span><span class="sxs-lookup"><span data-stu-id="6c28c-114">The actual invocation happens via a proxy object; to the profiler, it appears that certain functions are JIT-compiled but never used.</span></span>  
  
- <span data-ttu-id="6c28c-115">探查器不会为异步远程处理事件接收准确的通知。</span><span class="sxs-lookup"><span data-stu-id="6c28c-115">The profiler does not receive accurate notifications for asynchronous remoting events.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6c28c-116">要求</span><span class="sxs-lookup"><span data-stu-id="6c28c-116">Requirements</span></span>  

 <span data-ttu-id="6c28c-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6c28c-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c28c-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="6c28c-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="6c28c-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6c28c-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6c28c-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c28c-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c28c-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="6c28c-121">See also</span></span>

- [<span data-ttu-id="6c28c-122">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="6c28c-122">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
