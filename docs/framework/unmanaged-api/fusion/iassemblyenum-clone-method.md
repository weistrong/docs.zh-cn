---
description: 了解详细信息： IAssemblyEnum：： Clone 方法
title: IAssemblyEnum::Clone 方法
ms.date: 03/30/2017
api_name:
- IAssemblyEnum.Clone
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyEnum::Clone
helpviewer_keywords:
- Clone method, IAssemblyEnum interface [.NET Framework fusion]
- IAssemblyEnum::Clone method [.NET Framework fusion]
ms.assetid: 0014bb66-590c-486c-9ade-f2133905cd99
topic_type:
- apiref
ms.openlocfilehash: 0b4da5818b66d5b82da0b693c2d1cfa257f08a7f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760831"
---
# <a name="iassemblyenumclone-method"></a>IAssemblyEnum::Clone 方法

创建此 [IAssemblyEnum](iassemblyenum-interface.md) 对象的浅表副本。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT Clone (  
    [out] IAssemblyEnum   **ppEnum  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppEnum`  
 弄指向复制的指针。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IAssemblyEnum 接口](iassemblyenum-interface.md)
