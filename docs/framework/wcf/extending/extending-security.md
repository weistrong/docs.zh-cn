---
description: 了解详细信息：扩展安全性
title: 扩展安全性
ms.date: 03/30/2017
helpviewer_keywords:
- security [WCF], extending
ms.assetid: a015a040-9fdf-4147-9ea9-f83b570be1d4
ms.openlocfilehash: 8dd514e16106ac5cdae072d92c7de66cefd39fe4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99685720"
---
# <a name="extending-security"></a><span data-ttu-id="72577-103">扩展安全性</span><span class="sxs-lookup"><span data-stu-id="72577-103">Extending Security</span></span>

<span data-ttu-id="72577-104">为了容纳新的声明类型和自定义令牌，你可以将 Windows Communication Foundation (WCF) 的安全基础结构扩展。</span><span class="sxs-lookup"><span data-stu-id="72577-104">To accommodate new claim types and custom tokens, you can extend the security infrastructure of Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="72577-105">本节中的主题将向您介绍如何完成此任务。</span><span class="sxs-lookup"><span data-stu-id="72577-105">The topics in this section show you how this is done.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="72577-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="72577-106">In This Section</span></span>  
  
 [<span data-ttu-id="72577-107">自定义凭据和凭据验证</span><span class="sxs-lookup"><span data-stu-id="72577-107">Custom Credential and Credential Validation</span></span>](custom-credential-and-credential-validation.md)  
 <span data-ttu-id="72577-108">说明在验证自定义凭据时如何使用标识模型。</span><span class="sxs-lookup"><span data-stu-id="72577-108">Explains how the Identity Model is used when validating custom credentials.</span></span>  
  
 [<span data-ttu-id="72577-109">自定义令牌</span><span class="sxs-lookup"><span data-stu-id="72577-109">Custom Tokens</span></span>](custom-tokens.md)  
 <span data-ttu-id="72577-110">安全令牌服务 (STS) 颁发的令牌通常为 SAML 令牌。</span><span class="sxs-lookup"><span data-stu-id="72577-110">Issued tokens from a Security Token Service (STS) are typically SAML tokens.</span></span> <span data-ttu-id="72577-111">本主题说明如何创建自定义令牌类型。</span><span class="sxs-lookup"><span data-stu-id="72577-111">This topic explains how to create a custom token type.</span></span>  
  
 [<span data-ttu-id="72577-112">自定义授权</span><span class="sxs-lookup"><span data-stu-id="72577-112">Custom Authorization</span></span>](custom-authorization.md)  
 <span data-ttu-id="72577-113">说明如何实现自定义授权。</span><span class="sxs-lookup"><span data-stu-id="72577-113">Explains how to implement custom authorization.</span></span>  
  
 [<span data-ttu-id="72577-114">重写服务标识以便进行身份验证</span><span class="sxs-lookup"><span data-stu-id="72577-114">Overriding the Identity of a Service for Authentication</span></span>](overriding-the-identity-of-a-service-for-authentication.md)  
 <span data-ttu-id="72577-115">介绍如何重写身份验证服务的标识。</span><span class="sxs-lookup"><span data-stu-id="72577-115">Describes how to override the identity of a service for authentication.</span></span>  
  
 [<span data-ttu-id="72577-116">如何：创建自定义客户端标识验证工具</span><span class="sxs-lookup"><span data-stu-id="72577-116">How to: Create a Custom Client Identity Verifier</span></span>](how-to-create-a-custom-client-identity-verifier.md)  
 <span data-ttu-id="72577-117">演示如何验证自定义终结点标识。</span><span class="sxs-lookup"><span data-stu-id="72577-117">Demonstrates how to validate a custom endpoint identity.</span></span>  
  
 [<span data-ttu-id="72577-118">如何：使用独立的 X.509 证书进行签名和加密</span><span class="sxs-lookup"><span data-stu-id="72577-118">How to: Use Separate X.509 Certificates for Signing and Encryption</span></span>](how-to-use-separate-x-509-certificates-for-signing-and-encryption.md)  
 <span data-ttu-id="72577-119">通常使用单个证书对消息进行签名和加密。</span><span class="sxs-lookup"><span data-stu-id="72577-119">Messages are typically signed and encrypted with a single certificate.</span></span> <span data-ttu-id="72577-120">本主题说明如何按照要求使用两个证书。</span><span class="sxs-lookup"><span data-stu-id="72577-120">This topic explains how two certificates can be used, when required.</span></span>  
  
 [<span data-ttu-id="72577-121">如何：更改 X.509 证书私钥的加密提供程序</span><span class="sxs-lookup"><span data-stu-id="72577-121">How to: Change the Cryptographic Provider for an X.509 Certificate's Private Key</span></span>](change-cryptographic-provider-x509-certificate-private-key.md)  
 <span data-ttu-id="72577-122">说明如何更改用于提供 x.509 证书的私钥的加密提供程序，以及如何将该提供程序集成到 Windows Communication Foundation (WCF) 框架中。</span><span class="sxs-lookup"><span data-stu-id="72577-122">Explains how to change the cryptographic provider used to provide an X.509 certificate's private key and how to integrate the provider into the Windows Communication Foundation (WCF) framework.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="72577-123">参考</span><span class="sxs-lookup"><span data-stu-id="72577-123">Reference</span></span>  

 <xref:System.ServiceModel.ServiceAuthorizationManager>  
  
 <xref:System.ServiceModel.Security>  
  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.IdentityModel.Policy>  
  
 <xref:System.IdentityModel.Tokens>  
  
 <xref:System.IdentityModel.Selectors>  
  
## <a name="related-sections"></a><span data-ttu-id="72577-124">相关章节</span><span class="sxs-lookup"><span data-stu-id="72577-124">Related Sections</span></span>  

 [<span data-ttu-id="72577-125">安全性</span><span class="sxs-lookup"><span data-stu-id="72577-125">Security</span></span>](../feature-details/security.md)  
  
 [<span data-ttu-id="72577-126">基本 WCF 编程</span><span class="sxs-lookup"><span data-stu-id="72577-126">Basic WCF Programming</span></span>](../basic-wcf-programming.md)  
  
## <a name="see-also"></a><span data-ttu-id="72577-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="72577-127">See also</span></span>

- [<span data-ttu-id="72577-128">安全性概述</span><span class="sxs-lookup"><span data-stu-id="72577-128">Security Overview</span></span>](../feature-details/security-overview.md)
