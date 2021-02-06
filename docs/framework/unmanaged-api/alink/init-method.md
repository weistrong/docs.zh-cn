---
description: 了解有关以下内容的详细信息： Init 方法
title: Init 方法
ms.date: 03/30/2017
api_name:
- IALink.Init
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- Init
helpviewer_keywords:
- Init method
ms.assetid: e48b5c64-049f-4f93-ad87-d07ae9cd5845
topic_type:
- apiref
ms.openlocfilehash: 531e05a09cbecbfb67c8c004d1e4ba1deb7e59a0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662554"
---
# <a name="init-method"></a>Init 方法

准备实现 [IALink 接口](ialink-interface.md) 以便使用的对象。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT Init(  
    IMetaDataDispenserEx* pDispenser,  
    IMetaDataError* pErrorHandler  
) PURE;  
```  
  
## <a name="parameters"></a>参数  

 `pDispenser`  
 指向元数据分配器的[IMetaDataDispenserEx 接口](../metadata/imetadatadispenserex-interface.md)指针。  
  
 `pErrorHandler`  
 指向可选错误处理接口的[IMetaDataError 接口](../metadata/imetadataerror-interface.md)指针。  
  
## <a name="return-value"></a>返回值  

 如果方法成功，则返回 S_OK。  
  
## <a name="requirements"></a>要求  

 需要 alink  
  
## <a name="see-also"></a>请参阅

- [IALink 接口](ialink-interface.md)
- [IALink2 接口](ialink2-interface.md)
- [ALink API](index.md)
