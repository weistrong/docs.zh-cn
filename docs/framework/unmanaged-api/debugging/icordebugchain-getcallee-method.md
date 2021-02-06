---
description: 了解详细信息： ICorDebugChain：： GetCallee 方法
title: ICorDebugChain::GetCallee 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetCallee
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetCallee method
helpviewer_keywords:
- ICorDebugChain::GetCallee method [.NET Framework debugging]
- GetCallee method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 19560c79-abdc-4bdf-a5fe-eb362a59edc0
topic_type:
- apiref
ms.openlocfilehash: 4787893c86804c648dae14bf2e6f7425808104b7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661384"
---
# <a name="icordebugchaingetcallee-method"></a>ICorDebugChain::GetCallee 方法

获取此链调用的链。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetCallee (  
    [out] ICorDebugChain     **ppChain  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppChain`  
 弄指向 ICorDebugChain 对象的地址的指针，该对象表示调用的链。 如果此链当前正在执行 (即，如果此链未等待调用的链返回) ， `ppChain` 则将为 null。  
  
## <a name="remarks"></a>备注  

 此链将等待调用的链返回，然后再继续执行。 对于跨线程封送调用，被调用的链可以在另一个线程上。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
