---
description: 了解详细信息： ICorDebugStepper2 接口
title: ICorDebugStepper2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugStepper2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper2
helpviewer_keywords:
- ICorDebugStepper2 interface [.NET Framework debugging]
ms.assetid: 7a191c2a-95ea-4d47-83b0-44de2b632d63
topic_type:
- apiref
ms.openlocfilehash: 31e9216535da239573a7a4ecde8cb2e670ad5418
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717545"
---
# <a name="icordebugstepper2-interface"></a>ICorDebugStepper2 接口

 (JMC) 调试提供 "仅我的代码" 支持。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[SetJMC 方法](icordebugstepper2-setjmc-method.md)|设置一个值，该值指定此 ICorDebugStepper 是否仅通过应用程序开发人员编写的代码执行步骤。|  
  
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
