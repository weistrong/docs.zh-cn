---
description: 了解详细信息： ICorDebugHeapEnum 接口
title: ICorDebugHeapEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugHeapEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapEnum
helpviewer_keywords:
- ICorDebugHeapEnum interface [.NET Framework debugging]
ms.assetid: 99cbc1eb-d539-4f76-a0d8-b93348112f14
topic_type:
- apiref
ms.openlocfilehash: c8a2f46bf412e2c4b2fe43d3eb50169191f40445
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660890"
---
# <a name="icordebugheapenum-interface"></a>ICorDebugHeapEnum 接口

提供针对托管堆上的对象的枚举器。 此接口是 ICorDebugEnum 接口的子类。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[下一方法](icordebugheapenum-next-method.md)|获取指定数量的 [COR_HEAPOBJECT](cor-heapobject-structure.md) 实例，这些实例包含有关托管堆上的对象的信息。|  
  
## <a name="remarks"></a>备注  

 `ICorDebugHeapEnum`接口实现 ICorDebugEnum 接口。  
  
 `ICorDebugHeapEnum`实例通过调用[ICorDebugProcess5：： EnumerateHeap](icordebugprocess5-enumerateheap-method.md)方法填充[COR_HEAPOBJECT](cor-heapobject-structure.md)的实例。 集合中的每个 [COR_HEAPOBJECT](cor-heapobject-structure.md) 实例都表示堆上的一个活动对象，或表示一个对象，该对象不是任何对象的根路径，但尚未由垃圾回收器收集。 可以通过调用[ICorDebugHeapEnum：： Next](icordebugheapenum-next-method.md)方法枚举集合中的[COR_HEAPOBJECT](cor-heapobject-structure.md)对象。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](debugging-interfaces.md)
