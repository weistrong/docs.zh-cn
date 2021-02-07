---
description: 了解详细信息： IAssemblyName：： GetProperty 方法
title: IAssemblyName::GetProperty 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetProperty
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetProperty
helpviewer_keywords:
- IAssemblyName::GetProperty method [.NET Framework fusion]
- GetProperty method [.NET Framework fusion]
ms.assetid: e59fda62-77d5-4e37-89cb-ce7ae4627975
topic_type:
- apiref
ms.openlocfilehash: 66528bb54e1cb4adbba8fa87088065bc40c2ee15
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760727"
---
# <a name="iassemblynamegetproperty-method"></a>IAssemblyName::GetProperty 方法

获取一个指针，该指针指向由指定的属性标识符引用的属性。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetProperty (  
    [in]      DWORD    PropertyId,  
    [out]     LPVOID   pvProperty,  
    [in, out] LPDWORD  pcbProperty  
);  
```  
  
## <a name="parameters"></a>参数  

 `PropertyId`  
 中请求的属性的唯一标识符。  
  
 `pvProperty`  
 弄返回的属性数据。  
  
 `pcbProperty`  
 [in，out]的大小（以字节为单位） `pvProperty` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IAssemblyName 接口](iassemblyname-interface.md)
