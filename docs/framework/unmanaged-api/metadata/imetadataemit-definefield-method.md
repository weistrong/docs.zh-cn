---
description: 了解详细信息： IMetaDataEmit：:D efineField 方法
title: IMetaDataEmit::DefineField 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineField
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineField
helpviewer_keywords:
- IMetaDataEmit::DefineField method [.NET Framework metadata]
- DefineField method, IMetaDataEmit interface [.NET Framework metadata
ms.assetid: 6b5be4fc-2e86-499c-8b09-833160bca767
topic_type:
- apiref
ms.openlocfilehash: 7636b1521de721cc183305e8a0763ff0a61f331b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753440"
---
# <a name="imetadataemitdefinefield-method"></a>IMetaDataEmit::DefineField 方法

使用指定的元数据签名创建字段的定义，并获取该字段定义的标记。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT DefineField (
    [in]  mdTypeDef   td,
    [in]  LPCWSTR     szName,
    [in]  DWORD       dwFieldFlags,
    [in]  PCCOR_SIGNATURE pvSigBlob,
    [in]  ULONG       cbSigBlob,
    [in]  DWORD       dwCPlusTypeFlag,
    [in]  void const  *pValue,
    [in]  ULONG       cchValue,
    [out] mdFieldDef  *pmd
);  
```  
  
## <a name="parameters"></a>参数  

 `td`  
 中 `mdTypeDef` 封闭类或接口的标记。  
  
 `szName`  
 中Unicode 中的字段名称。  
  
 `dwFieldFlags`  
 中字段特性。 这是一个值的位掩码 `CorFieldAttr` 。  
  
 `pvSigBlob`  
 中作为 BLOB 的字段签名。  
  
 `cbSigBlob`  
 中中的字节数 `pvSigBlob` 。  
  
 `dwCPlusTypeFlag`  
 中`ELEMENT_TYPE_` *\** 常数值的。 这是一个 `CorElementType` 值。 如果没有为字段定义常数值，请使用 `ELEMENT_TYPE_END` 。  
  
 `pValue`  
 中字段的常数值。  
  
 `cchValue`  
 中 (Unicode) 字符的大小 `pValue` 。  
  
 `pmd`  
 弄 `mdFieldDef` 分配的令牌。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MSCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataEmit 接口](imetadataemit-interface.md)
- [IMetaDataEmit2 接口](imetadataemit2-interface.md)
