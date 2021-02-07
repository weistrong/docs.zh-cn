---
description: 了解详细信息： ICorDebugValue：： GetType 方法
title: ICorDebugValue::GetType 方法
ms.date: 03/30/2017
api_name:
- ICorDebugValue.GetType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue::GetType
helpviewer_keywords:
- ICorDebugValue::GetType method [.NET Framework debugging]
- GetType method, ICorDebugValue interface [.NET Framework debugging]
ms.assetid: 41e2d503-e1f1-407b-abe0-6a29adb3e0d1
topic_type:
- apiref
ms.openlocfilehash: 750e73634683a03e811d2756cc62c16b6dcea3de
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690320"
---
# <a name="icordebugvaluegettype-method"></a>ICorDebugValue::GetType 方法

获取此 "ICorDebugValue" 对象的基元类型。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetType (  
    [out] CorElementType   *pType  
);  
```  
  
## <a name="parameters"></a>参数  

 `pType`  
 弄一个指针，指向 "CorElementType" 枚举的值，该值指示值的类型。  
  
## <a name="remarks"></a>备注  

 如果对象是复杂的运行时类型，则可以通过接口的相应子类检查该类型 `ICorDebugValue` 。 例如，"ICorDebugObjectValue" 是从继承的，它 `ICorDebugValue` 表示一个复杂类型。  
  
 `GetType`和[ICorDebugObjectValue：： GetClass](icordebugobjectvalue-getclass-method.md)方法各自返回值类型的相关信息。 它们都是由识别泛型的 [ICorDebugValue2：： GetExactType](icordebugvalue2-getexacttype-method.md) 方法取代的。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅
