---
description: 了解详细信息： ICorDebugStackWalk：： SetContext 方法
title: ICorDebugStackWalk::SetContext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk.SetContext Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk::SetContext
helpviewer_keywords:
- SetContext method [.NET Framework debugging]
- ICorDebugStackWalk::SetContext method [.NET Framework debugging]
ms.assetid: bac0b156-31a3-4e7f-be4d-ab21789c81f1
topic_type:
- apiref
ms.openlocfilehash: 20e18460d237a63e4c2695b9e7cbfa766ed3908f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794710"
---
# <a name="icordebugstackwalksetcontext-method"></a>ICorDebugStackWalk::SetContext 方法

将 [ICorDebugStackWalk](icordebugstackwalk-interface.md) 对象的当前上下文设置为线程的有效上下文。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT SetContext([in] CorDebugSetContextFlag flag,  
                   [in] ULONG32 contextSize,  
                   [in, size_is(contextSize)] BYTE context[]);  
```  
  
## <a name="parameters"></a>参数  

 `flag`  
 中 [CorDebugSetContextFlag](cordebugsetcontextflag-enumeration.md) 标志，用于指示上下文是否来自堆栈上的活动帧，或通过展开堆栈获取的上下文。  
  
 `contextSize`  
 中缓冲区的已分配大小 `CONTEXT` 。  
  
 `context`  
 中 `CONTEXT` 缓冲区。  
  
## <a name="return-value"></a>返回值  

 此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。  
  
|HRESULT|说明|  
|-------------|-----------------|  
|S_OK|`ICorDebugStackWalk`已成功设置对象的上下文。|  
|E_FAIL|`ICorDebugStackWalk`未设置对象的上下文。|  
|E_INVALIDARG|上下文为 null。|  
|HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)|上下文缓冲区太小。|  
  
## <a name="exceptions"></a>例外  
  
## <a name="remarks"></a>备注  

 此方法不会更改线程的当前上下文。  
  
 将当前上下文设置为无效上下文可能会导致堆栈查看程序产生不可预知的结果。  
  
 可以通过立即调用 [ICorDebugStackWalk：： GetContext](icordebugstackwalk-getcontext-method.md) 方法来检索此上下文的精确按位副本。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](debugging-interfaces.md)
- [调试](index.md)
