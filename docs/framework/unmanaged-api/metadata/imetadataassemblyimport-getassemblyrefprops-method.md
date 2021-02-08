---
description: 了解详细信息： IMetaDataAssemblyImport：： GetAssemblyRefProps 方法
title: IMetaDataAssemblyImport::GetAssemblyRefProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetAssemblyRefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetAssemblyRefProps
helpviewer_keywords:
- IMetaDataAssemblyImport::GetAssemblyRefProps method [.NET Framework metadata]
- GetAssemblyRefProps method [.NET Framework metadata]
ms.assetid: 5c6b7fb4-cbca-4479-b650-ab9a99732ea0
topic_type:
- apiref
ms.openlocfilehash: f7011806920ba37ca84b1a48f12da3a5557fa464
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784127"
---
# <a name="imetadataassemblyimportgetassemblyrefprops-method"></a>IMetaDataAssemblyImport::GetAssemblyRefProps 方法

获取具有指定元数据签名的程序集引用的属性集。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetAssemblyRefProps (  
    [in]  mdAssemblyRef        mdar,
    [out] const void          **ppbPublicKeyOrToken,
    [out] ULONG                *pcbPublicKeyOrToken,
    [out] LPWSTR               szName,
    [in]  ULONG                cchName,
    [out] ULONG                *pchName,
    [out] ASSEMBLYMETADATA     *pMetaData,
    [out] const void           **ppbHashValue,
    [out] ULONG                *pcbHashValue,
    [out] DWORD                *pdwAssemblyRefFlags  
);  
```  
  
## <a name="parameters"></a>参数  

 `mdar`  
 中 `mdAssemblyRef` 表示要获取其属性的程序集引用的元数据标记。  
  
 `ppbPublicKeyOrToken`  
 弄指向公钥或元数据标记的指针。  
  
 `pcbPublicKeyOrToken`  
 弄返回的公钥或令牌中的字节数。  
  
 `szName`  
 弄程序集的简单名称。  
  
 `cchName`  
 中的大小（宽字符） `szName` 。  
  
 `pchName`  
 弄一个指针，指向在中实际返回的宽字符数 `szName` 。  
  
 `pMetaData`  
 弄指向 ASSEMBLYMETADATA 结构的指针，该结构包含程序集元数据。  
  
 `ppbHashValue`  
 弄指向哈希值的指针。 这是所引用程序集的属性的哈希，使用 SHA-1 算法， `PublicKey` 除非已设置 [AssemblyRefFlags](assemblyrefflags-enumeration.md) 枚举的 arfFullOriginator 标志。  
  
 `pcbHashValue`  
 弄返回的哈希值中的宽字符数。  
  
 `pdwAssemblyRefFlags`  
 弄一个指针，指向用于描述应用于程序集的元数据的标志。 Flags 值是一个或多个 [CorAssemblyFlags](corassemblyflags-enumeration.md) 值的组合。  
  
## <a name="return-value"></a>返回值  

 如果成功，则此方法返回 S_OK;否则，它将返回在 Winerror.h 头文件中定义的错误代码之一。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MsCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataAssemblyImport 接口](imetadataassemblyimport-interface.md)
