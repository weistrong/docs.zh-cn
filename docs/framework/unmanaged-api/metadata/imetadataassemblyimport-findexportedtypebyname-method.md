---
description: 了解详细信息： IMetaDataAssemblyImport：： FindExportedTypeByName 方法
title: IMetaDataAssemblyImport::FindExportedTypeByName 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.FindExportedTypeByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::FindExportedTypeByName
helpviewer_keywords:
- FindExportedTypeByName method [.NET Framework metadata]
- IMetaDataAssemblyImport::FindExportedTypeByName method [.NET Framework metadata]
ms.assetid: 46264b2c-574d-4dde-aafc-77187a104fdd
topic_type:
- apiref
ms.openlocfilehash: 4a2dc2b65b7f7fe6d5f2e120c635214d457991bc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677979"
---
# <a name="imetadataassemblyimportfindexportedtypebyname-method"></a>IMetaDataAssemblyImport::FindExportedTypeByName 方法

获取一个指针，该指针指向导出的类型（给定其名称和封闭类型）。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT FindExportedTypeByName (  
    [in]  LPCWSTR           szName,
    [in]  mdToken           mdtExportedType,
    [out] mdExportedType    *ptkExportedType  
);  
```  
  
## <a name="parameters"></a>参数  

 `szName`  
 中导出的类型的名称。  
  
 `mdtExportedType`  
 中导出类型的封闭类的元数据标记。 `mdExportedTypeNil`如果请求的导出类型不是嵌套类型，则此值为。  
  
 `ptkExportedType`  
 弄一个指针，指向 `mdExportedType` 表示导出类型的标记。  
  
## <a name="remarks"></a>备注  

 `FindExportedTypeByName`方法使用公共语言运行时所使用的标准规则来解析引用。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MsCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataAssemblyImport 接口](imetadataassemblyimport-interface.md)
- [运行时如何定位程序集](../../deployment/how-the-runtime-locates-assemblies.md)
