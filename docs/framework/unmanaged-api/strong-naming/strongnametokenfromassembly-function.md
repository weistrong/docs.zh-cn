---
description: 了解详细信息： StrongNameTokenFromAssembly 函数
title: StrongNameTokenFromAssembly 函数
ms.date: 03/30/2017
api_name:
- StrongNameTokenFromAssembly
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameTokenFromAssembly
helpviewer_keywords:
- StrongNameTokenFromAssembly function [.NET Framework strong naming]
ms.assetid: 0a4b47ee-02f6-4a98-864e-a6f11ca3f2d9
topic_type:
- apiref
ms.openlocfilehash: 3646d441da4885624c15d5e53670a8dd8db45160
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794476"
---
# <a name="strongnametokenfromassembly-function"></a>StrongNameTokenFromAssembly 函数

从指定的程序集文件创建强名称令牌。  
  
 此函数已弃用。 改为使用 [ICLRStrongName：： StrongNameTokenFromAssembly](../hosting/iclrstrongname-strongnametokenfromassembly-method.md) 方法。  
  
## <a name="syntax"></a>语法  
  
```cpp  
BOOLEAN StrongNameTokenFromAssembly (  
    [in]  LPCWSTR   wszFilePath,  
    [out] BYTE      **ppbStrongNameToken,  
    [out] ULONG     *pcbStrongNameToken  
);  
```  
  
## <a name="parameters"></a>参数  

 `wszFilePath`  
 中适用于程序集的可移植可执行文件 (PE) 文件的路径。  
  
 `ppbStrongNameToken`  
 弄返回的强名称标记。  
  
 `pcbStrongNameToken`  
 弄强名称令牌的大小（以字节为单位）。  
  
## <a name="return-value"></a>返回值  

 `true` 成功完成时;否则为 `false` 。  
  
## <a name="remarks"></a>备注  

 强名称标记是公钥的缩写形式。 标记是从用于对程序集进行签名的公钥创建的64位哈希。 该令牌是程序集的强名称的一部分，并且可以从程序集元数据中读取。  
  
 创建令牌后，应调用 [StrongNameFreeBuffer](strongnamefreebuffer-function.md) 函数以释放已分配的内存。  
  
 如果 `StrongNameTokenFromAssembly` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Stackexchange.redis.strongname  
  
 **库：** 作为中的资源包含 mscoree.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [StrongNameTokenFromAssembly 方法](../hosting/iclrstrongname-strongnametokenfromassembly-method.md)
- [StrongNameTokenFromAssemblyEx 方法](../hosting/iclrstrongname-strongnametokenfromassemblyex-method.md)
- [ICLRStrongName 接口](../hosting/iclrstrongname-interface.md)
