---
description: 了解详细信息： CLRDataCreateInstance 函数
title: CLRDataCreateInstance 函数
ms.date: 03/30/2017
api_name:
- CLRDataCreateInstance
api_location:
- mscordbi.dll
- mscordacwks.dll
api_type:
- DLLExport
f1_keywords:
- CLRDataCreateInstance
helpviewer_keywords:
- CLRDataCreateInstance function [.NET Framework debugging]
ms.assetid: 440bad90-5a88-45e7-9157-4596801d8d19
topic_type:
- apiref
ms.openlocfilehash: 923b0c687d2b337eacb475973927452e3b47ad0d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747252"
---
# <a name="clrdatacreateinstance-function"></a>CLRDataCreateInstance 函数

为指定的目标项创建接口对象。

## <a name="syntax"></a>语法

```cpp
HRESULT CLRDataCreateInstance (
    [in]  REFIID           iid,
    [in]  ICLRDataTarget  *target,
    [out] void           **iface  
);  
```  
  
## <a name="parameters"></a>参数  

 `iid`  
 中要实例化的接口的标识符。  
  
 `target`  
 中一个指向用户实现的 [ICLRDataTarget](iclrdatatarget-interface.md) 对象的指针，该对象表示要为其创建 interface 对象的目标项。  
  
 `iface`  
 弄指向返回的接口对象地址的指针。  
  
## <a name="remarks"></a>备注  

 `ICLRDataTarget`对象由调试应用程序的编写器实现。 实现取决于所表示的目标项的类型。 目标项可以是进程、内存转储、远程计算机，等等。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** ClrData .idl  
  
 **库：** CorGuids.lib  

 **程序集**： mscordacwks.dll、mscordbi.dll
  
 **.NET Framework 版本：** 自 .NET Framework 2.0 起可用
  
## <a name="see-also"></a>请参阅

- [调试全局静态函数](debugging-global-static-functions.md)
