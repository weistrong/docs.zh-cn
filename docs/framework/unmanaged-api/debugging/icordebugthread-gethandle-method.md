---
description: 了解详细信息： ICorDebugThread：： GetHandle 方法
title: ICorDebugThread::GetHandle 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetHandle
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetHandle
helpviewer_keywords:
- GetHandle method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetHandle method [.NET Framework debugging]
ms.assetid: 172ef8c4-2ead-4cfc-bd2e-dee4fb7191cd
topic_type:
- apiref
ms.openlocfilehash: 378bb395e56f0fc287a480d67d2047e082d0796f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659096"
---
# <a name="icordebugthreadgethandle-method"></a>ICorDebugThread::GetHandle 方法

获取此 ICorDebugThread 的活动部分的当前句柄。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetHandle (  
    [out] HTHREAD *phThreadHandle  
);  
```  
  
## <a name="parameters"></a>参数  

 `phThreadHandle`  
 弄指向 HTHREAD 的指针，该指针是此线程的活动部分的句柄。  
  
## <a name="remarks"></a>备注  

 该句柄可能在进程执行时发生更改，并且可能不同于线程的不同部分。  
  
 此句柄属于调试 API。 调试器应在使用之前进行复制。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
