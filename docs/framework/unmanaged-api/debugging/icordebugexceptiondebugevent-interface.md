---
description: 了解详细信息： ICorDebugExceptionDebugEvent 接口
title: “ICor调试异常调试事件”接口
ms.date: 03/30/2017
ms.assetid: f9ba60d8-b54d-417e-bb3e-fde4b41ca44c
ms.openlocfilehash: eacaa344763fb77faef5f66282809d741f017b37
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693416"
---
# <a name="icordebugexceptiondebugevent-interface"></a>“ICor调试异常调试事件”接口

扩展 [ICorDebugDebugEvent](icordebugdebugevent-interface.md) 接口以支持异常事件。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetFlags 方法](icordebugexceptiondebugevent-getflags-method.md)|获取指示是否可拦截异常的标志。|  
|[GetNativeIP 方法](icordebugexceptiondebugevent-getnativeip-method.md)|获取此异常调试事件的本机接口指针。|  
|[GetStackPointer 方法](icordebugexceptiondebugevent-getstackpointer-method.md)|获取此异常调试事件的堆栈指针。|  
  
## <a name="remarks"></a>备注  

 `ICorDebugExceptionDebugEvent` 接口由以下事件类型实现：  
  
- [MANAGED_EXCEPTION_FIRST_CHANCE](cordebugrecordformat-enumeration.md)  
  
- [MANAGED_EXCEPTION_USER_FIRST_CHANCE](cordebugrecordformat-enumeration.md)  
  
- [MANAGED_EXCEPTION_CATCH_HANDLER_FOUND](cordebugrecordformat-enumeration.md)  
  
- [MANAGED_EXCEPTION_UNHANDLED](cordebugrecordformat-enumeration.md)  
  
> [!NOTE]
> 此接口仅适用于 .NET Native。 尝试调用 `QueryInterface` 来检索接口指针会为 .NET Native 外部的 ICorDebug 方案返回 `E_NOINTERFACE`。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](debugging-interfaces.md)
- [调试](index.md)
