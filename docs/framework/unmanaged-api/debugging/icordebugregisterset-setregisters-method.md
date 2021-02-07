---
description: 了解详细信息： ICorDebugRegisterSet：： SetRegisters 方法
title: ICorDebugRegisterSet::SetRegisters 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.SetRegisters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::SetRegisters
helpviewer_keywords:
- SetRegisters method, ICorDebugRegisterSet interface [.NET Framework debugging]
- ICorDebugRegisterSet::SetRegisters method [.NET Framework debugging]
ms.assetid: ac6244b9-54ba-475f-b72a-abed6afc46ec
topic_type:
- apiref
ms.openlocfilehash: 7a83d9d01a392d7ed435292f45ee0c75765ced36
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690673"
---
# <a name="icordebugregistersetsetregisters-method"></a>ICorDebugRegisterSet::SetRegisters 方法

`SetRegisters` 在 .NET Framework 版本2.0 中未实现。 请勿调用此方法。  
  
> [!NOTE]
> 使用较高级别的操作，如 [ICorDebugILFrame：： setip](icordebugilframe-setip-method.md) 或 [ICorDebugNativeFrame：： setip](icordebugnativeframe-setip-method.md)。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT SetRegisters (  
    [in] ULONG64   mask,  
    [in] ULONG32   regCount,  
    [in, size_is(regCount)] CORDB_REGISTER regBuffer[]  
);  
```  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：** 1.1、1。0  
  
## <a name="see-also"></a>请参阅

- [ICorDebugRegisterSet 接口](icordebugregisterset-interface.md)
- [ICorDebugRegisterSet2 接口](icordebugregisterset2-interface.md)
