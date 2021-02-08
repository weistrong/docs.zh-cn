---
description: 了解详细信息： ICorDebugInstanceFieldSymbol 接口
title: ICorDebugInstanceFieldSymbol 接口
ms.date: 03/30/2017
ms.assetid: a4a8f259-b83a-4425-ae8b-72b067dbc0d9
ms.openlocfilehash: aa47c858ec5b4b0d04b851357fe81c0fc9b2e30a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791127"
---
# <a name="icordebuginstancefieldsymbol-interface"></a>ICorDebugInstanceFieldSymbol 接口

表示某一实例字段的调试符号信息。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetName 方法](icordebuginstancefieldsymbol-getname-method.md)|获取实例字段的名称。|  
|[GetOffset 方法](icordebuginstancefieldsymbol-getoffset-method.md)|获取父类中此示例字段的偏移量（以字节为单位）。|  
|[GetSize 方法](icordebuginstancefieldsymbol-getsize-method.md)|获取实例字段的大小（以字节为单位）。|  
  
## <a name="remarks"></a>备注  

 `ICorDebugInstanceFieldSymbol` 接口用于检索实例字段的调试符号信息。  
  
> [!NOTE]
> 此接口仅适用于 .NET Native。 如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorDebugStaticFieldSymbol 接口](icordebugstaticfieldsymbol-interface.md)
- [调试接口](debugging-interfaces.md)
- [调试](index.md)
