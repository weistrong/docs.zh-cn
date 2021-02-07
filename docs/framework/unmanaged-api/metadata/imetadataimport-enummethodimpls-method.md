---
description: 了解详细信息： IMetaDataImport：： EnumMethodImpls 方法
title: IMetaDataImport::EnumMethodImpls 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMethodImpls
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMethodImpls
helpviewer_keywords:
- EnumMethodImpls method [.NET Framework metadata]
- IMetaDataImport::EnumMethodImpls method [.NET Framework metadata]
ms.assetid: 4e0f865d-88b5-44bd-be35-492622e5e08e
topic_type:
- apiref
ms.openlocfilehash: 3ae5795bdde36ad07c447370553e24e1ceacf493
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670690"
---
# <a name="imetadataimportenummethodimpls-method"></a>IMetaDataImport::EnumMethodImpls 方法

枚举表示指定类型的方法的 MethodBody 和 MethodDeclaration 标记。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT EnumMethodImpls (  
   [in, out] HCORENUM    *phEnum,
   [in]      mdTypeDef   td,
   [out]     mdToken     rMethodBody[],
   [out]     mdToken     rMethodDecl[],
   [in]      ULONG       cMax,
   [in]      ULONG       *pcTokens  
);  
```  
  
## <a name="parameters"></a>参数  

 `phEnum`  
 [in，out]指向枚举器的指针。 第一次调用此方法时，此值必须为 NULL。  
  
 `td`  
 中要枚举其方法实现的类型的 TypeDef 标记。  
  
 `rMethodBody`  
 弄用于存储 MethodBody 标记的数组。  
  
 `rMethodDecl`  
 弄用于存储 MethodDeclaration 标记的数组。  
  
 `cMax`  
 中和数组的最大 `rMethodBody` 大小 `rMethodDecl` 。  
  
 `pcTokens`  
 中和中返回的实际方法数 `rMethodBody` `rMethodDecl` 。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|`S_OK`|`EnumMethodImpls` 已成功返回。|  
|`S_FALSE`|没有要枚举的方法标记。 在这种情况下， `pcTokens` 为零。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataImport 接口](imetadataimport-interface.md)
- [IMetaDataImport2 接口](imetadataimport2-interface.md)
