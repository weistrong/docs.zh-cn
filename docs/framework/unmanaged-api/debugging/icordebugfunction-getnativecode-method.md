---
description: 了解详细信息： ICorDebugFunction：： GetNativeCode 方法
title: ICorDebugFunction::GetNativeCode 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetNativeCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetNativeCode
helpviewer_keywords:
- GetNativeCode method [.NET Framework debugging]
- ICorDebugFunction::GetNativeCode method [.NET Framework debugging]
ms.assetid: c8a34916-0eef-4987-8d29-c8bcb4be9cf6
topic_type:
- apiref
ms.openlocfilehash: 8938e11a5fdc3aa693faf04eec639941475d95ac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692441"
---
# <a name="icordebugfunctiongetnativecode-method"></a>ICorDebugFunction::GetNativeCode 方法

获取此 ICorDebugFunction 实例所表示的函数的本机代码。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetNativeCode (  
    [out] ICorDebugCode **ppCode  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppCode`  
 弄一个指针，指向表示此函数的本机代码的 ICorDebugCode 实例，如果此函数为 Microsoft 中间语言，则为 null; 如果此函数为 Microsoft 中间 (语言，则为) 代码，该代码不是实时 (JIT) 编译的。  
  
## <a name="remarks"></a>备注  

 如果此实例表示的函数已多次 `ICorDebugFunction` JIT 编译（如泛型类型），则 `GetNativeCode` 返回随机的本机代码对象。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
