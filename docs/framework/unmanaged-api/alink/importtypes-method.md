---
description: 了解详细信息： ImportTypes 方法
title: ImportTypes 方法
ms.date: 03/30/2017
api_name:
- IALink.ImportTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportTypes
helpviewer_keywords:
- ImportTypes method
ms.assetid: 351d4b4c-c939-486d-9471-51914a55f471
topic_type:
- apiref
ms.openlocfilehash: 9a30c735ca2c9ad0f945628c3de1eb1bb56efe2c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662619"
---
# <a name="importtypes-method"></a>ImportTypes 方法

开始从通过 [ImportFile 方法](importfile-method.md)导入的每个范围导入类型。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT ImportTypes(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    HALINKENUM* phEnum,  
    IMetaDataImport** ppImportScope,  
    DWORD* pdwCountOfTypes  
) PURE;  
```  
  
## <a name="parameters"></a>参数  

 `AssemblyID`  
 要导入到的程序集的 ID。  
  
 `FileToken`  
 要从中导入的文件的 ID。  
  
 `dwScope`  
 要导入的从零开始的范围。  
  
 `phEnum`  
 接收此范围内的类型的枚举器句柄。  
  
 `ppImportScope`  
 可以选择接收 [IMetaDataImport 接口](../metadata/imetadataimport-interface.md) 接口。  
  
 `pdwCountOfTypes`  
 可以选择接收指定范围内的类型的计数。  
  
## <a name="return-value"></a>返回值  

 如果方法成功，则返回 S_OK。  
  
## <a name="requirements"></a>要求  

 需要 alink  
  
## <a name="see-also"></a>请参阅

- [IALink 接口](ialink-interface.md)
- [IALink2 接口](ialink2-interface.md)
- [ALink API](index.md)
