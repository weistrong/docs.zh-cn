---
description: 了解详细信息： ICorDebugHeapSegmentEnum 接口
title: ICorDebugHeapSegmentEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugHealRegionEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapSegmentEnum
helpviewer_keywords:
- ICorDebugHeapSegmentEnum interface [.NET Framework debugging]
ms.assetid: 20fc1b9d-e228-4107-bd76-53934c1724b9
topic_type:
- apiref
ms.openlocfilehash: 614bae0ea5e3eb7816fdeec23a0dc7aa6e44801d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660877"
---
# <a name="icordebugheapsegmentenum-interface"></a>ICorDebugHeapSegmentEnum 接口

提供针对托管堆的内存区域的枚举器。 此接口是 ICorDebugEnum 接口的子类。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[下一方法](icordebugheapsegmentenum-next-method.md)|获取指定数量的 [COR_SEGMENT](cor-segment-structure.md) 实例，这些实例包含有关托管堆区域的信息。|  
  
## <a name="remarks"></a>备注  

 `ICorDebugHeapSegmentEnum`接口实现 ICorDebugEnum 接口。  
  
 `ICorDebugHeapSegmentEnum`实例通过调用[ICorDebugProcess5：： EnumerateHeapRegions](icordebugprocess5-enumerateheapregions-method.md)方法填充[COR_SEGMENT](cor-segment-structure.md)的实例。 可以通过调用[ICorDebugHeapSegmentEnum：： Next](icordebugheapsegmentenum-next-method.md)方法枚举集合中的[COR_SEGMENT](cor-segment-structure.md)对象。  
  
 `ICorDebugHeapSegmentEnum`集合对象枚举可能包含托管对象的所有内存区域，但不保证托管对象实际驻留在这些区域中。 它可能包括有关空的或保留的内存区域的信息。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](debugging-interfaces.md)
