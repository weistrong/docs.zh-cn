---
description: 了解详细信息： IMetaDataImport：： EnumEvents 方法
title: IMetaDataImport::EnumEvents 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumEvents
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumEvents
helpviewer_keywords:
- IMetaDataImport::EnumEvents method [.NET Framework metadata]
- EnumEvents method [.NET Framework metadata]
ms.assetid: e1efedcb-3dd7-42ae-a399-21c24728aec5
topic_type:
- apiref
ms.openlocfilehash: e944c15a19314b315e01493836ce078fccc917eb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799390"
---
# <a name="imetadataimportenumevents-method"></a>IMetaDataImport::EnumEvents 方法

枚举指定的 TypeDef 标记的事件定义标记。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT EnumEvents (
   [in, out] HCORENUM    *phEnum,
   [in]      mdTypeDef   td,
   [out]     mdEvent     rEvents[],
   [in]      ULONG       cMax,  
   [out]    ULONG        *pcEvents  
);  
```  
  
## <a name="parameters"></a>参数  

 `phEnum`  
 [in，out]指向枚举器的指针。  
  
 `td`  
 中要枚举其事件定义的 TypeDef 标记。  
  
 `rEvents`  
 弄返回的事件的数组。  
  
 `cMax`  
 [in] `rEvents` 数组的最大大小。  
  
 `pcEvents`  
 弄中返回的实际事件数 `rEvents` 。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|`S_OK`|`EnumEvents` 已成功返回。|  
|`S_FALSE`|没有要枚举的事件。 在这种情况下， `pcEvents` 为零。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataImport 接口](imetadataimport-interface.md)
- [IMetaDataImport2 接口](imetadataimport2-interface.md)
