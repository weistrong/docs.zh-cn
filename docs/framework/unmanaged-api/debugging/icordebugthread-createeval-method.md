---
description: 了解详细信息： ICorDebugThread：： CreateEval 方法
title: ICorDebugThread::CreateEval 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.CreateEval
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::CreateEval
helpviewer_keywords:
- CreateEval method [.NET Framework debugging]
- ICorDebugThread::CreateEval method [.NET Framework debugging]
ms.assetid: 36605067-33d3-4579-9c72-fb0e551ab0f1
topic_type:
- apiref
ms.openlocfilehash: a789840e099a14b584e5713bee12f5c4b0717fe7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659382"
---
# <a name="icordebugthreadcreateeval-method"></a>ICorDebugThread::CreateEval 方法

创建一个 ICorDebugEval 对象，该对象收集并公开此 ICorDebugThread 的功能。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateEval (  
    [out] ICorDebugEval   **ppEval  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppEval`  
 弄指向 `ICorDebugEval` 收集并公开此线程功能的对象地址的指针。  
  
## <a name="remarks"></a>备注  

 计算对象在计算之前会在线程上推送新的链。 这会中断当前正在线程上执行的计算，直到完成计算。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
