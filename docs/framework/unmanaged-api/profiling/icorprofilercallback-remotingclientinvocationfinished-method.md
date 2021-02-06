---
description: 了解详细信息： ICorProfilerCallback：： RemotingClientInvocationFinished 方法
title: ICorProfilerCallback::RemotingClientInvocationFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingClientInvocationFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingClientInvocationFinished
helpviewer_keywords:
- RemotingClientInvocationFinished method [.NET Framework profiling]
- ICorProfilerCallback::RemotingClientInvocationFinished method [.NET Framework profiling]
ms.assetid: ea4b283b-1210-4f41-a7a2-c398b1adde4e
topic_type:
- apiref
ms.openlocfilehash: bc15139e10b7634c50604d9a05ba290566145c21
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647994"
---
# <a name="icorprofilercallbackremotingclientinvocationfinished-method"></a><span data-ttu-id="eaceb-103">ICorProfilerCallback::RemotingClientInvocationFinished 方法</span><span class="sxs-lookup"><span data-stu-id="eaceb-103">ICorProfilerCallback::RemotingClientInvocationFinished Method</span></span>

<span data-ttu-id="eaceb-104">通知探查器远程处理调用已在客户端上完成运行。</span><span class="sxs-lookup"><span data-stu-id="eaceb-104">Notifies the profiler that a remoting call has run to completion on the client.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eaceb-105">语法</span><span class="sxs-lookup"><span data-stu-id="eaceb-105">Syntax</span></span>  
  
```cpp  
HRESULT RemotingClientInvocationFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="eaceb-106">备注</span><span class="sxs-lookup"><span data-stu-id="eaceb-106">Remarks</span></span>  

 <span data-ttu-id="eaceb-107">如果远程处理调用是同步的，则它还会在服务器上运行到完成。</span><span class="sxs-lookup"><span data-stu-id="eaceb-107">If the remoting call was synchronous, it has also run to completion on the server.</span></span> <span data-ttu-id="eaceb-108">如果远程处理调用是异步的，则在处理调用时可能仍会出现回复。</span><span class="sxs-lookup"><span data-stu-id="eaceb-108">If the remoting call was asynchronous, a reply might still be expected when the call is handled.</span></span> <span data-ttu-id="eaceb-109">如果需要答复，则会作为对 [ICorProfilerCallback：： RemotingClientReceivingReply](icorprofilercallback-remotingclientreceivingreply-method.md) 的调用，以及对的其他调用 `RemotingClientInvocationFinished` 以指示异步调用所需的辅助处理。</span><span class="sxs-lookup"><span data-stu-id="eaceb-109">If a reply is expected, it will occur as a call to [ICorProfilerCallback::RemotingClientReceivingReply](icorprofilercallback-remotingclientreceivingreply-method.md) and an additional call to `RemotingClientInvocationFinished` to indicate the required secondary processing of an asynchronous call.</span></span>  
  
 <span data-ttu-id="eaceb-110">以下每对回调都将在同一线程上进行：</span><span class="sxs-lookup"><span data-stu-id="eaceb-110">Each of the following pairs of callbacks will occur on the same thread:</span></span>  
  
- <span data-ttu-id="eaceb-111">`RemotingClientInvocationStarted` 和 [ICorProfilerCallback：： RemotingClientSendingMessage](icorprofilercallback-remotingclientsendingmessage-method.md)</span><span class="sxs-lookup"><span data-stu-id="eaceb-111">`RemotingClientInvocationStarted` and [ICorProfilerCallback::RemotingClientSendingMessage](icorprofilercallback-remotingclientsendingmessage-method.md)</span></span>  
  
- <span data-ttu-id="eaceb-112">[ICorProfilerCallback：： RemotingClientReceivingReply](icorprofilercallback-remotingclientreceivingreply-method.md) 和 [ICorProfilerCallback：： RemotingClientInvocationFinished](icorprofilercallback-remotingclientinvocationfinished-method.md)</span><span class="sxs-lookup"><span data-stu-id="eaceb-112">[ICorProfilerCallback::RemotingClientReceivingReply](icorprofilercallback-remotingclientreceivingreply-method.md) and [ICorProfilerCallback::RemotingClientInvocationFinished](icorprofilercallback-remotingclientinvocationfinished-method.md)</span></span>  
  
- <span data-ttu-id="eaceb-113">[ICorProfilerCallback：： RemotingServerInvocationReturned](icorprofilercallback-remotingserverinvocationreturned-method.md) 和 [ICorProfilerCallback：： RemotingServerSendingReply](icorprofilercallback-remotingserversendingreply-method.md)</span><span class="sxs-lookup"><span data-stu-id="eaceb-113">[ICorProfilerCallback::RemotingServerInvocationReturned](icorprofilercallback-remotingserverinvocationreturned-method.md) and [ICorProfilerCallback::RemotingServerSendingReply](icorprofilercallback-remotingserversendingreply-method.md)</span></span>  
  
 <span data-ttu-id="eaceb-114">应注意远程处理回调的以下问题：</span><span class="sxs-lookup"><span data-stu-id="eaceb-114">You should be aware of the following issues with the remoting callbacks:</span></span>  
  
- <span data-ttu-id="eaceb-115">远程处理函数的执行不会由探查器 API 反射，因此无法正确地接收从客户端调用并在服务器上执行的函数的通知。</span><span class="sxs-lookup"><span data-stu-id="eaceb-115">Execution of a remoting function is not reflected by the profiler API, so notifications for functions that are called from the client and executed on the server are not properly received.</span></span> <span data-ttu-id="eaceb-116">实际调用是通过代理对象进行的;对于探查器，似乎某些函数是 JIT 编译的，但从未使用过。</span><span class="sxs-lookup"><span data-stu-id="eaceb-116">The actual invocation happens via a proxy object; to the profiler, it appears that certain functions are JIT-compiled but never used.</span></span>  
  
- <span data-ttu-id="eaceb-117">探查器不会为异步远程处理事件接收准确的通知。</span><span class="sxs-lookup"><span data-stu-id="eaceb-117">The profiler does not receive accurate notifications for asynchronous remoting events.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eaceb-118">要求</span><span class="sxs-lookup"><span data-stu-id="eaceb-118">Requirements</span></span>  

 <span data-ttu-id="eaceb-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="eaceb-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eaceb-120">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="eaceb-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="eaceb-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eaceb-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eaceb-122">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eaceb-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eaceb-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="eaceb-123">See also</span></span>

- [<span data-ttu-id="eaceb-124">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="eaceb-124">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
