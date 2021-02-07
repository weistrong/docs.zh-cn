---
description: 了解详细信息： ICorDebugStepper：： SetRangeIL 方法
title: ICorDebugStepper::SetRangeIL 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.SetRangeIL
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::SetRangeIL
helpviewer_keywords:
- SetRangeIL method [.NET Framework debugging]
- ICorDebugStepper::SetRangeIL method [.NET Framework debugging]
ms.assetid: a20c95f0-6da7-4b41-b27f-584211cebb92
topic_type:
- apiref
ms.openlocfilehash: 8bccaf8ba8e52a7fe94555fa99b1c3cf92842efe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717676"
---
# <a name="icordebugsteppersetrangeil-method"></a>ICorDebugStepper::SetRangeIL 方法

设置一个值，该值指定对 [ICorDebugStepper：： StepRange](icordebugstepper-steprange-method.md) 的调用是传递与本机代码相关的参数值，还是相对于 Microsoft 中间)  (语言传递参数值。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT SetRangeIL (  
    [in] BOOL    bIL  
);  
```  
  
## <a name="parameters"></a>参数  

 `bIL`  
 中如果设置为， `true` 则指定范围是相对于 MSIL 代码的。 设置为， `false` 以指定范围相对于本机代码。 默认值是 `true`。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
