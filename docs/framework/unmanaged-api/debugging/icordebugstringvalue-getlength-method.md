---
description: 了解详细信息： ICorDebugStringValue：： GetLength 方法
title: ICorDebugStringValue::GetLength 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStringValue.GetLength
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStringValue::GetLength
helpviewer_keywords:
- ICorDebugStringValue::GetLength method [.NET Framework debugging]
- GetLength method [.NET Framework debugging]
ms.assetid: a1ebfc69-46a6-4225-8788-b7cfb2f15e1d
topic_type:
- apiref
ms.openlocfilehash: ae4d42b5b65e5f80e884415a5acfc7f894ffe11e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717376"
---
# <a name="icordebugstringvaluegetlength-method"></a>ICorDebugStringValue::GetLength 方法

获取此 ICorDebugStringValue 引用的字符串中的字符数。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetLength (  
    [out] ULONG32   *pcchString  
);  
```  
  
## <a name="parameters"></a>参数  

 `pcchString`  
 弄一个指向值的指针，该值指定此对象所引用的字符串的长度 `ICorDebugStringValue` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
