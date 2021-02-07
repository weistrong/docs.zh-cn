---
description: 了解详细信息： ICorDebugFrame：： CreateStepper 方法
title: ICorDebugFrame::CreateStepper 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.CreateStepper
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::CreateStepper
helpviewer_keywords:
- ICorDebugFrame::CreateStepper method [.NET Framework debugging]
- CreateStepper method, ICorDebugFrame interface [.NET Framework debugging]
ms.assetid: 689e7f28-20c1-4d5c-9baa-17441cd63a88
topic_type:
- apiref
ms.openlocfilehash: 394418b89fd7a1c780a5bc33b97b8ef40bab8df2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693091"
---
# <a name="icordebugframecreatestepper-method"></a>ICorDebugFrame::CreateStepper 方法

获取一个分档器，该分档器允许调试器执行相对于此 ICorDebugFrame 的单步执行操作。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateStepper (  
    [out] ICorDebugStepper   **ppStepper  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppStepper`  
 弄指向 ICorDebugStepper 对象地址的指针，该对象允许调试器相对于当前帧执行单步操作。  
  
## <a name="remarks"></a>备注  

 如果帧不处于活动状态，则在步骤完成之前，分档器对象通常需要返回到帧。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
