---
description: 了解详细信息： IMetaDataAssemblyImport：： CloseEnum 方法
title: IMetaDataAssemblyImport::CloseEnum 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.CloseEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::CloseEnum
helpviewer_keywords:
- CloseEnum method, IMetaDataAssemblyImport interface [.NET Framework metadata]
- IMetaDataAssemblyImport::CloseEnum method [.NET Framework metadata]
ms.assetid: c9df4087-12b3-46d9-b075-9067dd7805df
topic_type:
- apiref
ms.openlocfilehash: 3ff234fac905a058ed832d58a0f996a2c7393ed0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678076"
---
# <a name="imetadataassemblyimportcloseenum-method"></a>IMetaDataAssemblyImport::CloseEnum 方法

释放对指定枚举实例的引用。  
  
## <a name="syntax"></a>语法  
  
```cpp  
void CloseEnum (  
    [in] HCORENUM     hEnum  
);  
```  
  
## <a name="parameters"></a>参数  

 `hEnum`  
 中要关闭的枚举实例。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MsCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataAssemblyImport 接口](imetadataassemblyimport-interface.md)
