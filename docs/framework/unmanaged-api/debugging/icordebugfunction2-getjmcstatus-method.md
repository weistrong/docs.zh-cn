---
description: 了解详细信息： ICorDebugFunction2：： GetJMCStatus 方法
title: ICorDebugFunction2::GetJMCStatus 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction2.GetJMCStatus
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction2::GetJMCStatus
helpviewer_keywords:
- ICorDebugFunction2::GetJMCStatus method [.NET Framework debugging]
- GetJMCStatus method [.NET Framework debugging]
ms.assetid: 840a71ed-bf5a-4f5e-8ed6-762222b34493
topic_type:
- apiref
ms.openlocfilehash: 42c72256df57b96a52737f4a0e5e90d6ba5d4e0c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692285"
---
# <a name="icordebugfunction2getjmcstatus-method"></a>ICorDebugFunction2::GetJMCStatus 方法

获取一个值，该值指示此 ICorDebugFunction2 对象表示的函数是否被标记为 "用户代码"。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetJMCStatus (  
    [out] BOOL   *pbIsJustMyCode  
);  
```  
  
## <a name="parameters"></a>参数  

 `pbIsJustMyCode`  
 弄 `true`如果此函数标记为用户代码，则为指向布尔值的指针; 否则，该值为 `false` 。  
  
## <a name="remarks"></a>备注  

 如果此表示的函数 `ICorDebugFunction2` 无法调试， `pbIsJustMyCode` 将始终为 `false` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
