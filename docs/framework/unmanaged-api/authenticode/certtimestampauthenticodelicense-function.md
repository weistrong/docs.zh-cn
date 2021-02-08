---
description: 了解详细信息： CertTimestampAuthenticodeLicense 函数
title: CertTimestampAuthenticodeLicense 函数
ms.date: 03/30/2017
api_name:
- CertTimestampAuthenticodeLicense
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: d468325a-21c5-43ce-8567-84e342b22308
topic_type:
- apiref
ms.openlocfilehash: 79b1a924a99a76c18e6434abfed0a90da71eb6f9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772913"
---
# <a name="certtimestampauthenticodelicense-function"></a><span data-ttu-id="2d49b-103">CertTimestampAuthenticodeLicense 函数</span><span class="sxs-lookup"><span data-stu-id="2d49b-103">CertTimestampAuthenticodeLicense Function</span></span>

<span data-ttu-id="2d49b-104">为验证码 XrML 许可证添加时间戳。</span><span class="sxs-lookup"><span data-stu-id="2d49b-104">Time-stamps an Authenticode XrML license.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d49b-105">语法</span><span class="sxs-lookup"><span data-stu-id="2d49b-105">Syntax</span></span>

```cpp
HRESULT CertTimestampAuthenticodeLicense (
    [in]  PCRYPT_DATA_BLOB   pSignedLicenseBlob,
    [in]  LPCWSTR            pwszTimestampURI,
    [out] PCRYPT_DATA_BLOB   pTimestampSignatureBlob
);
```

## <a name="parameters"></a><span data-ttu-id="2d49b-106">参数</span><span class="sxs-lookup"><span data-stu-id="2d49b-106">Parameters</span></span>

 `pSignedLicenseBlob`\
 <span data-ttu-id="2d49b-107">[in] 要添加时间戳的已签名验证码 XrML 许可证。</span><span class="sxs-lookup"><span data-stu-id="2d49b-107">[in] The signed Authenticode XrML license to be time-stamped.</span></span> <span data-ttu-id="2d49b-108">请参阅 [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) 结构。</span><span class="sxs-lookup"><span data-stu-id="2d49b-108">See the [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure.</span></span>

 `pwszTimestampURI`\
 <span data-ttu-id="2d49b-109">[in] 时间戳服务器的 URI。</span><span class="sxs-lookup"><span data-stu-id="2d49b-109">[in] The time-stamp server's URI.</span></span>

 `pTimestampSignatureBlob`\
 <span data-ttu-id="2d49b-110">[out] 指向 CRYPT_DATA_BLOB 的指针，用于接收 base64 编码的时间戳签名。</span><span class="sxs-lookup"><span data-stu-id="2d49b-110">[out] A pointer to CRYPT_DATA_BLOB to receive the base64-encoded time-stamp signature.</span></span> <span data-ttu-id="2d49b-111">调用方负责 `pTimestampSignatureBlob` -> `pbData` `HepFree()` 在使用后释放。</span><span class="sxs-lookup"><span data-stu-id="2d49b-111">It is the caller's responsibility to free `pTimestampSignatureBlob`->`pbData` with `HepFree()` after use.</span></span> <span data-ttu-id="2d49b-112">请参阅 [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) 结构。</span><span class="sxs-lookup"><span data-stu-id="2d49b-112">See the [CRYPTOAPI_BLOB](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d49b-113">备注</span><span class="sxs-lookup"><span data-stu-id="2d49b-113">Remarks</span></span>

 <span data-ttu-id="2d49b-114">时间戳签名实际上是一条 PKCS #7 SignedData 消息，其内容是许可证签名中 SignatureValue 的二进制格式。</span><span class="sxs-lookup"><span data-stu-id="2d49b-114">The time-stamp signature is actually a PKCS #7 SignedData message whose content is the binary form of the SignatureValue from the license's signature.</span></span> <span data-ttu-id="2d49b-115">基本上，它充当许可证的副署。</span><span class="sxs-lookup"><span data-stu-id="2d49b-115">Basically, this acts as a counter-signature of the license.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d49b-116">返回值</span><span class="sxs-lookup"><span data-stu-id="2d49b-116">Return Value</span></span>

 <span data-ttu-id="2d49b-117">如果此函数成功，则返回 `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="2d49b-117">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="2d49b-118">否则，返回错误代码。</span><span class="sxs-lookup"><span data-stu-id="2d49b-118">Otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d49b-119">要求</span><span class="sxs-lookup"><span data-stu-id="2d49b-119">Requirements</span></span>

<span data-ttu-id="2d49b-120">**程序集**： clr.dll</span><span class="sxs-lookup"><span data-stu-id="2d49b-120">**Assembly**: clr.dll</span></span>

## <a name="see-also"></a><span data-ttu-id="2d49b-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="2d49b-121">See also</span></span>

- [<span data-ttu-id="2d49b-122">验证码</span><span class="sxs-lookup"><span data-stu-id="2d49b-122">Authenticode</span></span>](index.md)
