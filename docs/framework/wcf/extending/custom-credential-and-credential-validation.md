---
description: 了解详细信息：自定义凭据和凭据验证
title: 自定义凭据和凭据验证
ms.date: 03/30/2017
helpviewer_keywords:
- credentials [WCF], custom
- credentials [WCF]
- custom credentials [WCF]
- credential validation [WCF]
- credentials [WCF], validation
ms.assetid: da831bec-e281-4d44-b343-437b5eef688e
ms.openlocfilehash: f1ceb8cf46cca01ac31faeb9485cbeb6c8663d31
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99735304"
---
# <a name="custom-credential-and-credential-validation"></a><span data-ttu-id="b26d6-103">自定义凭据和凭据验证</span><span class="sxs-lookup"><span data-stu-id="b26d6-103">Custom Credential and Credential Validation</span></span>

<span data-ttu-id="b26d6-104">WCF) Windows Communication Foundation (的安全性基于服务与客户端之间的凭据交换。</span><span class="sxs-lookup"><span data-stu-id="b26d6-104">Security in Windows Communication Foundation (WCF) is based on the exchange of credentials between services and clients.</span></span> <span data-ttu-id="b26d6-105">大多数安全方案均可使用常见的凭据类型来实现，如 Windows (Kerberos)、用户名和密码以及证书。</span><span class="sxs-lookup"><span data-stu-id="b26d6-105">Most security scenarios can be satisfied using common credential types, such as Windows (Kerberos), username and passwords, and certificates.</span></span> <span data-ttu-id="b26d6-106">而本节中的主题针对需要使用新类型的凭据的情况说明如何处理和验证这些新类型。</span><span class="sxs-lookup"><span data-stu-id="b26d6-106">However, if a new type of credential is required, the topics in this section explain how to handle and validate new types.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b26d6-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="b26d6-107">In This Section</span></span>  

 [<span data-ttu-id="b26d6-108">如何：创建使用自定义证书验证程序的服务</span><span class="sxs-lookup"><span data-stu-id="b26d6-108">How to: Create a Service that Employs a Custom Certificate Validator</span></span>](how-to-create-a-service-that-employs-a-custom-certificate-validator.md)  
 <span data-ttu-id="b26d6-109">说明如何通过从类继承来自定义 WCF 验证 <xref:System.IdentityModel.Selectors.X509CertificateValidator> 。</span><span class="sxs-lookup"><span data-stu-id="b26d6-109">Explains how to customize WCF validation by inheriting from the <xref:System.IdentityModel.Selectors.X509CertificateValidator> class.</span></span>  
  
 [<span data-ttu-id="b26d6-110">演练：创建自定义客户端和服务凭据</span><span class="sxs-lookup"><span data-stu-id="b26d6-110">Walkthrough: Creating Custom Client and Service Credentials</span></span>](walkthrough-creating-custom-client-and-service-credentials.md)  
 <span data-ttu-id="b26d6-111">演示如何扩展 <xref:System.ServiceModel.Description.ClientCredentials> 和 <xref:System.ServiceModel.Description.ServiceCredentials> 类以容纳新的凭据类型。</span><span class="sxs-lookup"><span data-stu-id="b26d6-111">Demonstrates how to extend the <xref:System.ServiceModel.Description.ClientCredentials> and <xref:System.ServiceModel.Description.ServiceCredentials> classes to accommodate new credential types.</span></span> <span data-ttu-id="b26d6-112">这是介绍如何创建自定义凭据类型的系列主题中的第一个主题。</span><span class="sxs-lookup"><span data-stu-id="b26d6-112">This is first in a series of topics that enable creation of custom credential types.</span></span>  
  
 [<span data-ttu-id="b26d6-113">如何：创建自定义安全令牌提供程序</span><span class="sxs-lookup"><span data-stu-id="b26d6-113">How to: Create a Custom Security Token Provider</span></span>](how-to-create-a-custom-security-token-provider.md)  
 <span data-ttu-id="b26d6-114">说明如何创建安全令牌提供程序来处理新的凭据类型并返回凭据的新令牌。</span><span class="sxs-lookup"><span data-stu-id="b26d6-114">Explains how to create a security token provider to handle new credential types and return new tokens for the credential.</span></span> <span data-ttu-id="b26d6-115">这是该系列主题中的第二个主题。</span><span class="sxs-lookup"><span data-stu-id="b26d6-115">This is the second topic in the series.</span></span>  
  
 [<span data-ttu-id="b26d6-116">如何：创建自定义安全令牌身份验证器</span><span class="sxs-lookup"><span data-stu-id="b26d6-116">How to: Create a Custom Security Token Authenticator</span></span>](how-to-create-a-custom-security-token-authenticator.md)  
 <span data-ttu-id="b26d6-117">说明如何创建自定义身份验证器来验证新的凭据类型。</span><span class="sxs-lookup"><span data-stu-id="b26d6-117">Explains how to create a custom authenticator to authenticate a new credential type.</span></span> <span data-ttu-id="b26d6-118">这是该系列主题中的第三个主题。</span><span class="sxs-lookup"><span data-stu-id="b26d6-118">This is the third topic in the series.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="b26d6-119">参考</span><span class="sxs-lookup"><span data-stu-id="b26d6-119">Reference</span></span>  

 <xref:System.ServiceModel.Security>  
  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.IdentityModel.Policy>  
  
 <xref:System.IdentityModel.Tokens>  
  
 <xref:System.IdentityModel.Selectors>  
  
 <xref:System.IdentityModel.Selectors.X509CertificateValidator>  
  
 <xref:System.ServiceModel.Description.ClientCredentials>  
  
 <xref:System.ServiceModel.Description.ServiceCredentials>  
  
## <a name="related-sections"></a><span data-ttu-id="b26d6-120">相关章节</span><span class="sxs-lookup"><span data-stu-id="b26d6-120">Related Sections</span></span>  

 [<span data-ttu-id="b26d6-121">身份验证</span><span class="sxs-lookup"><span data-stu-id="b26d6-121">Authentication</span></span>](../feature-details/authentication-in-wcf.md)  
  
 [<span data-ttu-id="b26d6-122">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="b26d6-122">Federation and Issued Tokens</span></span>](../feature-details/federation-and-issued-tokens.md)  
  
 [<span data-ttu-id="b26d6-123">授权</span><span class="sxs-lookup"><span data-stu-id="b26d6-123">Authorization</span></span>](../feature-details/authorization-in-wcf.md)  
  
## <a name="see-also"></a><span data-ttu-id="b26d6-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="b26d6-124">See also</span></span>

- [<span data-ttu-id="b26d6-125">安全性</span><span class="sxs-lookup"><span data-stu-id="b26d6-125">Security</span></span>](../feature-details/security.md)
