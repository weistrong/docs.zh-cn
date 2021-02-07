---
description: 了解详细信息： ICorDebugBreakpoint 接口
title: ICorDebugBreakpoint 接口
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpoint
helpviewer_keywords:
- ICorDebugBreakpoint interface [.NET Framework debugging]
ms.assetid: aa5ad3d7-e1bb-42af-99bc-471224e3bcaa
topic_type:
- apiref
ms.openlocfilehash: 63917512cceeccedea37acdf2ba7ab3b849d9fad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711799"
---
# <a name="icordebugbreakpoint-interface"></a>ICorDebugBreakpoint 接口

表示函数中的断点或某个值的监视点。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[Activate 方法](icordebugbreakpoint-activate-method.md)|设置此的活动状态 `ICorDebugBreakpoint` 。|  
|[IsActive 方法](icordebugbreakpoint-isactive-method.md)|获取一个值，该值指示此是否处于 `ICorDebugBreakpoint` 活动状态。|  
  
## <a name="remarks"></a>备注  

 断点不直接支持条件表达式。 如果需要此类功能，调试程序必须在顶层实现它 `ICorDebugBreakpoint` 。  
  
 ICorDebugFunctionBreakpoint 接口扩展 `ICorDebugBreakpoint` 以支持函数内的断点。  
  
> [!NOTE]
> 此接口不支持跨计算机或跨进程远程调用。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](debugging-interfaces.md)
