---
description: 了解详细信息： ICorProfilerCallback：： RemotingServerSendingReply 方法
title: ICorProfilerCallback::RemotingServerSendingReply 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingServerSendingReply
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingServerSendingReply
helpviewer_keywords:
- RemotingServerSendingReply method [.NET Framework profiling]
- ICorProfilerCallback::RemotingServerSendingReply method [.NET Framework profiling]
ms.assetid: dfe84a19-2e03-4be2-8b25-f02bad38e4a9
topic_type:
- apiref
ms.openlocfilehash: 236a707fcbc051a3d00c408f71f3b4f9f452c220
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788873"
---
# <a name="icorprofilercallbackremotingserversendingreply-method"></a><span data-ttu-id="fd531-103">ICorProfilerCallback::RemotingServerSendingReply 方法</span><span class="sxs-lookup"><span data-stu-id="fd531-103">ICorProfilerCallback::RemotingServerSendingReply Method</span></span>

<span data-ttu-id="fd531-104">通知探查器进程已处理完远程方法调用请求，即将通过通道传输答复。</span><span class="sxs-lookup"><span data-stu-id="fd531-104">Notifies the profiler that the process has finished processing a remote method invocation request and is about to transmit the reply through a channel.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd531-105">语法</span><span class="sxs-lookup"><span data-stu-id="fd531-105">Syntax</span></span>  
  
```cpp  
HRESULT RemotingServerSendingReply(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fd531-106">参数</span><span class="sxs-lookup"><span data-stu-id="fd531-106">Parameters</span></span>  

 `pCookie`  
 <span data-ttu-id="fd531-107">中指向 GUID 的指针，该 GUID 将与以下条件下的 [ICorProfilerCallback：： RemotingClientReceivingReply](icorprofilercallback-remotingclientreceivingreply-method.md) 中提供的值相对应：</span><span class="sxs-lookup"><span data-stu-id="fd531-107">[in] A pointer to a GUID that will correspond with the value provided in [ICorProfilerCallback::RemotingClientReceivingReply](icorprofilercallback-remotingclientreceivingreply-method.md) under these conditions:</span></span>  
  
- <span data-ttu-id="fd531-108">远程处理 GUID cookie 处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="fd531-108">Remoting GUID cookies are active.</span></span>  
  
- <span data-ttu-id="fd531-109">通道成功传输消息。</span><span class="sxs-lookup"><span data-stu-id="fd531-109">The channel succeeds in transmitting the message.</span></span>  
  
- <span data-ttu-id="fd531-110">GUID cookie 在客户端进程中处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="fd531-110">GUID cookies are active on the client-side process.</span></span>  
  
 <span data-ttu-id="fd531-111">这样就可以轻松地配对远程调用和逻辑调用堆栈的创建。</span><span class="sxs-lookup"><span data-stu-id="fd531-111">This allows easy pairing of remoting calls and the creation of a logical call stack.</span></span>  
  
 `fIsAsync`  
 <span data-ttu-id="fd531-112">中 `true` 如果调用是异步的，则该值为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="fd531-112">[in] A value that is `true` if the call is asynchronous; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd531-113">要求</span><span class="sxs-lookup"><span data-stu-id="fd531-113">Requirements</span></span>  

 <span data-ttu-id="fd531-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fd531-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fd531-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fd531-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fd531-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fd531-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fd531-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd531-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd531-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="fd531-118">See also</span></span>

- [<span data-ttu-id="fd531-119">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="fd531-119">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
