---
description: 了解详细信息： ICorDebugInternalFrame2 接口
title: ICorDebugInternalFrame2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugInternalFrame2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugInternalFrame2
helpviewer_keywords:
- ICorDebugInternalFrame2 interface [.NET Framework debugging]
ms.assetid: d4755569-85b8-4ff4-bf50-0e608e76429f
topic_type:
- apiref
ms.openlocfilehash: 3edc666c043513562b2fcece478b2879f294ce33
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791096"
---
# <a name="icordebuginternalframe2-interface"></a>ICorDebugInternalFrame2 接口

提供有关内部帧的信息，包括堆栈地址和相对于 ICorDebugFrame 对象的位置。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetFrameAddress 方法](icordebuginternalframe2-getframeaddress-method.md)|返回内部帧的堆栈地址。|  
|[IsCloserToLeaf 方法](icordebuginternalframe2-isclosertoleaf-method.md)|检查 `this` 内部帧是否接近于指定的 ICorDebugFrame 对象。|  
  
## <a name="remarks"></a>备注  

 此接口扩展 ICorDebugInternalFrame 接口。  
  
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
