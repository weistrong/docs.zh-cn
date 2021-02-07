---
description: 了解详细信息： CreateAssemblyNameObject 函数
title: CreateAssemblyNameObject 函数
ms.date: 03/30/2017
api_name:
- CreateAssemblyNameObject
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateAssemblyNameObject
helpviewer_keywords:
- CreateAssemblyNameObject function [.NET Framework fusion]
ms.assetid: 55c8b41e-fbe4-4ae0-aa29-68fbb2311691
topic_type:
- apiref
ms.openlocfilehash: 0eaa74bdb37a098ad58b81658229f8c04259b730
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761169"
---
# <a name="createassemblynameobject-function"></a>CreateAssemblyNameObject 函数

获取一个接口指针，该指针指向表示具有指定名称的程序集的唯一标识的 [IAssemblyName](iassemblyname-interface.md) 实例。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateAssemblyNameObject (  
    [out] LPASSEMBLYNAME  *ppAssemblyNameObj,  
    [in]  LPCWSTR         szAssemblyName,  
    [in]  DWORD           dwFlags,  
    [in]  LPVOID          pvReserved  
 );  
```  
  
## <a name="parameters"></a>参数  

 `ppAssemblyNameObj`  
 弄返回的 `IAssemblyName` 。  
  
 `szAssemblyName`  
 中要为其创建新实例的程序集的名称 `IAssemblyName` 。  
  
 `dwFlags`  
 中要传递给对象构造函数的标志。  
  
 `pvReserved`  
 中保留以供将来进行扩展。 `pvReserved` 必须为空引用。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IAssemblyName 接口](iassemblyname-interface.md)
- [合成全局静态函数](fusion-global-static-functions.md)
