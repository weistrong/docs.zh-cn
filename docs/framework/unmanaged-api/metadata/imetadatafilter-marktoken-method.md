---
description: 了解详细信息： IMetaDataFilter：： MarkToken 方法
title: IMetaDataFilter::MarkToken 方法
ms.date: 03/30/2017
api_name:
- IMetaDataFilter.MarkToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataFilter::MarkToken
helpviewer_keywords:
- IMetaDataFilter::MarkToken method [.NET Framework metadata]
- MarkToken method, IMetaDataFilter interface [.NET Framework metadata]
ms.assetid: bd492834-6529-4d39-b93d-f8cdbd3e297f
topic_type:
- apiref
ms.openlocfilehash: 97191533ae7d2bdc951521f1929a4c001c521b9d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677770"
---
# <a name="imetadatafiltermarktoken-method"></a>IMetaDataFilter::MarkToken 方法

设置一个值，该值指示已处理指定的元数据标记。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT MarkToken (  
    [in] mdToken   tk  
);  
```  
  
## <a name="parameters"></a>参数  

 `tk`  
 中标记为已处理的标记。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MsCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataFilter 接口](imetadatafilter-interface.md)
