---
description: 了解详细信息： _AxlGetIssuerPublicKeyHash 函数
title: _AxlGetIssuerPublicKeyHash 函数
ms.date: 03/30/2017
api_name:
- _AxlGetIssuerPublicKeyHash
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: fb626b41-b888-4625-84c3-2c02b5e3866f
topic_type:
- apiref
ms.openlocfilehash: 586a072b33376a2fdade119fe3db0f48addfa3f5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747356"
---
# <a name="_axlgetissuerpublickeyhash-function"></a><span data-ttu-id="bfec2-103">\_AxlGetIssuerPublicKeyHash 函数</span><span class="sxs-lookup"><span data-stu-id="bfec2-103">\_AxlGetIssuerPublicKeyHash Function</span></span>

<span data-ttu-id="bfec2-104">检索与用于对指定证书进行签名的私钥关联的公钥的 SHA-1 哈希。</span><span class="sxs-lookup"><span data-stu-id="bfec2-104">Retrieves the SHA-1 hash of the public key associated with the private key that is used to sign the specified certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfec2-105">语法</span><span class="sxs-lookup"><span data-stu-id="bfec2-105">Syntax</span></span>

```cpp
HRESULT _AxlGetIssuerPublicKeyHash (
    [in]  IN PCRYPT_DATA_BLOB   pChainContext,
    [out] LPWSTR                *ppwszPublicKeyHash
);
```

## <a name="parameters"></a><span data-ttu-id="bfec2-106">参数</span><span class="sxs-lookup"><span data-stu-id="bfec2-106">Parameters</span></span>

 `pChainContext`\
 <span data-ttu-id="bfec2-107">[in] CSP 公钥 Blob。</span><span class="sxs-lookup"><span data-stu-id="bfec2-107">[in] The CSP public key blob.</span></span> <span data-ttu-id="bfec2-108">请参阅 [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) 结构。</span><span class="sxs-lookup"><span data-stu-id="bfec2-108">See the [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure.</span></span>

 `ppwszPublicKeyHash`\
 <span data-ttu-id="bfec2-109">[out] 指向 WCHAR \* 的指针，用于接收十六进制编码的公钥标记。</span><span class="sxs-lookup"><span data-stu-id="bfec2-109">[out] A pointer to WCHAR \* to receive the hex-encoded public key token.</span></span>

## <a name="return-value"></a><span data-ttu-id="bfec2-110">返回值</span><span class="sxs-lookup"><span data-stu-id="bfec2-110">Return Value</span></span>

 <span data-ttu-id="bfec2-111">如果函数成功，则为 `S_OK`；否则为 `S_FALSE`。</span><span class="sxs-lookup"><span data-stu-id="bfec2-111">`S_OK` if the function succeeds; otherwise `S_FALSE`.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfec2-112">要求</span><span class="sxs-lookup"><span data-stu-id="bfec2-112">Requirements</span></span>

<span data-ttu-id="bfec2-113">**程序集**： clr.dll</span><span class="sxs-lookup"><span data-stu-id="bfec2-113">**Assembly**: clr.dll</span></span>

## <a name="see-also"></a><span data-ttu-id="bfec2-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="bfec2-114">See also</span></span>

- [<span data-ttu-id="bfec2-115">验证码</span><span class="sxs-lookup"><span data-stu-id="bfec2-115">Authenticode</span></span>](index.md)
