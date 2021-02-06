---
description: 了解详细信息： ICorDebugHeapValue2 接口
title: ICorDebugHeapValue2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue2
helpviewer_keywords:
- ICorDebugHeapValue2 interface [.NET Framework debugging]
ms.assetid: 87360a52-90b1-4ada-80c0-589a556116d8
topic_type:
- apiref
ms.openlocfilehash: 04c757540a11a74db0a9bdf7f638786af46055c7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660747"
---
# <a name="icordebugheapvalue2-interface"></a>ICorDebugHeapValue2 接口

ICorDebugHeapValue 的扩展，它为公共语言运行时 (CLR) 句柄提供支持。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[CreateHandle 方法](icordebugheapvalue2-createhandle-method.md)|为此对象创建指定类型的句柄 `ICorDebugHeapValue2` 。|  
  
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
