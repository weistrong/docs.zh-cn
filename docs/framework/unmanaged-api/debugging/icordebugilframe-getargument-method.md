---
description: 了解详细信息： ICorDebugILFrame：： GetArgument 方法
title: ICorDebugILFrame::GetArgument 方法
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.GetArgument
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::GetArgument
helpviewer_keywords:
- GetArgument method [.NET Framework debugging]
- ICorDebugILFrame::GetArgument method [.NET Framework debugging]
ms.assetid: 4e2fd423-f643-4c27-ba5f-41b5ebc3b416
topic_type:
- apiref
ms.openlocfilehash: c845f3c07502f3b1ce564833ee6ef98e3305463f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650503"
---
# <a name="icordebugilframegetargument-method"></a>ICorDebugILFrame::GetArgument 方法

获取此 Microsoft 中间语言 (MSIL) 堆栈帧中的指定参数的值。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetArgument (  
    [in] DWORD                  dwIndex,  
    [out] ICorDebugValue        **ppValue  
);  
```  
  
## <a name="parameters"></a>参数  

 `dwIndex`  
 中此 MSIL 堆栈帧中的参数的索引。  
  
 `ppValue`  
 [out] 一个指向 ICorDebugValue 对象地址的指针，该对象表示检索到的值。  
  
## <a name="remarks"></a>备注  

 `GetArgument`方法既可以在 MSIL 堆栈帧中使用，也可以在实时 (JIT) 编译的框架中使用。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
