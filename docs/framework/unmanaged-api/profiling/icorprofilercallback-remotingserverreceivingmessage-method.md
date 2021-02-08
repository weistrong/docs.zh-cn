---
description: 了解详细信息： ICorProfilerCallback：： RemotingServerReceivingMessage 方法
title: ICorProfilerCallback::RemotingServerReceivingMessage 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingServerReceivingMessage
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingServerReceivingMessage
helpviewer_keywords:
- ICorProfilerCallback::RemotingServerReceivingMessage method [.NET Framework profiling]
- RemotingServerReceivingMessage method [.NET Framework profiling]
ms.assetid: 5604d21f-e6b7-490e-b469-42122a7568e1
topic_type:
- apiref
ms.openlocfilehash: 5efa706d934158d09796dfab40b132a334c10ffd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788886"
---
# <a name="icorprofilercallbackremotingserverreceivingmessage-method"></a><span data-ttu-id="a07a6-103">ICorProfilerCallback::RemotingServerReceivingMessage 方法</span><span class="sxs-lookup"><span data-stu-id="a07a6-103">ICorProfilerCallback::RemotingServerReceivingMessage Method</span></span>

<span data-ttu-id="a07a6-104">通知探查器进程已收到远程方法调用或激活请求。</span><span class="sxs-lookup"><span data-stu-id="a07a6-104">Notifies the profiler that the process has received a remote method invocation or activation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a07a6-105">语法</span><span class="sxs-lookup"><span data-stu-id="a07a6-105">Syntax</span></span>  
  
```cpp  
HRESULT RemotingClientSendingMessage(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a07a6-106">参数</span><span class="sxs-lookup"><span data-stu-id="a07a6-106">Parameters</span></span>  

 `pCookie`  
 <span data-ttu-id="a07a6-107">中与以下条件下的 [ICorProfilerCallback：： RemotingClientSendingMessage](icorprofilercallback-remotingclientsendingmessage-method.md) 中提供的值对应的值：</span><span class="sxs-lookup"><span data-stu-id="a07a6-107">[in] A value that will correspond with the value provided in [ICorProfilerCallback::RemotingClientSendingMessage](icorprofilercallback-remotingclientsendingmessage-method.md) under these conditions:</span></span>  
  
- <span data-ttu-id="a07a6-108">远程处理 GUID cookie 处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="a07a6-108">Remoting GUID cookies are active.</span></span>  
  
- <span data-ttu-id="a07a6-109">通道成功传输消息。</span><span class="sxs-lookup"><span data-stu-id="a07a6-109">The channel succeeds in transmitting the message.</span></span>  
  
- <span data-ttu-id="a07a6-110">GUID cookie 在客户端进程中处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="a07a6-110">GUID cookies are active on the client-side process.</span></span>  
  
 <span data-ttu-id="a07a6-111">这样就可以轻松地配对远程调用和逻辑调用堆栈的创建。</span><span class="sxs-lookup"><span data-stu-id="a07a6-111">This allows easy pairing of remoting calls and the creation of a logical call stack.</span></span>  
  
 `fIsAsync`  
 <span data-ttu-id="a07a6-112">中 `true` 如果调用是异步的，则该值为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="a07a6-112">[in] A value that is `true` if the call is asynchronous; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a07a6-113">备注</span><span class="sxs-lookup"><span data-stu-id="a07a6-113">Remarks</span></span>  

 <span data-ttu-id="a07a6-114">如果消息请求是异步的，则该请求可由任意线程提供服务。</span><span class="sxs-lookup"><span data-stu-id="a07a6-114">If the message request is asynchronous, the request can be serviced by any arbitrary thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a07a6-115">要求</span><span class="sxs-lookup"><span data-stu-id="a07a6-115">Requirements</span></span>  

 <span data-ttu-id="a07a6-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a07a6-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a07a6-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a07a6-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a07a6-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a07a6-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a07a6-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a07a6-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a07a6-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="a07a6-120">See also</span></span>

- [<span data-ttu-id="a07a6-121">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="a07a6-121">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
