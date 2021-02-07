---
description: 了解详细信息： PublicKeyBlob 结构
title: PublicKeyBlob 结构
ms.date: 03/30/2017
api_name:
- PublicKeyBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- PublicKeyBlob
helpviewer_keywords:
- PublicKeyBlob structure [.NET Framework strong naming]
ms.assetid: b9240712-829c-4c8d-9a09-a6e7aa63f63a
topic_type:
- apiref
ms.openlocfilehash: 94c1ea3d5a41bbb8941658e87f97cd6d6336187a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736474"
---
# <a name="publickeyblob-structure"></a>PublicKeyBlob 结构

表示公钥/私钥对的公钥，采用二进制格式。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef struct {  
    unsigned int SigAlgId;  
    unsigned int HashAlgId;  
    ULONG cbPublicKey;  
    BYTE PublicKey[1]  
} PublicKeyBlob;
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`SigAlgId`| (类型的签名算法的标识符 `ALG_ID` ，在公钥的 wincrypt.h) 中定义。|  
|`HashAlgId`| (类型的哈希算法的标识符 `ALG_ID` ，在公钥的 wincrypt.h) 中定义。|  
|`cbPublicKey`|密钥的长度（以字节为单位）。|  
|`PublicKey`|可变长度的字节数组，其中包含由 CryptoAPI 返回的格式的键值。|  
  
## <a name="remarks"></a>备注  

 `PublicKeyBlob`结构由[StrongNameGetPublicKey](strongnamegetpublickey-function.md)、 [StrongNameSignatureGeneration](strongnamesignaturegeneration-function.md)和其他强名称函数用来表示公钥/私钥对的公钥。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Stackexchange.redis.strongname  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [StrongNameGetPublicKey 函数](strongnamegetpublickey-function.md)
- [StrongNameSignatureGeneration 函数](strongnamesignaturegeneration-function.md)
