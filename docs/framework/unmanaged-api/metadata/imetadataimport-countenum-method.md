---
description: 了解详细信息： IMetaDataImport：： CountEnum 方法
title: IMetaDataImport::CountEnum 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.CountEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::CountEnum
helpviewer_keywords:
- CountEnum method [.NET Framework metadata]
- IMetaDataImport::CountEnum method [.NET Framework metadata]
ms.assetid: d1de53ad-9435-4b5f-9df7-07f21210e5b5
topic_type:
- apiref
ms.openlocfilehash: c579ef7ce440e3552ab28572fc6c96ad12d66400
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677686"
---
# <a name="imetadataimportcountenum-method"></a>IMetaDataImport::CountEnum 方法

获取由指定枚举器检索的枚举中的元素数目。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CountEnum (  
   [in]  HCORENUM    hEnum,
   [out] ULONG       *pulCount  
);  
```  
  
## <a name="parameters"></a>参数  

 `hEnum`  
 中枚举器的句柄。  
  
 `pulCount`  
 弄枚举的元素的数目。  
  
## <a name="remarks"></a>备注  

 指定的句柄 `hEnum` 是从以前的 `Enum` *名称* 调用获取的 (例如， [IMetaDataImport：： EnumTypeDefs](imetadataimport-enumtypedefs-method.md)) 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataImport 接口](imetadataimport-interface.md)
- [IMetaDataImport2 接口](imetadataimport2-interface.md)
