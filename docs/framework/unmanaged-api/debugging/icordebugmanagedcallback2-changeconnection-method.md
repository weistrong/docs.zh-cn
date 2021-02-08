---
description: 了解详细信息： ICorDebugManagedCallback2：： ChangeConnection 方法
title: ICorDebugManagedCallback2::ChangeConnection 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.ChangeConnection
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::ChangeConnection
helpviewer_keywords:
- ICorDebugManagedCallback2::ChangeConnection method [.NET Framework debugging]
- ChangeConnection method [.NET Framework debugging]
ms.assetid: 7263f9a9-4c0b-4d82-a181-288873fb2b18
topic_type:
- apiref
ms.openlocfilehash: 854ea7f40cad9bce613b4034afe7688f4aaf4e52
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790914"
---
# <a name="icordebugmanagedcallback2changeconnection-method"></a>ICorDebugManagedCallback2::ChangeConnection 方法

通知调试器与指定连接关联的任务集已更改。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT ChangeConnection (  
    [in] ICorDebugProcess     *pProcess,  
    [in] CONNID               dwConnectionId  
);  
```  
  
## <a name="parameters"></a>参数  

 `pProcess`  
 中一个指向 "ICorDebugProcess" 对象的指针，该对象表示包含已更改的连接的进程。  
  
 `dwConnectionId`  
 中已更改的连接的 ID。  
  
## <a name="remarks"></a>备注  

 `ChangeConnection`在以下任一情况下，都将激发回调：  
  
- 调试器附加到包含连接的进程时。 在这种情况下，运行时将为进程中的每个连接生成并调度一个 [ICorDebugManagedCallback2：： CreateConnection](icordebugmanagedcallback2-createconnection-method.md) 事件和一个 `ChangeConnection` 事件。 将 `ChangeConnection` 为每个现有连接生成一个事件，而不管该连接的一组任务在创建后是否已更改。  
  
- 当主机在[托管 API](../hosting/index.md)中调用[ICLRDebugManager：： SetConnectionTasks](../hosting/iclrdebugmanager-setconnectiontasks-method.md)时。  
  
 调试器应扫描进程中的所有线程以选取新的更改。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorDebugManagedCallback2 接口](icordebugmanagedcallback2-interface.md)
- [ICorDebugManagedCallback 接口](icordebugmanagedcallback-interface.md)
