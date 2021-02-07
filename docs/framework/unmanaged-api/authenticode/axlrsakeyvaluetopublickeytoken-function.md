---
description: 了解详细信息： _AxlRSAKeyValueToPublicKeyToken 函数
title: _AxlRSAKeyValueToPublicKeyToken 函数
ms.date: 03/30/2017
api_name:
- _AxlRSAKeyValueToPublicKeyToken
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: d60f19fe-7bec-47ba-b60e-ba9ce66abf8c
topic_type:
- apiref
ms.openlocfilehash: 01fc4cdc1d9985375748307ca2d7fff97191c908
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747265"
---
# <a name="_axlrsakeyvaluetopublickeytoken-function"></a><span data-ttu-id="56e1e-103">\_AxlRSAKeyValueToPublicKeyToken 函数</span><span class="sxs-lookup"><span data-stu-id="56e1e-103">\_AxlRSAKeyValueToPublicKeyToken function</span></span>

<span data-ttu-id="56e1e-104">将模数和指数转换为强名称公钥标记。</span><span class="sxs-lookup"><span data-stu-id="56e1e-104">Converts a Modulus and Exponent to a strong name public key token.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e1e-105">语法</span><span class="sxs-lookup"><span data-stu-id="56e1e-105">Syntax</span></span>

```cpp
HRESULT _AxlRSAKeyValueToPublicKeyToken (
    [in]  PCRYPT_DATA_BLOB pModulusBlob,
    [in]  PCRYPT_DATA_BLOB pExponentBlob,
    [out] LPWSTR           *ppwszPublicKeyToken
);
```

## <a name="parameters"></a><span data-ttu-id="56e1e-106">参数</span><span class="sxs-lookup"><span data-stu-id="56e1e-106">Parameters</span></span>

 `pModulusBlob`\
 <span data-ttu-id="56e1e-107">中Base64 编码的模数 blob 从 \<Modulus> 元素)  (。</span><span class="sxs-lookup"><span data-stu-id="56e1e-107">[in] The base64-encoded Modulus blob (from the \<Modulus> element).</span></span>  <span data-ttu-id="56e1e-108">请参阅 [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) 结构。</span><span class="sxs-lookup"><span data-stu-id="56e1e-108">See the [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure.</span></span>

 `pExponentBlob`\
 <span data-ttu-id="56e1e-109">中Base64 编码的指数 blob 从 \<Exponent> 元素)  (。</span><span class="sxs-lookup"><span data-stu-id="56e1e-109">[in] The base64-encoded Exponent blob (from the \<Exponent> element).</span></span> <span data-ttu-id="56e1e-110">请参阅 [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) 结构。</span><span class="sxs-lookup"><span data-stu-id="56e1e-110">See the [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure.</span></span>

 `ppwszPublicKeyToken`\
 <span data-ttu-id="56e1e-111">[out] 指向 WCHAR \* 的指针，用于接收十六进制编码的公钥标记。</span><span class="sxs-lookup"><span data-stu-id="56e1e-111">[out] A pointer to WCHAR \* to receive the hex-encoded public key token.</span></span>

## <a name="return-value"></a><span data-ttu-id="56e1e-112">返回值</span><span class="sxs-lookup"><span data-stu-id="56e1e-112">Return Value</span></span>

 <span data-ttu-id="56e1e-113">如果此函数成功，则返回 `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="56e1e-113">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="56e1e-114">否则，返回错误代码。</span><span class="sxs-lookup"><span data-stu-id="56e1e-114">Otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="56e1e-115">要求</span><span class="sxs-lookup"><span data-stu-id="56e1e-115">Requirements</span></span>

<span data-ttu-id="56e1e-116">**程序集**： clr.dll</span><span class="sxs-lookup"><span data-stu-id="56e1e-116">**Assembly**: clr.dll</span></span>

## <a name="see-also"></a><span data-ttu-id="56e1e-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="56e1e-117">See also</span></span>

- [<span data-ttu-id="56e1e-118">验证码</span><span class="sxs-lookup"><span data-stu-id="56e1e-118">Authenticode</span></span>](index.md)
