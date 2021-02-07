---
description: 了解详细信息： ICorDebugCode：： CreateBreakpoint 方法
title: ICorDebugCode::CreateBreakpoint 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.CreateBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::CreateBreakpoint
helpviewer_keywords:
- ICorDebugCode::CreateBreakpoint method [.NET Framework debugging]
- CreateBreakpoint method, ICorDebugCode interface [.NET Framework debugging]
ms.assetid: 46842618-0fe4-480b-871c-82fba82d23d9
topic_type:
- apiref
ms.openlocfilehash: a9285d59da3e3f34ea303413fca67bc39aff9e32
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711370"
---
# <a name="icordebugcodecreatebreakpoint-method"></a>ICorDebugCode::CreateBreakpoint 方法

在此代码段中的指定偏移量处创建断点。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateBreakpoint (  
    [in] ULONG32     offset,  
    [out] ICorDebugFunctionBreakpoint **ppBreakpoint  
);  
```  
  
## <a name="parameters"></a>参数  

 `offset`  
 中创建断点的偏移量。  
  
 `ppBreakpoint`  
 弄指向表示断点的 "ICorDebugFunctionBreakpoint" 对象地址的指针。  
  
## <a name="remarks"></a>备注  

 在断点处于活动状态之前，必须将其添加到进程对象。  
  
 如果此代码为 Microsoft 中间语言 (MSIL) 代码，并且存在 (JIT) 编译的本机版本代码，则将在 JIT 编译的代码中应用该断点。 如果稍后对代码进行 JIT 编译，则 (相同。 )   
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
