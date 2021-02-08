---
description: 了解详细信息： IMetaDataImport：： EnumProperties 方法
title: IMetaDataImport::EnumProperties 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumProperties
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumProperties
helpviewer_keywords:
- IMetaDataImport::EnumProperties method [.NET Framework metadata]
- EnumProperties method [.NET Framework metadata]
ms.assetid: 60573ad7-8821-4721-a068-3f7a6d25926a
topic_type:
- apiref
ms.openlocfilehash: 7503dd14668e8ea4ccf8939e67b91a41db187105
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799351"
---
# <a name="imetadataimportenumproperties-method"></a>IMetaDataImport::EnumProperties 方法

枚举 PropertyDef 标记，这些标记表示指定的 TypeDef 标记所引用的类型的属性。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT EnumProperties (  
   [in, out] HCORENUM    *phEnum,  
   [in]      mdTypeDef   td,  
   [out]     mdProperty  rProperties[],  
   [in]      ULONG       cMax,  
   [out]     ULONG       *pcProperties  
);  
```  
  
## <a name="parameters"></a>参数  

 `phEnum`  
 [in，out]指向枚举器的指针。 第一次调用此方法时，此值必须为 NULL。  
  
 `td`  
 中一个 TypeDef 标记，它表示具有要枚举的属性的类型。  
  
 `rProperties`  
 弄用于存储 PropertyDef 标记的数组。  
  
 `cMax`  
 [in] `rProperties` 数组的最大大小。  
  
 `pcProperties`  
 弄中返回的 PropertyDef 令牌数 `rProperties` 。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|`S_OK`|`EnumProperties` 已成功返回。|  
|`S_FALSE`|没有要枚举的令牌。 在这种情况下， `pcProperties` 为零。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataImport 接口](imetadataimport-interface.md)
- [IMetaDataImport2 接口](imetadataimport2-interface.md)
