---
description: 了解详细信息： ICorDebugVariableSymbol：： GetSlotIndex 方法
title: ICorDebugVariableSymbol::GetSlotIndex 方法
ms.date: 03/30/2017
ms.assetid: 09c19f5f-afc4-4e0c-bffe-cd7147bc7a43
ms.openlocfilehash: 3b5cba06a5e80ffa323d2e6521e9ec4666f6f5f3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790550"
---
# <a name="icordebugvariablesymbolgetslotindex-method"></a>ICorDebugVariableSymbol::GetSlotIndex 方法

获取本地变量的托管槽索引。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetSlotIndex(  
   [out] ULONG32 *pSlotIndex  
);  
```  
  
## <a name="parameters"></a>参数  

 `pSlotIndex`  
 [out] 指向本地变量的槽索引的指针。  
  
## <a name="return-value"></a>返回值  

 `S_OK` 如果成功。 如果变量是一个函数自变量，则为 `E_FAIL`。  
  
## <a name="remarks"></a>备注  

 本地变量的托管槽索引可用于检索变量的元数据信息  
  
> [!NOTE]
> 此方法仅适用于 .NET Native。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorDebugVariableSymbol 接口](icordebugvariablesymbol-interface.md)
- [调试接口](debugging-interfaces.md)
