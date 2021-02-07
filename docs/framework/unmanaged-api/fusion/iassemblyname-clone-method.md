---
description: 了解详细信息： IAssemblyName：： Clone 方法
title: IAssemblyName::Clone 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.Clone
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::Clone
helpviewer_keywords:
- Clone method, IAssemblyName interface [.NET Framework fusion]
- IAssemblyName::Clone method [.NET Framework fusion]
ms.assetid: 7b345e08-5e16-4e3d-a044-4e19d0892943
topic_type:
- apiref
ms.openlocfilehash: b1d8ba2aec73565e9f6acaa44a5ef3731baa3af9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760779"
---
# <a name="iassemblynameclone-method"></a>IAssemblyName::Clone 方法

创建此 [IAssemblyName](iassemblyname-interface.md) 对象的浅表副本。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT Clone (  
    [out] IAssemblyName **pName  
);  
```  
  
## <a name="parameters"></a>参数  

 `pName`  
 弄此对象的返回副本 `IAssemblyName` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IAssemblyName 接口](iassemblyname-interface.md)
