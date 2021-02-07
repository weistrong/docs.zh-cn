---
description: 了解详细信息： ICorDebugVariableHome：： GetOffset 方法
title: ICorDebugVariableHome：： GetOffset 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetOffset
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetOffset
helpviewer_keywords:
- ICorDebugVariableHome::GetOffset method [.NET Framework debugging]
- GetOffset method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: f025c2e5-3f6c-4be8-9ffe-c8b214617dfe
topic_type:
- apiref
ms.openlocfilehash: 48b57856d2825dd2ea9328064a28783b4b36029b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728764"
---
# <a name="icordebugvariablehomegetoffset-method"></a>ICorDebugVariableHome：： GetOffset 方法

获取与基寄存器相对应的偏移量。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetOffset(  
    [out] LONG *pOffset  
);  
```  
  
## <a name="parameters"></a>参数  

 `pOffset`  
 弄基寄存器的偏移量。  
  
## <a name="return-value"></a>返回值  

 方法返回以下值：  
  
|值|说明|  
|-----------|-----------------|  
|`S_OK`|变量在寄存器相对内存位置。|  
|`E_FAIL`|变量不在寄存器相对内存位置中。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorDebugVariableHome 接口](icordebugvariablehome-interface.md)
