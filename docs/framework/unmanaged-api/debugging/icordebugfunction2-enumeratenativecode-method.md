---
description: 了解详细信息： ICorDebugFunction2：： EnumerateNativeCode 方法
title: ICorDebugFunction2::EnumerateNativeCode 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction2.EnumerateNativeCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction2::EnumerateNativeCode
helpviewer_keywords:
- ICorDebugFunction2::EnumerateNativeCode method [.NET Framework debugging]
- EnumerateNativeCode method [.NET Framework debugging]
ms.assetid: d383f5cc-1144-4b6d-b57a-db34d9134ab2
topic_type:
- apiref
ms.openlocfilehash: 617d6dbfdb596df192e2722a47d81517ae57ac1f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692246"
---
# <a name="icordebugfunction2enumeratenativecode-method"></a>ICorDebugFunction2::EnumerateNativeCode 方法

获取一个指向 ICorDebugCodeEnum 对象的接口指针，该对象包含此 ICorDebugFunction2 对象引用的函数中的本机代码语句。  
  
> [!NOTE]
> `EnumerateNativeCode` 在 .NET Framework 的当前版本中未实现。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT EnumerateNativeCode (  
    [out] ICorDebugCodeEnum   **ppCodeEnum  
);  
```  
  
## <a name="requirements"></a>要求  

 **标头**：CorDebug.idl、CorDebug.h
