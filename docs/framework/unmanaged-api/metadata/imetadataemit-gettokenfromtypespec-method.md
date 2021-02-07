---
description: 了解详细信息： IMetaDataEmit：： GetTokenFromTypeSpec 方法
title: IMetaDataEmit::GetTokenFromTypeSpec 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.GetTokenFromTypeSpec
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::GetTokenFromTypeSpec
helpviewer_keywords:
- GetTokenFromTypeSpec method [.NET Framework metadata]
- IMetaDataEmit::GetTokenFromTypeSpec method [.NET Framework metadata]
ms.assetid: 7de6447a-a751-49d8-87e2-951cee77b536
topic_type:
- apiref
ms.openlocfilehash: 09f7133af9b9d912b03cdc1c93744ee260c69169
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728231"
---
# <a name="imetadataemitgettokenfromtypespec-method"></a>IMetaDataEmit::GetTokenFromTypeSpec 方法

获取具有指定元数据签名的类型的元数据标记。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetTokenFromTypeSpec (
    [in]  PCCOR_SIGNATURE       pvSig,
    [in]  ULONG                 cbSig,
    [out] mdTypeSpec            *ptypespec
);  
```  
  
## <a name="parameters"></a>参数  

 `pvSig`  
 中要定义的签名。  
  
 `cbSig`  
 中中的字节数 `pvSig` 。  
  
 `ptypespec`  
 弄 `mdTypeSpec` 分配的令牌。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MSCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataEmit 接口](imetadataemit-interface.md)
- [IMetaDataEmit2 接口](imetadataemit2-interface.md)
