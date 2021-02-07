---
description: 了解详细信息： ICorDebugDataTarget：： GetThreadContext 方法
title: ICorDebugDataTarget::GetThreadContext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugDataTarget.GetThreadContext Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugDataTarget::GetThreadContext
helpviewer_keywords:
- ICorDebugDataTarget::GetThreadContext method [.NET Framework debugging]
- GetThreadContext method, ICorDebugDataTarget interface [.NET Framework debugging]
ms.assetid: c8954268-1821-4b23-b665-dbb55f2af31b
topic_type:
- apiref
ms.openlocfilehash: cf40579aa0a495af4e5e775334d177ca6f3da86f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710629"
---
# <a name="icordebugdatatargetgetthreadcontext-method"></a>ICorDebugDataTarget::GetThreadContext 方法

返回指定线程的当前线程上下文。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetThreadContext(  
       [in] DWORD dwThreadID,  
       [in] ULONG32 contextFlags,  
       [in] ULONG32 contextSize,  
       [out, size_is(contextSize)] BYTE * pContext);  
```  
  
## <a name="parameters"></a>参数  

 `dwThreadID`  
 中要检索其上下文的线程的标识符。 标识符由操作系统定义。  
  
 `contextFlags`  
 中平台相关标志的按位组合，用于指示应读取上下文的哪些部分。  
  
 `contextSize`  
 [输入] `pContext` 的大小。  
  
 `pContext`  
 弄将存储线程上下文的缓冲区。  
  
## <a name="remarks"></a>备注  

 在 Windows 平台上， `pContext` 必须是 `CONTEXT`) 在 [ICorDebugDataTarget：： GetPlatform](icordebugdatatarget-getplatform-method.md) 方法指定的计算机类型中定义的结构 (。 `contextFlags` 必须与结构的字段具有相同的值 `ContextFlags` `CONTEXT` 。 `CONTEXT`结构特定于处理器; 有关详细信息，请参阅 WinNT .h 文件。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorDebugDataTarget 接口](icordebugdatatarget-interface.md)
- [调试接口](debugging-interfaces.md)
- [调试](index.md)
