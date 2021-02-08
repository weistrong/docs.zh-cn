---
description: 了解详细信息： CertFreeAuthenticodeSignerInfo 函数
title: CertFreeAuthenticodeSignerInfo 函数
ms.date: 03/30/2017
api_name:
- CertFreeAuthenticodeSignerInfo
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 8029633c-b6e4-4665-a7c2-89607c3247ef
topic_type:
- apiref
ms.openlocfilehash: 6e8a97e8fee37d885c7d32102ed8cc7654992223
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772973"
---
# <a name="certfreeauthenticodesignerinfo-function"></a>CertFreeAuthenticodeSignerInfo 函数

释放为 [AXL_AUTHENTICODE_SIGNER_INFO](axl-authenticode-signer-info-structure.md) 结构分配的资源。

## <a name="syntax"></a>语法

```cpp
HRESULT CertFreeAuthenticodeSignerInfo (
    [in, out]  PAXL_AUTHENTICODE_SIGNER_INFO   pSignerInfo);
```

## <a name="parameters"></a>参数

 `pSignerInfo`\
 [in, out] 要释放的签署人信息。 请参阅 [AXL_AUTHENTICODE_SIGNER_INFO](axl-authenticode-signer-info-structure.md) 结构。

## <a name="return-value"></a>返回值

 如果此函数成功，则返回 `S_OK`。 否则，返回错误代码。

## <a name="requirements"></a>要求

**程序集**： clr.dll

## <a name="see-also"></a>请参阅

- [验证码](index.md)
