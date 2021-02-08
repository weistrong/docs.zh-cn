---
description: 了解详细信息： IMetaDataValidate：： ValidatorInit 方法
title: IMetaDataValidate::ValidatorInit 方法
ms.date: 03/30/2017
api_name:
- IMetaDataValidate.ValidatorInit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataValidate::ValidatorInit
helpviewer_keywords:
- IMetaDataValidate::ValidatorInit method [.NET Framework metadata]
- ValidatorInit method [.NET Framework metadata]
ms.assetid: 6bafd75a-e2d0-4aea-aed1-074374d5dff6
topic_type:
- apiref
ms.openlocfilehash: 99435eeab542e9cb3bb679ad146b546ce51c8df4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799182"
---
# <a name="imetadatavalidatevalidatorinit-method"></a>IMetaDataValidate::ValidatorInit 方法

设置一个标志，该标志指定当前元数据范围内的模块类型，并注册验证错误的指定回调方法。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT ValidatorInit (  
   [in] DWORD       dwModuleType,  
   [in] IUnknown    *pUnk  
);  
```  
  
## <a name="parameters"></a>参数  

 `dwModule`  
 中 [CorValidatorModuleType](corvalidatormoduletype-enumeration.md) 枚举的一个值，该值指定当前元数据范围内的模块的类型。  
  
 `pUnk`  
 中指向 [IUnknown](/cpp/atl/iunknown) 实例的指针，该实例用作验证错误的函数回调。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MsCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataValidate 接口](imetadatavalidate-interface.md)
