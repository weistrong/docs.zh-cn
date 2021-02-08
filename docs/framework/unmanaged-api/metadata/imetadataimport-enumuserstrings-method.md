---
description: 了解详细信息： IMetaDataImport：： EnumUserStrings 方法
title: IMetaDataImport::EnumUserStrings 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumUserStrings
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumUserStrings
helpviewer_keywords:
- IMetaDataImport::EnumUserStrings method [.NET Framework metadata]
- EnumUserStrings method [.NET Framework metadata]
ms.assetid: 2b1f1418-4be8-4cdb-b418-b3abccc527a7
topic_type:
- apiref
ms.openlocfilehash: a4ead696f3d924fef9ebfed5c4f1eb97eb13e14e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799312"
---
# <a name="imetadataimportenumuserstrings-method"></a>IMetaDataImport::EnumUserStrings 方法

枚举表示当前元数据范围内的硬编码字符串的 String 标记。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT EnumUserStrings (  
   [in, out]  HCORENUM    *phEnum,  
   [out]  mdString        rStrings[],  
   [in]   ULONG           cMax,  
   [out]  ULONG           *pcStrings  
);  
```  
  
## <a name="parameters"></a>参数  

 `phEnum`  
 [in，out]指向枚举器的指针。 第一次调用此方法时，此值必须为 NULL。  
  
 `rStrings`  
 弄用于存储字符串标记的数组。  
  
 `cMax`  
 [in] `rStrings` 数组的最大大小。  
  
 `pcStrings`  
 弄中返回的字符串标记的数目 `rStrings` 。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|`S_OK`|`EnumUserStrings` 已成功返回。|  
|`S_FALSE`|没有要枚举的令牌。 在这种情况下， `pcStrings` 为零。|  
  
## <a name="remarks"></a>备注  

 字符串标记由 [IMetaDataEmit：:D efineuserstring](imetadataemit-defineuserstring-method.md) 方法创建。 此方法旨在由元数据浏览器而不是编译器使用。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataImport 接口](imetadataimport-interface.md)
- [IMetaDataImport2 接口](imetadataimport2-interface.md)
