---
description: 了解详细信息： _AxlPublicKeyBlobToPublicKeyToken 函数
title: _AxlPublicKeyBlobToPublicKeyToken 函数
ms.date: 03/30/2017
api_name:
- _AxlPublicKeyBlobToPublicKeyToken
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 2d92a746-d68c-4f53-a16e-727f071a2d80
topic_type:
- apiref
ms.openlocfilehash: df0b484bad64051eb892d4898a6c90777cc2d5cf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781930"
---
# <a name="_axlpublickeyblobtopublickeytoken-function"></a><span data-ttu-id="0edba-103">\_AxlPublicKeyBlobToPublicKeyToken 函数</span><span class="sxs-lookup"><span data-stu-id="0edba-103">\_AxlPublicKeyBlobToPublicKeyToken Function</span></span>

<span data-ttu-id="0edba-104">从 CSP PUBLICKEYBLOB 格式计算强名称公钥标记。</span><span class="sxs-lookup"><span data-stu-id="0edba-104">Computes the strong name public key token from a CSP PUBLICKEYBLOB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="0edba-105">语法</span><span class="sxs-lookup"><span data-stu-id="0edba-105">Syntax</span></span>

```cpp
HRESULT _AxlPublicKeyBlobToPublicKeyToken (
    [in]  PCCERT_CHAIN_CONTEXT   pCspPublicKeyBlob,
    [out] LPWSTR                 *ppwszPublicKeyToken
);
```

## <a name="parameters"></a><span data-ttu-id="0edba-106">参数</span><span class="sxs-lookup"><span data-stu-id="0edba-106">Parameters</span></span>

 `pCspPublicKeyBlob`\
 <span data-ttu-id="0edba-107">[in] CSP 公钥 Blob。</span><span class="sxs-lookup"><span data-stu-id="0edba-107">[in] The CSP public key blob.</span></span>

 `ppwszPublicKeyHash`\
 <span data-ttu-id="0edba-108">[out] 指向 WCHAR \* 的指针，用于接收十六进制编码的公钥哈希。</span><span class="sxs-lookup"><span data-stu-id="0edba-108">[out] A pointer to WCHAR \* to receive the hex-encoded public key hash.</span></span>

## <a name="return-value"></a><span data-ttu-id="0edba-109">返回值</span><span class="sxs-lookup"><span data-stu-id="0edba-109">Return Value</span></span>

 <span data-ttu-id="0edba-110">如果函数成功，则为 `S_OK`；否则为 `S_FALSE`。</span><span class="sxs-lookup"><span data-stu-id="0edba-110">`S_OK` if the function succeeds; otherwise `S_FALSE`.</span></span>

## <a name="requirements"></a><span data-ttu-id="0edba-111">要求</span><span class="sxs-lookup"><span data-stu-id="0edba-111">Requirements</span></span>

<span data-ttu-id="0edba-112">**程序集**： clr.dll</span><span class="sxs-lookup"><span data-stu-id="0edba-112">**Assembly**: clr.dll</span></span>

## <a name="see-also"></a><span data-ttu-id="0edba-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="0edba-113">See also</span></span>

- [<span data-ttu-id="0edba-114">验证码</span><span class="sxs-lookup"><span data-stu-id="0edba-114">Authenticode</span></span>](index.md)
