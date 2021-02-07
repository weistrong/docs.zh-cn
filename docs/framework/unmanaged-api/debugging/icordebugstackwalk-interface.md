---
description: 了解详细信息： ICorDebugStackWalk 接口
title: ICorDebugStackWalk 接口
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk
helpviewer_keywords:
- ICorDebugStackWalk interface [.NET Framework debugging]
ms.assetid: 16d695e8-975d-431b-8421-e9e6c3e3f476
topic_type:
- apiref
ms.openlocfilehash: 27dcdfc90829a3a28d81ad28dce0cd4d1d674948
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738086"
---
# <a name="icordebugstackwalk-interface"></a>ICorDebugStackWalk 接口

提供用于获取线程堆栈上的托管方法或帧的方法。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetContext 方法](icordebugstackwalk-getcontext-method.md)|返回对象中当前帧的上下文 `ICorDebugStackWalk` 。|  
|[SetContext 方法](icordebugstackwalk-setcontext-method.md)|将 `ICorDebugStackWalk` 对象的当前上下文设置为线程的有效上下文。|  
|[下一方法](icordebugstackwalk-next-method.md)|将 `ICorDebugStackWalk` 对象移动到下一帧。|  
|[GetFrame 方法](icordebugstackwalk-getframe-method.md)|获取对象中的当前帧 `ICorDebugStackWalk` 。|  
  
## <a name="remarks"></a>备注  
  
> [!NOTE]
> 此接口不支持跨计算机或跨进程远程调用。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](debugging-interfaces.md)
- [调试](index.md)
