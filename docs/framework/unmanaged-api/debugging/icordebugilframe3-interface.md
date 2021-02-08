---
description: 了解详细信息： ICorDebugILFrame3 接口
title: ICorDebugILFrame3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 15212cb5-93d4-4025-bec9-d4b9919eb1fe
topic_type:
- apiref
ms.openlocfilehash: a34a3f0941871a2d0a63fb2d9f78ccb7ff455866
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791252"
---
# <a name="icordebugilframe3-interface"></a>ICorDebugILFrame3 接口

提供用于封装函数的返回值的方法。 `ICorDebugILFrame3` 是 ICorDebugILFrame 和 ICorDebugILFrame2 接口的逻辑扩展。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetReturnValueForILOffset 方法](icordebugilframe3-getreturnvalueforiloffset-method.md)|获取一个 ICorDebugValue 对象，该对象封装函数的返回值。|  
  
## <a name="remarks"></a>备注  
  
> [!NOTE]
> 此接口不支持跨计算机或跨进程远程调用。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorDebugCode3 接口](icordebugcode3-interface.md)
- [调试接口](debugging-interfaces.md)
