---
description: 了解详细信息： ICorDebugFrame：： GetStackRange 方法
title: ICorDebugFrame::GetStackRange 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetStackRange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetStackRange
helpviewer_keywords:
- GetStackRange method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetStackRange method [.NET Framework debugging]
ms.assetid: fab037cb-fda6-40fb-9367-921e435dd5a0
topic_type:
- apiref
ms.openlocfilehash: 1f1278e0c00addc3c14f4e1c8d3ed5aad0381526
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692896"
---
# <a name="icordebugframegetstackrange-method"></a>ICorDebugFrame::GetStackRange 方法

获取此堆栈帧的绝对地址范围。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetStackRange (  
    [out] CORDB_ADDRESS      *pStart,
    [out] CORDB_ADDRESS      *pEnd  
);  
```  
  
## <a name="parameters"></a>参数  

 `pStart`  
 弄指向的指针 `CORDB_ADDRESS` ，它指定此对象表示的堆栈帧的起始地址 `ICorDebugFrame` 。  
  
 `pEnd`  
 弄指向的指针 `CORDB_ADDRESS` ，它指定此对象表示的堆栈帧的结束地址 `ICorDebugFrame` 。  
  
## <a name="remarks"></a>备注  

 堆栈的地址范围可用于拼凑将从多个调试引擎中收集的交错堆栈跟踪组合在一起。 数值范围不提供有关堆栈帧内容的信息。 它仅用于比较堆栈帧位置。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
