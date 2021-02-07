---
description: 了解详细信息： IAssemblyName：： GetName 方法
title: IAssemblyName::GetName 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetName
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetName
helpviewer_keywords:
- GetName method, IAssemblyName interface [.NET Framework debugging]
- IAssemblyName::GetName method [.NET Framework fusion]
ms.assetid: 1dee9781-1cf3-48a9-a376-d18ea1f73280
topic_type:
- apiref
ms.openlocfilehash: 04cd6258c2fc60c9fc40e1e4b731e5c04a8d3112
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760740"
---
# <a name="iassemblynamegetname-method"></a>IAssemblyName::GetName 方法

获取此 [IAssemblyName](iassemblyname-interface.md) 对象所引用的程序集的简单、未加密名称。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetName (  
    [in, out] LPDWORD lpcwBuffer,  
    [out]     WCHAR *pwzName  
);  
```  
  
## <a name="parameters"></a>参数  

 `lpcwBuffer`  
 [in，out] `pwzName` 宽字符的大小，包括 null 终止符。  
  
 `pwzName`  
 弄用于保存所引用程序集的名称的缓冲区。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IAssemblyName 接口](iassemblyname-interface.md)
