---
description: 了解详细信息： ICLRStrongName：： StrongNameTokenFromPublicKey 方法
title: ICLRStrongName::StrongNameTokenFromPublicKey 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameTokenFromPublicKey
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameTokenFromPublicKey
helpviewer_keywords:
- ICLRStrongName::StrongNameTokenFromPublicKey method [.NET Framework hosting]
- StrongNameTokenFromPublicKey method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 7962ce88-7e86-4a6f-8298-621b01ffc3c2
topic_type:
- apiref
ms.openlocfilehash: de245b151e5ca016a00793a8901c0fd990a3f804
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789738"
---
# <a name="iclrstrongnamestrongnametokenfrompublickey-method"></a>ICLRStrongName::StrongNameTokenFromPublicKey 方法

获取表示公钥的标记。 强名称标记是公钥的缩写形式。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT StrongNameTokenFromPublicKey (
    [in]  BYTE    *pbPublicKeyBlob,  
    [in]  ULONG   cbPublicKeyBlob,  
    [out] BYTE    **ppbStrongNameToken,  
    [out] ULONG   *pcbStrongNameToken  
);  
```  
  
## <a name="parameters"></a>参数  

 `pbPublicKeyBlob`  
 中 [PublicKeyBlob](../strong-naming/publickeyblob-structure.md) 类型的结构，它包含用于生成强名称签名的密钥对的公共部分。  
  
 `cbPublicKeyBlob`  
 中的大小（以字节为单位） `pbPublicKeyBlob` 。  
  
 `ppbStrongNameToken`  
 弄与传入的密钥对应的强名称标记 `pbPublicKeyBlob` 。 公共语言运行时分配要在其中返回标记的内存。 调用方必须通过使用 [ICLRStrongName：： StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) 方法释放此内存。  
  
 `pcbStrongNameToken`  
 弄返回的强名称标记的大小（以字节为单位）。  
  
## <a name="return-value"></a>返回值  

 `S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。  
  
## <a name="remarks"></a>备注  

 强名称标记是用于在元数据中存储密钥信息时节省空间的公钥的缩写形式。 具体而言，强名称令牌在程序集引用中用于引用依赖程序集。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** MetaHost  
  
 **库：** 作为中的资源包含 mscoree.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [StrongNameGetPublicKey 方法](iclrstrongname-strongnamegetpublickey-method.md)
- [PublicKeyBlob 结构](../strong-naming/publickeyblob-structure.md)
- [ICLRStrongName 接口](iclrstrongname-interface.md)
