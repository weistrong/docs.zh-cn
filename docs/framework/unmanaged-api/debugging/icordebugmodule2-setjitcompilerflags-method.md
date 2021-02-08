---
description: 了解详细信息： ICorDebugModule2：： SetJITCompilerFlags 方法
title: ICorDebugModule2::SetJITCompilerFlags 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule2.SetJITCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2::SetJITCompilerFlags
helpviewer_keywords:
- ICorDebugModule2::SetJITCompilerFlags method [.NET Framework debugging]
- SetJITCompilerFlags method [.NET Framework debugging]
ms.assetid: ea574c84-c622-4589-9a14-b55771af5e06
topic_type:
- apiref
ms.openlocfilehash: 72139c2fefc0eab7e76e38d07558e4386b47bc34
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801054"
---
# <a name="icordebugmodule2setjitcompilerflags-method"></a>ICorDebugModule2::SetJITCompilerFlags 方法

设置用于控制此 ICorDebugModule2 的实时 (JIT) 编译的标志。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT SetJITCompilerFlags (  
    [in] DWORD dwFlags  
);  
```  
  
## <a name="parameters"></a>参数  

 `dwFlags`  
 中 [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) 枚举值的按位组合。  
  
## <a name="remarks"></a>备注  

 如果 `dwFlags` 值无效，则该 `SetJITCompilerFlags` 方法将失败。  
  
 只能在 `SetJITCompilerFlags` 此模块的 [ICorDebugManagedCallback：： LoadModule](icordebugmanagedcallback-loadmodule-method.md) 回调中调用方法。 在提供回调后，尝试调用它 `ICorDebugManagedCallback::LoadModule` 将会失败。  
  
 64位或 Win9x 平台不支持 "编辑并继续"。 因此，如果在这 `SetJITCompilerFlags` 两个平台中的任何一个上调用方法，并且在中设置了 CORDEBUG_JIT_ENABLE_ENC 标志 `dwFlags` ，则 `SetJITCompilerFlags` 特定于 "编辑并继续" 的方法和所有方法（例如 [ICorDebugModule2：： ApplyChanges](icordebugmodule2-applychanges-method.md)）将会失败。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
