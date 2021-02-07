---
description: 了解详细信息： ICorDebugAppDomain：： GetObject 方法
title: ICorDebugAppDomain::GetObject 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetObject
api_location:
- corguids.lib
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetObject
helpviewer_keywords:
- ICorDebugAppDomain::GetObject method [.NET Framework debugging]
- GetObject method, ICorDebugAppDomain interface [.NET Framework debugging]
ms.assetid: 78232e6f-ae18-4cfa-a6cd-e79471cf9d76
topic_type:
- apiref
ms.openlocfilehash: 59389e2a4ca72f8dcdd7117213e968440d30aaa6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754206"
---
# <a name="icordebugappdomaingetobject-method"></a>ICorDebugAppDomain::GetObject 方法

获取 (CLR) 应用程序域的公共语言运行时的接口指针。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetObject (  
    [out] ICorDebugValue   **ppObject  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppObject`  
 弄指向表示 CLR 应用程序域的 ICorDebugValue 接口对象地址的指针。  
  
## <a name="return-value"></a>返回值  

 如果 <xref:System.AppDomain?displayProperty=nameWithType> 尚未为此应用程序域构造托管对象，则该方法将返回 `S_FALSE` ，并将放 `NULL` 入 `*ppObject` 。  
  
## <a name="remarks"></a>备注  

 进程中的每个应用程序域在运行时中都可能有一个 <xref:System.AppDomain?displayProperty=nameWithType> 表示该对象的托管对象。 此函数获取对应于此托管对象的 ICorDebugValue 接口对象 <xref:System.AppDomain?displayProperty=nameWithType> 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]
