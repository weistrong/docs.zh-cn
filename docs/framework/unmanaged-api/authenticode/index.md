---
description: 详细了解：Authenticode（非托管 API 参考）
title: Authenticode（非托管 API 参考）
ms.date: 03/30/2017
ms.assetid: 7e8cc303-6e77-4116-aa8b-7ea297a3a467
ms.openlocfilehash: d7a1684fde900bfc01161193d0747b156c6856a8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772830"
---
# <a name="authenticode-unmanaged-api-reference"></a><span data-ttu-id="fb09b-103">Authenticode（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="fb09b-103">Authenticode (Unmanaged API Reference)</span></span>

<span data-ttu-id="fb09b-104">支持验证码 XrML 许可证创建和验证模块。</span><span class="sxs-lookup"><span data-stu-id="fb09b-104">Supports the Authenticode XrML license creation and verification module.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="fb09b-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="fb09b-105">In This Section</span></span>  

 [<span data-ttu-id="fb09b-106">_AxlGetIssuerPublicKeyHash 函数</span><span class="sxs-lookup"><span data-stu-id="fb09b-106">_AxlGetIssuerPublicKeyHash Function</span></span>](axlgetissuerpublickeyhash-function.md)  
 <span data-ttu-id="fb09b-107">检索与用于对指定证书进行签名的私钥关联的公钥的 SHA-1 哈希。</span><span class="sxs-lookup"><span data-stu-id="fb09b-107">Retrieves the SHA-1 hash of the public key associated with the private key that is used to sign the specified certificate.</span></span>  
  
 [<span data-ttu-id="fb09b-108">_AxlPublicKeyBlobToPublicKeyToken 函数</span><span class="sxs-lookup"><span data-stu-id="fb09b-108">_AxlPublicKeyBlobToPublicKeyToken Function</span></span>](axlpublickeyblobtopublickeytoken-function.md)  
 <span data-ttu-id="fb09b-109">从 CSP PUBLICKEYBLOB 格式计算强名称公钥标记。</span><span class="sxs-lookup"><span data-stu-id="fb09b-109">Computes the strong name public key token from a CSP PUBLICKEYBLOB format.</span></span>  
  
 [<span data-ttu-id="fb09b-110">_AxlRSAKeyValueToPublicKeyToken 函数</span><span class="sxs-lookup"><span data-stu-id="fb09b-110">_AxlRSAKeyValueToPublicKeyToken Function</span></span>](axlrsakeyvaluetopublickeytoken-function.md)  
 <span data-ttu-id="fb09b-111">将模数和指数转换为强名称公钥标记。</span><span class="sxs-lookup"><span data-stu-id="fb09b-111">Converts a Modulus and Exponent to a strong name public key token.</span></span>  
  
 [<span data-ttu-id="fb09b-112">CertFreeAuthenticodeSignerInfo 函数</span><span class="sxs-lookup"><span data-stu-id="fb09b-112">CertFreeAuthenticodeSignerInfo Function</span></span>](certfreeauthenticodesignerinfo-function.md)  
 <span data-ttu-id="fb09b-113">释放为 AXL_AUTHENTICODE_SIGNER_INFO 结构分配的资源。</span><span class="sxs-lookup"><span data-stu-id="fb09b-113">Frees resources allocated for the AXL_AUTHENTICODE_SIGNER_INFO structure.</span></span>  
  
 [<span data-ttu-id="fb09b-114">CertFreeAuthenticodeTimestamperInfo 函数</span><span class="sxs-lookup"><span data-stu-id="fb09b-114">CertFreeAuthenticodeTimestamperInfo Function</span></span>](certfreeauthenticodetimestamperinfo-function.md)  
 <span data-ttu-id="fb09b-115">释放为 AXL_AUTHENTICODE_TIMESTAMPER_INFO 结构分配的资源。</span><span class="sxs-lookup"><span data-stu-id="fb09b-115">Frees resources allocated for the AXL_AUTHENTICODE_TIMESTAMPER_INFO structure.</span></span>  
  
 [<span data-ttu-id="fb09b-116">CertTimestampAuthenticodeLicense 函数</span><span class="sxs-lookup"><span data-stu-id="fb09b-116">CertTimestampAuthenticodeLicense Function</span></span>](certtimestampauthenticodelicense-function.md)  
 <span data-ttu-id="fb09b-117">为由 CertCreateAuthenticodeLicense 创建的验证码 XrML 许可证添加时间戳。</span><span class="sxs-lookup"><span data-stu-id="fb09b-117">Time stamps an Authenticode XrML license created by CertCreateAuthenticodeLicense.</span></span>  
  
 [<span data-ttu-id="fb09b-118">CertVerifyAuthenticodeLicense 函数</span><span class="sxs-lookup"><span data-stu-id="fb09b-118">CertVerifyAuthenticodeLicense Function</span></span>](certverifyauthenticodelicense-function.md)  
 <span data-ttu-id="fb09b-119">验证验证码 XrML 许可证的有效性。</span><span class="sxs-lookup"><span data-stu-id="fb09b-119">Verifies the validity of an Authenticode XrML license.</span></span>  
  
 [<span data-ttu-id="fb09b-120">AXL_AUTHENTICODE_SIGNER_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="fb09b-120">AXL_AUTHENTICODE_SIGNER_INFO Structure</span></span>](axl-authenticode-signer-info-structure.md)  
 <span data-ttu-id="fb09b-121">定义验证码签署人的信息。</span><span class="sxs-lookup"><span data-stu-id="fb09b-121">Defines the Authenticode signer information.</span></span>  
  
 [<span data-ttu-id="fb09b-122">AXL_AUTHENTICODE_TIMESTAMPER_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="fb09b-122">AXL_AUTHENTICODE_TIMESTAMPER_INFO Structure</span></span>](axl-authenticode-timestamper-info-structure.md)  
 <span data-ttu-id="fb09b-123">定义验证码时间戳签署人的信息。</span><span class="sxs-lookup"><span data-stu-id="fb09b-123">Defines the Authenticode time stamper information.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fb09b-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fb09b-124">See also</span></span>

- [<span data-ttu-id="fb09b-125">非托管 API 参考</span><span class="sxs-lookup"><span data-stu-id="fb09b-125">Unmanaged API Reference</span></span>](../index.md)
