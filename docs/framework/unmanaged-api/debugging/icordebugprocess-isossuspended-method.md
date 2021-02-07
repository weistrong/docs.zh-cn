---
description: 了解详细信息： ICorDebugProcess：： IsOSSuspended 方法
title: ICorDebugProcess::IsOSSuspended 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.IsOSSuspended
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::IsOSSuspended
helpviewer_keywords:
- IsOSSuspended method [.NET Framework debugging]
- ICorDebugProcess::IsOSSuspended method [.NET Framework debugging]
ms.assetid: 83406cb2-5797-4402-872d-89c9516aefec
topic_type:
- apiref
ms.openlocfilehash: aa5e438418330d9fee51fcdb56a617421df06904
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746732"
---
# <a name="icordebugprocessisossuspended-method"></a>ICorDebugProcess::IsOSSuspended 方法

获取一个值，该值指示是否由于调试器停止此进程而挂起了指定线程。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT IsOSSuspended(  
    [in]  DWORD threadID,  
    [out] BOOL  *pbSuspended);  
```  
  
## <a name="parameters"></a>参数  

 `threadID`  
 中相关线程的 ID。  
  
 `pbSuspended`  
 弄指向布尔值的指针， `true` 如果指定线程已挂起，则为; 否则 `pbSuspended` 为 `false` 。  
  
## <a name="remarks"></a>备注  

 当由于调试器停止此进程而暂停指定的线程时，指定线程的 Win32 挂起计数将递增1。 如果调试器用户界面向用户显示操作系统 (OS) 挂起线程计数，则 (UI) 可能需要考虑此信息。  
  
 此 `IsOSSuspended` 方法仅在非托管调试的上下文中有意义。 在托管调试期间，线程会以协作方式暂停，而不是由 OS 挂起。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
