---
description: 了解详细信息： ICorDebugCode：： GetFunction 方法
title: ICorDebugCode::GetFunction 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetFunction
helpviewer_keywords:
- GetFunction method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetFunction method [.NET Framework debugging]
ms.assetid: c568b737-fdb2-4816-accd-051f5ab760f1
topic_type:
- apiref
ms.openlocfilehash: c90635bf1821d70d6d056d5cbd495ddfa2d2a2ff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711201"
---
# <a name="icordebugcodegetfunction-method"></a>ICorDebugCode::GetFunction 方法

获取与此 "ICorDebugCode" 关联的 "ICorDebugFunction"。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetFunction (  
    [out] ICorDebugFunction **ppFunction  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppFunction`  
 弄指向函数的地址的指针。  
  
## <a name="remarks"></a>备注  

 `ICorDebugCode` 和 `ICorDebugFunction` 保持一对一关系。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
