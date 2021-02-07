---
description: 了解详细信息： IMetaDataAssemblyImport：： EnumExportedTypes 方法
title: IMetaDataAssemblyImport::EnumExportedTypes 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.EnumExportedTypes
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::EnumExportedTypes
helpviewer_keywords:
- EnumExportedTypes method [.NET Framework metadata]
- IMetaDataAssemblyImport::EnumExportedTypes method [.NET Framework metadata]
ms.assetid: e5912ed8-e4ce-438b-8ea3-d9e4c288d109
topic_type:
- apiref
ms.openlocfilehash: ecddcbd87586f5f61c57f8c04ea3bd68dc652839
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678024"
---
# <a name="imetadataassemblyimportenumexportedtypes-method"></a>IMetaDataAssemblyImport::EnumExportedTypes 方法

枚举当前元数据范围内的程序集清单中引用的导出类型。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT EnumExportedTypes (  
    [in, out] HCORENUM     *phEnum,
    [out] mdExportedType   rExportedTypes[],
    [in]  ULONG            cMax,
    [out] ULONG            *pcTokens  
);  
```  
  
## <a name="parameters"></a>参数  

 `phEnum`  
 [in，out]指向枚举器的指针。 第一次调用方法时，此值必须为 null 值 `EnumExportedTypes` 。  
  
 `rExportedTypes`  
 弄 `mdExportedType` 元数据标记的枚举。  
  
 `cMax`  
 中 `mdExportedType` 可置于数组中的最大标记数 `rExportedTypes` 。  
  
 `pcTokens`  
 弄 `mdExportedType` 实际置于中的标记数 `rExportedTypes` 。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|`S_OK`|`EnumExportedTypes` 已成功返回。|  
|`S_FALSE`|没有要枚举的令牌。 在这种情况下， `pcTokens` 设置为零。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MsCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataAssemblyImport 接口](imetadataassemblyimport-interface.md)
