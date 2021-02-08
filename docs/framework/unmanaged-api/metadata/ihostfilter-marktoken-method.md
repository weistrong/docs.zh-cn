---
description: 了解详细信息： IHostFilter：： MarkToken 方法
title: IHostFilter::MarkToken 方法
ms.date: 03/30/2017
api_name:
- IHostFilter.MarkToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostFilter::MarkToken
helpviewer_keywords:
- MarkToken method, IHostFilter interface [.NET Framework metadata]
- IHostFilter::MarkToken method [.NET Framework metadata]
ms.assetid: d7061343-d0a3-4fd5-b312-61974f98bd62
topic_type:
- apiref
ms.openlocfilehash: c8f5ecdef56b77e1b0031a93d6d8f7de79de4c3b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784179"
---
# <a name="ihostfiltermarktoken-method"></a>IHostFilter::MarkToken 方法

指示将处理指定的元数据标记。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT MarkToken (  
    [in]  mdToken         tk  
);  
```  
  
## <a name="parameters"></a>参数  

 `tk`  
 中要处理的元数据标记。  
  
## <a name="remarks"></a>备注  

 通常，如果令牌在元数据范围内，则需要对其进行处理。 `MarkToken`方法通过[IMetaDataEmit：： SetHandler](imetadataemit-sethandler-method.md)方法传递给元数据引擎。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MsCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [元数据接口](metadata-interfaces.md)
- [IHostFilter 接口](ihostfilter-interface.md)
