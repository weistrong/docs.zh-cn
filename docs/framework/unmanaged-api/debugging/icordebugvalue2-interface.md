---
description: 了解详细信息： ICorDebugValue2 接口
title: ICorDebugValue2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugValue2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue2
helpviewer_keywords:
- ICorDebugValue2 interface [.NET Framework debugging]
ms.assetid: 3ff2ad2a-da5a-461b-8627-1a8eba49df9c
topic_type:
- apiref
ms.openlocfilehash: b408bb5d1732a60fc9aa8ffb93321d3542f2cab7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690257"
---
# <a name="icordebugvalue2-interface"></a>ICorDebugValue2 接口

扩展 "ICorDebugValue" 接口，以提供对 "ICorDebugType" 对象的支持。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetExactType 方法](icordebugvalue2-getexacttype-method.md)|获取一个接口指针，该指针指向 `ICorDebugType` 表示 <xref:System.Type> 此值的的对象。|  
  
## <a name="remarks"></a>备注  
  
> [!NOTE]
> 此接口不支持跨计算机或跨进程远程调用。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](debugging-interfaces.md)

- [ICorDebugValue3 接口](icordebugvalue3-interface.md)
