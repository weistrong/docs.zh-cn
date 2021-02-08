---
description: 了解详细信息： IMetaDataImport：： EnumUnresolvedMethods 方法
title: IMetaDataImport::EnumUnresolvedMethods 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumUnresolvedMethods
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumUnresolvedMethods
helpviewer_keywords:
- EnumUnresolvedMethods method [.NET Framework metadata]
- IMetaDataImport::EnumUnresolvedMethods method [.NET Framework metadata]
ms.assetid: eb3187d7-74cf-44b1-aeeb-7a8d2b60e3b7
topic_type:
- apiref
ms.openlocfilehash: e894ecdde91a2263783234d73fa50d890a13e413
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799325"
---
# <a name="imetadataimportenumunresolvedmethods-method"></a>IMetaDataImport::EnumUnresolvedMethods 方法

枚举表示当前元数据范围内未解析的方法的 MemberDef 标记。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT EnumUnresolvedMethods (  
   [in, out] HCORENUM    *phEnum,  
   [out]     mdToken     rMethods[],  
   [in]      ULONG       cMax,  
   [out]     ULONG       *pcTokens  
);  
```  
  
## <a name="parameters"></a>参数  

 `phEnum`  
 [in，out]指向枚举器的指针。 第一次调用此方法时，此值必须为 NULL。  
  
 `rMethods`  
 弄用于存储 MemberDef 标记的数组。  
  
 `cMax`  
 [in] `rMethods` 数组的最大大小。  
  
 `pcTokens`  
 弄中返回的 MemberDef 令牌数 `rMethods` 。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|`S_OK`|`EnumUnresolvedMethods` 已成功返回。|  
|`S_FALSE`|没有要枚举的令牌。 在这种情况下， `pcTokens` 为零。|  
  
## <a name="remarks"></a>备注  

 未解析的方法是已声明但未实现的方法。 如果方法已标记 `miForwardRef` 并且 `mdPinvokeImpl` 或 `miRuntime` 设置为零，则枚举中将包含方法。 换句话说，未解析的方法是已标记 `miForwardRef` 但未在非托管代码中实现的类方法 (通过 PInvoke) 或由运行时本身内部实现  
  
 枚举排除在模块范围 (全局) 或接口或抽象类中定义的所有方法。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataImport 接口](imetadataimport-interface.md)
- [IMetaDataImport2 接口](imetadataimport2-interface.md)
