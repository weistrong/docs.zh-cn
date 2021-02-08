---
description: 了解详细信息： ICorProfilerCallback：： RemotingClientReceivingReply 方法
title: ICorProfilerCallback::RemotingClientReceivingReply 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingClientReceivingReply
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingClientReceivingReply
helpviewer_keywords:
- ICorProfilerCallback::RemotingClientReceivingReply method [.NET Framework profiling]
- RemotingClientReceivingReply method [.NET Framework profiling]
ms.assetid: 15cfc300-8231-4ecb-9a04-19851c3eb484
topic_type:
- apiref
ms.openlocfilehash: 4c1d42baa9f4381b66c9be75afa239899ae81b81
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788938"
---
# <a name="icorprofilercallbackremotingclientreceivingreply-method"></a><span data-ttu-id="7a0f1-103">ICorProfilerCallback::RemotingClientReceivingReply 方法</span><span class="sxs-lookup"><span data-stu-id="7a0f1-103">ICorProfilerCallback::RemotingClientReceivingReply Method</span></span>

<span data-ttu-id="7a0f1-104">通知探查器远程处理调用的服务器端部分已完成，并且客户端现在正在接收，并即将处理答复。</span><span class="sxs-lookup"><span data-stu-id="7a0f1-104">Notifies the profiler that the server-side portion of a remoting call has completed and the client is now receiving and about to process the reply.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a0f1-105">语法</span><span class="sxs-lookup"><span data-stu-id="7a0f1-105">Syntax</span></span>  
  
```cpp  
HRESULT RemotingClientReceivingReply(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);
```  
  
## <a name="parameters"></a><span data-ttu-id="7a0f1-106">参数</span><span class="sxs-lookup"><span data-stu-id="7a0f1-106">Parameters</span></span>  

 `pCookie`  
 <span data-ttu-id="7a0f1-107">中与以下条件下的 [ICorProfilerCallback：： RemotingServerSendingReply](icorprofilercallback-remotingserversendingreply-method.md) 中提供的值对应的值：</span><span class="sxs-lookup"><span data-stu-id="7a0f1-107">[in] A value that will correspond with the value provided in [ICorProfilerCallback::RemotingServerSendingReply](icorprofilercallback-remotingserversendingreply-method.md) under these conditions:</span></span>  
  
- <span data-ttu-id="7a0f1-108">远程处理 GUID cookie 处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="7a0f1-108">Remoting GUID cookies are active.</span></span>  
  
- <span data-ttu-id="7a0f1-109">通道成功传输消息。</span><span class="sxs-lookup"><span data-stu-id="7a0f1-109">The channel succeeds in transmitting the message.</span></span>  
  
- <span data-ttu-id="7a0f1-110">GUID cookie 在服务器端进程中处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="7a0f1-110">GUID cookies are active on the server-side process.</span></span>  
  
 <span data-ttu-id="7a0f1-111">这样就可以轻松地配对远程调用。</span><span class="sxs-lookup"><span data-stu-id="7a0f1-111">This allows easy pairing of remoting calls.</span></span>  
  
 `fIsAsync`  
 <span data-ttu-id="7a0f1-112">中 `true` 如果调用是异步的，则该值为; 否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="7a0f1-112">[in] A value that is `true` if the call is asynchronous; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a0f1-113">要求</span><span class="sxs-lookup"><span data-stu-id="7a0f1-113">Requirements</span></span>  

 <span data-ttu-id="7a0f1-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7a0f1-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a0f1-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7a0f1-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7a0f1-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7a0f1-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7a0f1-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7a0f1-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a0f1-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="7a0f1-118">See also</span></span>

- [<span data-ttu-id="7a0f1-119">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="7a0f1-119">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
