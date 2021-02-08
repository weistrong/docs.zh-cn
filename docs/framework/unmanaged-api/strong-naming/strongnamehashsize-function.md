---
description: 了解详细信息： StrongNameHashSize 函数
title: StrongNameHashSize 函数
ms.date: 03/30/2017
api_name:
- StrongNameHashSize
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameHashSize
helpviewer_keywords:
- StrongNameHashSize function [.NET Framework strong naming]
ms.assetid: 738c98d7-a60c-45fe-a296-220af05e6991
topic_type:
- apiref
ms.openlocfilehash: 3e6700bfce3ba480814f3837011c5f8f7107bbd5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781228"
---
# <a name="strongnamehashsize-function"></a>StrongNameHashSize 函数

使用指定的哈希算法获取哈希所需的缓冲区大小。  
  
 此函数已弃用。 改为使用 [ICLRStrongName：： StrongNameHashSize](../hosting/iclrstrongname-strongnamehashsize-method.md) 方法。  
  
## <a name="syntax"></a>语法  
  
```cpp  
BOOLEAN StrongNameHashSize (  
    [in]  ULONG   ulHashAlg,  
    [out] DWORD   *pcbSize  
);  
```  
  
## <a name="parameters"></a>参数  

 `ulHashAlg`  
 中用于计算缓冲区大小的哈希算法。  
  
 `pcbSize`  
 弄返回的缓冲区大小（以字节为单位）。  
  
## <a name="return-value"></a>返回值  

 `true` 成功完成时;否则为 `false` 。  
  
## <a name="remarks"></a>备注  

 如果 `StrongNameHashSize` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Stackexchange.redis.strongname  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [StrongNameHashSize 方法](../hosting/iclrstrongname-strongnamehashsize-method.md)
- [ICLRStrongName 接口](../hosting/iclrstrongname-interface.md)
