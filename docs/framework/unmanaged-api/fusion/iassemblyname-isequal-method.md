---
description: 了解详细信息： IAssemblyName：： IsEqual 方法
title: IAssemblyName::IsEqual 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.IsEqual
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::IsEqual
helpviewer_keywords:
- IsEqual method [.NET Framework fusion]
- IAssemblyName::IsEqual method [.NET Framework fusion]
ms.assetid: 6dfc220f-d0d4-45b3-bfce-5829f817766f
topic_type:
- apiref
ms.openlocfilehash: f1bb0e26a217354e904ff79b397771d727a7a661
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760677"
---
# <a name="iassemblynameisequal-method"></a>IAssemblyName::IsEqual 方法

根据指定的比较标志，确定指定的 [IAssemblyName](iassemblyname-interface.md) 对象是否等于此 `IAssemblyName` 。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT IsEqual (  
    [in] IAssemblyName  *pName,  
    [in] DWORD          dwCmpFlags  
);  
```  
  
## <a name="parameters"></a>参数  

 `pName`  
 中要与 `IAssemblyName` 此进行比较的对象 `IAssemblyName` 。  
  
 `dwCmpFlags`  
 中影响比较的 [ASM_CMP_FLAGS](asm-cmp-flags-enumeration.md) 值的按位组合。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IAssemblyName 接口](iassemblyname-interface.md)
- [合成枚举](fusion-enumerations.md)
