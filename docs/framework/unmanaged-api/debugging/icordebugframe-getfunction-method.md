---
description: 了解详细信息： ICorDebugFrame：： GetFunction 方法
title: ICorDebugFrame::GetFunction 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetFunction
helpviewer_keywords:
- GetFunction method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetFunction method [.NET Framework debugging]
ms.assetid: 879d2311-0ff1-4616-a8b3-959ea5868b2e
topic_type:
- apiref
ms.openlocfilehash: 0309a066f686e55d086de1cbb040eea58e031df3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692974"
---
# <a name="icordebugframegetfunction-method"></a>ICorDebugFrame::GetFunction 方法

获取一个函数，该函数包含与此堆栈帧关联的代码。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetFunction (  
    [out] ICorDebugFunction  **ppFunction  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppFunction`  
 弄指向 ICorDebugFunction 对象的地址的指针，该对象表示包含与此堆栈帧关联的代码的函数。  
  
## <a name="remarks"></a>备注  

 `GetFunction`如果框架不与任何特定函数关联，则该方法可能会失败。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
