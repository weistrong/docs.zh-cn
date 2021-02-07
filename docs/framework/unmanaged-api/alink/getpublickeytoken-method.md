---
description: 了解详细信息： GetPublicKeyToken 方法
title: GetPublicKeyToken 方法
ms.date: 03/30/2017
api_name:
- IALink2.GetPublicKeyToken
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetPublicKeyToken
helpviewer_keywords:
- GetPublicKeyToken method
ms.assetid: 4a16374c-94b0-47b0-9fed-88c2b0cdccd4
topic_type:
- apiref
ms.openlocfilehash: b864c1dc61c7498ccca6aa04ef29b57a30e1a9ea
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718416"
---
# <a name="getpublickeytoken-method"></a>GetPublicKeyToken 方法

检索给定 keyfile 或 key 容器的公钥标记。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetPublicKeyToken(  
    LPCWSTR pszKeyFile,  
    LPCWSTR pszKeyContainer,  
    void* pvPublicKeyToken,  
    DWORD* pcbPublicKeyToken  
) PURE;  
```  
  
## <a name="parameters"></a>参数  

 `pszKeyFile`  
 密钥的文件名。  
  
 `pszKeyContainer`  
 密钥容器的名称。  
  
 `pvPublicKeyToken`  
 要存储密钥标记的地址。  
  
 `pcbPublicKeyToken`  
 指定指定的缓冲区的大小（以字节为单位） `pvPublicKeyToken` 。 返回时，包含所使用的实际字节数。  
  
## <a name="return-value"></a>返回值  

 如果方法成功，则返回 S_OK。  
  
## <a name="requirements"></a>要求  

 需要 alink。  
  
## <a name="see-also"></a>请参阅

- [IALink2 接口](ialink2-interface.md)
- [IALink 接口](ialink-interface.md)
- [ALink API](index.md)
