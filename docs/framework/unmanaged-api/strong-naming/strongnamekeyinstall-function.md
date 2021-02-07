---
description: 了解详细信息： StrongNameKeyInstall 函数
title: StrongNameKeyInstall 函数
ms.date: 03/30/2017
api_name:
- StrongNameKeyInstall
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameKeyInstall
helpviewer_keywords:
- StrongNameKeyInstall function [.NET Framework strong naming]
ms.assetid: e32fd546-7757-4681-be3d-658e93281e50
topic_type:
- apiref
ms.openlocfilehash: 0a5d3971ac0927dda7066405adc01a5c80b7faca
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670536"
---
# <a name="strongnamekeyinstall-function"></a>StrongNameKeyInstall 函数

将公钥/私钥对导入容器。

此函数已弃用。 改为使用 [ICLRStrongName：： StrongNameKeyInstall](../hosting/iclrstrongname-strongnamekeyinstall-method.md) 方法。

## <a name="syntax"></a>语法

```cpp
BOOLEAN StrongNameKeyInstall (
    [in]  LPCWSTR   wszKeyContainer,
    [in]  BYTE      *pbKeyBlob,
    [in]  ULONG     cbKeyBlob
);
```

## <a name="parameters"></a>参数

`wszKeyContainer`\
中密钥容器的名称。 `wszKeyContainer` 必须为非空字符串。

`pbKeyBlob`\
中二进制密钥对。

`cbKeyBlob`\
中的大小（以字节为单位） `pbKeyBlob` 。

## <a name="return-value"></a>返回值

`true` 成功完成时;否则为 `false` 。

## <a name="remarks"></a>备注

使用 [StrongNameKeyDelete](strongnamekeydelete-function.md) 函数可删除密钥容器。

如果 `StrongNameKeyInstall` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。

## <a name="requirements"></a>要求

**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。

**标头：** Stackexchange.redis.strongname

**库：** 作为中的资源包含 MsCorEE.dll

**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]

## <a name="see-also"></a>请参阅

- [StrongNameKeyInstall 方法](../hosting/iclrstrongname-strongnamekeyinstall-method.md)
- [StrongNameKeyDelete 方法](../hosting/iclrstrongname-strongnamekeydelete-method.md)
- [ICLRStrongName 接口](../hosting/iclrstrongname-interface.md)
