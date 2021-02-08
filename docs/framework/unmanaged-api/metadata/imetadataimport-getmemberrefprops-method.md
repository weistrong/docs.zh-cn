---
description: 了解详细信息： IMetaDataImport：： GetMemberRefProps 方法
title: IMetaDataImport::GetMemberRefProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMemberRefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMemberRefProps
helpviewer_keywords:
- GetMemberRefProps method [.NET Framework metadata]
- IMetaDataImport::GetMemberRefProps method [.NET Framework metadata]
ms.assetid: 0ea73055-ece0-4151-a094-414c88ef8941
topic_type:
- apiref
ms.openlocfilehash: b441f39d95c9af1e18d34a1a4d86d6cea33508c9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783868"
---
# <a name="imetadataimportgetmemberrefprops-method"></a>IMetaDataImport::GetMemberRefProps 方法

获取与指定标记引用的成员关联的元数据。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetMemberRefProps (  
   [in]  mdMemberRef       mr,
   [out] mdToken           *ptk,
   [out] LPWSTR            szMember,
   [in]  ULONG             cchMember,
   [out] ULONG             *pchMember,
   [out] PCCOR_SIGNATURE   *ppvSigBlob,
   [out] ULONG             *pbSig
);  
```  
  
## <a name="parameters"></a>参数  

 `mr`  
 中要为其返回关联的元数据的 MemberRef 标记。  
  
 `ptk`  
 弄TypeDef 或 TypeRef 或 TypeSpec 标记，它表示声明成员的类，或表示声明成员的 module 类的 ModuleRef 标记或表示成员的 MethodDef。  
  
 `szMember`  
 弄成员名称的字符串缓冲区。  
  
 `cchMember`  
 中请求的大小（以宽字符为大小） `szMember` 。  
  
 `pchMember`  
 弄返回的宽字符大小 `szMember` 。  
  
 `ppvSibBlob`  
 弄指向成员的二进制元数据签名的指针。  
  
 `pbSig`  
 弄的大小（以字节为单位） `ppvSigBlob` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataImport 接口](imetadataimport-interface.md)
- [IMetaDataImport2 接口](imetadataimport2-interface.md)
