---
description: 了解详细信息： ICorProfilerCallback：： RemotingClientSendingMessage 方法
title: ICorProfilerCallback::RemotingClientSendingMessage 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingClientSendingMessage
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingClientSendingMessage
helpviewer_keywords:
- RemotingClientSendingMessage method [.NET Framework profiling]
- ICorProfilerCallback::RemotingClientSendingMessage method [.NET Framework profiling]
ms.assetid: 54d9a5a5-3877-49c1-a503-ce7c7943bc2a
topic_type:
- apiref
ms.openlocfilehash: 3d075b3f3c3ffe63c9d4401bdc182037593b5b19
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788925"
---
# <a name="icorprofilercallbackremotingclientsendingmessage-method"></a><span data-ttu-id="f45ba-103">ICorProfilerCallback::RemotingClientSendingMessage 方法</span><span class="sxs-lookup"><span data-stu-id="f45ba-103">ICorProfilerCallback::RemotingClientSendingMessage Method</span></span>

<span data-ttu-id="f45ba-104">通知探查器客户端正在向服务器发送请求。</span><span class="sxs-lookup"><span data-stu-id="f45ba-104">Notifies the profiler that the client is sending a request to the server.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f45ba-105">语法</span><span class="sxs-lookup"><span data-stu-id="f45ba-105">Syntax</span></span>  
  
```cpp  
HRESULT RemotingClientSendingMessage(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f45ba-106">参数</span><span class="sxs-lookup"><span data-stu-id="f45ba-106">Parameters</span></span>  

 `pCookie`  
 <span data-ttu-id="f45ba-107">中与以下条件下的 [ICorProfilerCallback：： RemotingServerReceivingMessage](icorprofilercallback-remotingserverreceivingmessage-method.md) 中提供的值对应的值：</span><span class="sxs-lookup"><span data-stu-id="f45ba-107">[in] A value that corresponds with the value provided in [ICorProfilerCallback::RemotingServerReceivingMessage](icorprofilercallback-remotingserverreceivingmessage-method.md) under these conditions:</span></span>  
  
- <span data-ttu-id="f45ba-108">远程处理 GUID cookie 处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="f45ba-108">Remoting GUID cookies are active.</span></span>  
  
- <span data-ttu-id="f45ba-109">通道成功传输消息。</span><span class="sxs-lookup"><span data-stu-id="f45ba-109">The channel succeeds in transmitting the message.</span></span>  
  
- <span data-ttu-id="f45ba-110">GUID cookie 在服务器端进程中处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="f45ba-110">GUID cookies are active on the server-side process.</span></span>  
  
 <span data-ttu-id="f45ba-111">这样就可以轻松地配对远程调用和逻辑调用堆栈的创建。</span><span class="sxs-lookup"><span data-stu-id="f45ba-111">This allows easy pairing of remoting calls and the creation of a logical call stack.</span></span>  
  
 `fIsAsync`  
 <span data-ttu-id="f45ba-112">中 `true` 如果调用是异步的，则该值为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="f45ba-112">[in] A value that is `true` if the call is asynchronous; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f45ba-113">要求</span><span class="sxs-lookup"><span data-stu-id="f45ba-113">Requirements</span></span>  

 <span data-ttu-id="f45ba-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f45ba-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f45ba-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="f45ba-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="f45ba-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f45ba-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f45ba-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f45ba-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f45ba-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="f45ba-118">See also</span></span>

- [<span data-ttu-id="f45ba-119">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="f45ba-119">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
