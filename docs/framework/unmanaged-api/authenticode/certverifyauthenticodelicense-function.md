---
description: 了解详细信息： CertVerifyAuthenticodeLicense 函数
title: CertVerifyAuthenticodeLicense 函数
ms.date: 03/30/2017
api_name:
- CertVerifyAuthenticodeLicense
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 00118de7-33c6-41c4-8e1f-5d5e35e0da83
topic_type:
- apiref
ms.openlocfilehash: 0174223a4c1b984bf2d5d957219a85230fef8d0e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772843"
---
# <a name="certverifyauthenticodelicense-function"></a><span data-ttu-id="95ad2-103">CertVerifyAuthenticodeLicense 函数</span><span class="sxs-lookup"><span data-stu-id="95ad2-103">CertVerifyAuthenticodeLicense Function</span></span>

<span data-ttu-id="95ad2-104">验证验证码 XrML 许可证的有效性。</span><span class="sxs-lookup"><span data-stu-id="95ad2-104">Verifies the validity of an Authenticode XrML license.</span></span>

## <a name="syntax"></a><span data-ttu-id="95ad2-105">语法</span><span class="sxs-lookup"><span data-stu-id="95ad2-105">Syntax</span></span>

```cpp
HRESULT CertVerifyAuthenticodeLicense (
    [in]   PCRYPT_DATA_BLOB                   pLicenseBlob,
    [in]   OPTIONAL DWORD                     dwFlags,
    [out]  PAXL_AUTHENTICODE_SIGNER_INFO      pSignerInfo,
    [out]  PAXL_AUTHENTICODE_TIMESTAMPER_INFO pTimestamperInfo
);
```

## <a name="parameters"></a><span data-ttu-id="95ad2-106">参数</span><span class="sxs-lookup"><span data-stu-id="95ad2-106">Parameters</span></span>

 `pLicenseBlob`\
 <span data-ttu-id="95ad2-107">[in] 要验证的验证码 XrML 许可证。</span><span class="sxs-lookup"><span data-stu-id="95ad2-107">[in] The Authenticode XrML license to be verified.</span></span>

 <span data-ttu-id="95ad2-108">请参阅 [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) 结构。</span><span class="sxs-lookup"><span data-stu-id="95ad2-108">See the [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure.</span></span>

 `dwFlags`\
 <span data-ttu-id="95ad2-109">[in] 可选。</span><span class="sxs-lookup"><span data-stu-id="95ad2-109">[in] Optional.</span></span> <span data-ttu-id="95ad2-110">以下值的组合：</span><span class="sxs-lookup"><span data-stu-id="95ad2-110">A combination of following values:</span></span>

- <span data-ttu-id="95ad2-111">AXL_REVOCATION_NO_CHECK</span><span class="sxs-lookup"><span data-stu-id="95ad2-111">AXL_REVOCATION_NO_CHECK</span></span>

- <span data-ttu-id="95ad2-112">AXL_REVOCATION_CHECK_END_CERT_ONLY</span><span class="sxs-lookup"><span data-stu-id="95ad2-112">AXL_REVOCATION_CHECK_END_CERT_ONLY</span></span>

- <span data-ttu-id="95ad2-113">AXL_REVOCATION_CHECK_ENTIRE_CHAIN</span><span class="sxs-lookup"><span data-stu-id="95ad2-113">AXL_REVOCATION_CHECK_ENTIRE_CHAIN</span></span>

- <span data-ttu-id="95ad2-114">AXL_URL_CACHE_ONLY_RETRIEVAL</span><span class="sxs-lookup"><span data-stu-id="95ad2-114">AXL_URL_CACHE_ONLY_RETRIEVAL</span></span>

- <span data-ttu-id="95ad2-115">AXL_LIFETIME_SIGNING</span><span class="sxs-lookup"><span data-stu-id="95ad2-115">AXL_LIFETIME_SIGNING</span></span>

- <span data-ttu-id="95ad2-116">AXL_TRUST_MICROSOFT_ROOT_ONLY</span><span class="sxs-lookup"><span data-stu-id="95ad2-116">AXL_TRUST_MICROSOFT_ROOT_ONLY</span></span>

 `pSignerInfo`\
 <span data-ttu-id="95ad2-117">[out] 接收签署人的信息。</span><span class="sxs-lookup"><span data-stu-id="95ad2-117">[out] To receive the signer's information.</span></span> <span data-ttu-id="95ad2-118">如果许可证未进行签名，则 `dwError` 将设置为 TRUST_E_NOSIGNATURE。</span><span class="sxs-lookup"><span data-stu-id="95ad2-118">If the license wasn't signed, `dwError` is set to TRUST_E_NOSIGNATURE.</span></span> <span data-ttu-id="95ad2-119">调用方负责在使用后使用 [CertFreeAuthenticodeSignerInfo](certfreeauthenticodesignerinfo-function.md) 函数释放资源。</span><span class="sxs-lookup"><span data-stu-id="95ad2-119">It is the caller's responsibility to free resources by using the [CertFreeAuthenticodeSignerInfo](certfreeauthenticodesignerinfo-function.md) function after use.</span></span>

 <span data-ttu-id="95ad2-120">请参阅 [AXL_AUTHENTICODE_SIGNER_INFO 结构](axl-authenticode-signer-info-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="95ad2-120">See [AXL_AUTHENTICODE_SIGNER_INFO Structure](axl-authenticode-signer-info-structure.md).</span></span>

 `pTimestamperInfo`\
 <span data-ttu-id="95ad2-121">[out] 接收时间戳签署人的信息（如果有）。</span><span class="sxs-lookup"><span data-stu-id="95ad2-121">[out] To receive time stamper's information, if available.</span></span> <span data-ttu-id="95ad2-122">如果未对许可证签署时间戳，则 `dwError` 将设置为 TRUST_E_NOSIGNATURE。</span><span class="sxs-lookup"><span data-stu-id="95ad2-122">If the license was not time-stamped, `dwError` is set to TRUST_E_NOSIGNATURE.</span></span> <span data-ttu-id="95ad2-123">调用方负责在使用后使用 [CertFreeAuthenticodeTimestamperInfo](certfreeauthenticodetimestamperinfo-function.md) 函数释放资源。</span><span class="sxs-lookup"><span data-stu-id="95ad2-123">It is the caller's responsibility to free resources by using the [CertFreeAuthenticodeTimestamperInfo](certfreeauthenticodetimestamperinfo-function.md) function after use.</span></span>

 <span data-ttu-id="95ad2-124">请参阅 [AXL_AUTHENTICODE_TIMESTAMPER_INFO 结构](axl-authenticode-timestamper-info-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="95ad2-124">See [AXL_AUTHENTICODE_TIMESTAMPER_INFO Structure](axl-authenticode-timestamper-info-structure.md).</span></span>

## <a name="return-value"></a><span data-ttu-id="95ad2-125">返回值</span><span class="sxs-lookup"><span data-stu-id="95ad2-125">Return Value</span></span>

 <span data-ttu-id="95ad2-126">如果成功，则返回 `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="95ad2-126">Returns `S_OK` if successful.</span></span> <span data-ttu-id="95ad2-127">否则，返回错误代码。</span><span class="sxs-lookup"><span data-stu-id="95ad2-127">Otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="95ad2-128">要求</span><span class="sxs-lookup"><span data-stu-id="95ad2-128">Requirements</span></span>

<span data-ttu-id="95ad2-129">**程序集**： clr.dll</span><span class="sxs-lookup"><span data-stu-id="95ad2-129">**Assembly**: clr.dll</span></span>

## <a name="see-also"></a><span data-ttu-id="95ad2-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="95ad2-130">See also</span></span>

- [<span data-ttu-id="95ad2-131">验证码</span><span class="sxs-lookup"><span data-stu-id="95ad2-131">Authenticode</span></span>](index.md)
- [<span data-ttu-id="95ad2-132">GetHashFromHandle 方法</span><span class="sxs-lookup"><span data-stu-id="95ad2-132">GetHashFromHandle Method</span></span>](../hosting/iclrstrongname-gethashfromhandle-method.md)
- [<span data-ttu-id="95ad2-133">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="95ad2-133">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
