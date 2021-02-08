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
# <a name="icorprofilercallbackremotingserverreceivingmessage-method"></a>ICorProfilerCallback::RemotingServerReceivingMessage 方法

通知探查器进程已收到远程方法调用或激活请求。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT RemotingClientSendingMessage(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);  
```  
  
## <a name="parameters"></a>参数  

 `pCookie`  
 中与以下条件下的 [ICorProfilerCallback：： RemotingClientSendingMessage](icorprofilercallback-remotingclientsendingmessage-method.md) 中提供的值对应的值：  
  
- 远程处理 GUID cookie 处于活动状态。  
  
- 通道成功传输消息。  
  
- GUID cookie 在客户端进程中处于活动状态。  
  
 这样就可以轻松地配对远程调用和逻辑调用堆栈的创建。  
  
 `fIsAsync`  
 中 `true` 如果调用是异步的，则该值为; 否则为 `false` 。  
  
## <a name="remarks"></a>备注  

 如果消息请求是异步的，则该请求可由任意线程提供服务。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorProfilerCallback 接口](icorprofilercallback-interface.md)
