---
description: 了解详细信息： ICorDebugArrayValue：： GetElement 方法
title: ICorDebugArrayValue::GetElement 方法
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetElement
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetElement
helpviewer_keywords:
- GetElement method [.NET Framework debugging]
- ICorDebugArrayValue::GetElement method [.NET Framework debugging]
ms.assetid: 7ac3cba5-c282-402e-b7ef-b46634f5176b
topic_type:
- apiref
ms.openlocfilehash: dfae074b78735934d1e71b13ce01c24741a5f2ed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723057"
---
# <a name="icordebugarrayvaluegetelement-method"></a>ICorDebugArrayValue::GetElement 方法

获取给定数组元素的值。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetElement (  
    [in]  ULONG32          cdim,  
    [in, size_is(cdim), length_is(cdim)]
         ULONG32           indices[],  
    [out] ICorDebugValue   **ppValue  
);  
```  
  
## <a name="parameters"></a>参数  

 `cdim`  
 中此对象的维度数 `ICorDebugArrayValue` 。  
  
 此值也是数组的大小， `indices` 因为其大小等于对象的维度数 `ICorDebugArrayValue` 。  
  
 `indices`  
 中索引值的数组，其中每个值指定对象的维度内的位置 `ICorDebugArrayValue` 。  
  
 此值不得为 Null。  
  
 `ppValue`  
 弄指向 ICorDebugValue 对象的地址的指针，该对象表示指定元素的值。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
