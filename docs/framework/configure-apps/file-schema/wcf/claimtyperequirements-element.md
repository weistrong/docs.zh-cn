---
description: 了解详细信息： <claimTypeRequirements> 元素
title: <claimTypeRequirements> 元素
ms.date: 03/30/2017
ms.assetid: a26efe73-4bad-4731-8cad-27f00d54354b
ms.openlocfilehash: 9553c129c246a5f4980d597406bee19ea949bdcc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638907"
---
# <a name="claimtyperequirements-element"></a><span data-ttu-id="c6593-103">\<claimTypeRequirements> 元素</span><span class="sxs-lookup"><span data-stu-id="c6593-103">\<claimTypeRequirements> element</span></span>

<span data-ttu-id="c6593-104">指定所需声明类型的集合。</span><span class="sxs-lookup"><span data-stu-id="c6593-104">Specifies a collection of required claim types.</span></span>  
  
 <span data-ttu-id="c6593-105">在联合方案中，服务规定有关传入凭据的要求。</span><span class="sxs-lookup"><span data-stu-id="c6593-105">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="c6593-106">例如，传入凭据必须具有某组声明类型。</span><span class="sxs-lookup"><span data-stu-id="c6593-106">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="c6593-107">此集合中的每个子元素都指定希望出现在联合凭据中的必选和可选的声明类型。</span><span class="sxs-lookup"><span data-stu-id="c6593-107">Each child element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>  
  
 <span data-ttu-id="c6593-108">声明类型需求由在已颁发令牌中请求的声明类型的 URI 和布尔参数组成，其中布尔参数可指示该声明类型在已颁发的令牌中是必选还是可选的。</span><span class="sxs-lookup"><span data-stu-id="c6593-108">A claim type requirement consists of the URI of the claim type requested in the issued token along with a Boolean parameter that indicates whether that claim type is required in the issued token, or is optional.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6593-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="c6593-109">See also</span></span>

- <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ClaimTypeElement>
- <xref:System.ServiceModel.Configuration.SecurityElementBase.IssuedTokenParameters%2A>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="c6593-110">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="c6593-110">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="c6593-111">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="c6593-111">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="c6593-112">使用自定义绑定的安全功能</span><span class="sxs-lookup"><span data-stu-id="c6593-112">Security Capabilities with Custom Bindings</span></span>](../../../wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="c6593-113">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="c6593-113">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [\<add>](add-of-claimtyperequirements.md)
- [<span data-ttu-id="c6593-114">绑定</span><span class="sxs-lookup"><span data-stu-id="c6593-114">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="c6593-115">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="c6593-115">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="c6593-116">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="c6593-116">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
- [<span data-ttu-id="c6593-117">如何：使用 SecurityBindingElement 创建自定义绑定</span><span class="sxs-lookup"><span data-stu-id="c6593-117">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="c6593-118">自定义绑定安全性</span><span class="sxs-lookup"><span data-stu-id="c6593-118">Custom Binding Security</span></span>](../../../wcf/samples/custom-binding-security.md)
