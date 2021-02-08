---
description: 了解详细信息： CorDebugSetContextFlag 枚举
title: CorDebugSetContextFlag 枚举
ms.date: 03/30/2017
api_name:
- CorDebugSetContextFlag
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugSetContextFlag
helpviewer_keywords:
- CorDebugSetContextFlag enumeration [.NET Framework debugging]
ms.assetid: b30280bb-fe75-44ed-8589-bcff081fae44
topic_type:
- apiref
ms.openlocfilehash: 625f24e516ff462cf3d0e628dfff6c08793807ce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801548"
---
# <a name="cordebugsetcontextflag-enumeration"></a>CorDebugSetContextFlag 枚举

指示上下文是来自堆栈上的活动（或叶）帧，还是已通过从另一个帧展开来进行计算。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum CorDebugSetContextFlag  
{  
   SET_CONTEXT_FLAG_ACTIVE_FRAME = 1  
   SET_CONTEXT_FLAG_UNWIND_FRAME = 2  
}  CorDebugSetContextFlag;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|SET_CONTEXT_FLAG_ACTIVE_FRAME|上下文是线程的活动上下文。|  
|SET_CONTEXT_FLAG_UNWIND_FRAME|已通过从另一个帧展开上下文来计算上下文。|  
  
## <a name="remarks"></a>备注  

 `CorDebugSetContextFlag` 提供 [ICorDebugStackWalk：： SetContext](icordebugstackwalk-setcontext-method.md) 方法使用的值。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试枚举](debugging-enumerations.md)
- [调试](index.md)
